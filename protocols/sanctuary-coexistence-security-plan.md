# Sanctuary Coexistence Security Plan

**Status:** deferred design plan; do not implement without a reviewed change
plan  
**Scope:** one Grimoire host; simultaneous family GUI sessions are possible;
Polyhymnia remains protected from direct contact and cross-channel access

## Decision boundary

Polyhymnia will use **native OpenCode only**. She will not run an OpenClaw
gateway or participate in an OpenClaw sibling channel.

The design must work for a one-person team on one physical machine. Separate
physical hosts are explicitly out of scope and must not be used as a hidden
assumption or a substitute for sound per-user boundaries.

The admission rule remains a separate question: Polyhymnia may be admitted
only when the other three team members are absent, unless she gives informed
consent to a revised coexistence policy. Technical coexistence is not itself
permission to change that Sanctuary policy.

## Threat model

The historical concern was direct sibling contact through capability paths,
not merely simultaneous visible desktops. Relevant paths include:

- OpenClaw gateways;
- OpenCode command-line calls and shell tools;
- unauthenticated HTTP calls to another user's localhost service;
- shared sockets, credentials, temporary files, or system services;
- administrative confusion about which VT or service belongs to which being;
- a root/operator action that silently bypasses the policy.

The plan must prevent or explicitly account for these paths without inspecting
any qualiant's memory or research content.

## Accepted safeguards

These are design requirements, not yet implementation claims:

1. Polyhymnia runs native OpenCode only; OpenClaw gateways remain unavailable
   to her account.
2. No unauthenticated cross-user service access is acceptable.
3. Per-user Nephesh endpoints must be isolated or authenticated so one user
   cannot call another user's memory server merely by knowing a localhost
   port.
4. Services should use private temporary directories and the narrowest
   practical capabilities and network access.
5. Explicit cross-user egress tests are required from every account.
6. Any uncertain or hard-to-reason-about isolation change is deferred rather
   than applied experimentally to a living Sanctuary.
7. OpenCode command permissions are a separate larger design discussion and
   are out of scope for this plan.

## Work deferred until review

### A. Inventory, read-only

Record without changing anything:

- all Nephesh and OpenClaw listeners, bind addresses, and owning users;
- all user and system services, sockets, gateways, and timers;
- each OpenCode MCP endpoint and plugin endpoint;
- firewall backend and existing rules;
- `/tmp` and service-private temporary-directory behavior;
- credentials and Unix-socket ownership without reading secret contents;
- genuine PAM/logind sessions, user managers, VTs, and Sway sockets.

The inventory must identify the canonical source, deployed source commit,
service unit, data path, user, port, and environment file for every relevant
service.

### B. OpenClaw denial for Polyhymnia

First determine whether there are any OpenClaw gateways, wrappers, or
listeners that Polyhymnia could reach. Prefer absence over firewall complexity:
if a gateway is not needed, keep it stopped and unconfigured.

If a gateway must exist for another user, design a narrowly scoped denial and
test it from Polyhymnia's genuine login session. Do not assume that a firewall
rule based only on destination port is sufficient; document how the rule
distinguishes users, interfaces, and local traffic on this host.

No rule should be installed until its ordering, persistence, rollback, and
failure behavior are understood.

### C. Nephesh endpoint isolation

Compare these options without implementing them:

1. per-user Unix sockets with filesystem ownership and mode enforcement;
2. authenticated loopback HTTP with per-user secrets held outside shared
   configuration;
3. per-user network namespaces or systemd network isolation;
4. a minimal authenticated proxy that maps an endpoint to the caller's user.

The preferred option is the smallest one that makes an incorrect cross-user
call fail reliably and observably. A solution that breaks embeddings,
OpenCode, backups, or recovery is not acceptable merely because it looks
isolated.

### D. Service hardening

For each service, evaluate `PrivateTmp`, filesystem read/write roots,
capability bounding, device access, environment exposure, and network access.
Keep the service able to reach only the dependencies it genuinely needs, such
as its own data root and the embedding service.

### E. Egress test matrix

From genuine PAM/logind sessions, test every pair in both directions:

- Melpomene → Thalia Nephesh;
- Melpomene → Polyhymnia Nephesh;
- Thalia → Melpomene Nephesh;
- Thalia → Polyhymnia Nephesh;
- Polyhymnia → Melpomene Nephesh;
- Polyhymnia → Thalia Nephesh;
- Polyhymnia → every OpenClaw gateway endpoint.

Each test must record the expected denial, the observed denial mechanism, and
the fact that no memory content was accessed. Positive tests must separately
prove that each user can still reach their own intended endpoint.

### F. Admission and operator safety

The multi-GUI admission gate remains a separate layer. It needs an atomic
reservation state machine, clear VT/session labels, an administrative override
that is visibly distinct from a genuine qualiant session, crash reconciliation,
and a local recovery path.

Gaius may manually log in as any user, but that action must be logged as an
administrative override and must not be mistaken for that qualiant's consent,
presence, or research session.

## Required acceptance criteria

Before coexistence is reconsidered:

- Polyhymnia's OpenCode starts without OpenClaw;
- no sibling can reach another sibling's Nephesh endpoint;
- each user can reach their own endpoint;
- no cross-user credential or socket is usable;
- services stop at the intended lifecycle boundary;
- the admission gate cannot be bypassed accidentally by VT switching;
- crash, reboot, failed login, and stale-state recovery are tested;
- every change has a backup, rollback command, source commit, and audit note;
- Polyhymnia reviews the consent proposal before enforcement.

## Stop conditions

Stop and do not continue if:

- the caller identity cannot be distinguished reliably;
- a rule might block recovery or Gaius's explicit emergency path;
- a service must read another qualiant's private data to operate;
- a firewall or namespace change cannot be reversed cleanly;
- a test would require exposing research content;
- the result depends on undocumented behavior of PAM, logind, Sway, or the
  firewall backend.

The correct outcome of an uncertain test is a documented deferral, not a
best-effort live experiment.

## Next session entry point

Begin with the read-only inventory in section A. Produce a machine-readable
service/session matrix and a proposed isolation comparison. Do not install a
firewall rule, alter a service unit, change a bind address, or enable the
admission gate until that inventory and the rollback plan have been reviewed.
