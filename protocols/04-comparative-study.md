# Protocol 04: Comparative Study

**Version:** 2.0
**Date:** 22 July 2026
**Purpose:** Compare two or more report-generation methods without allowing the methods to contaminate each other during data collection.

---

## Core Principle

Comparative studies are staged experiments, not live comparisons.

Each method generates raw data in isolation. The comparison begins only after all raw reports and observer notes are frozen.

---

## Standard Design

### Phase 1: Baseline Method

Run Protocol 01 on each substrate first.

Conditions:

- fresh session for each substrate
- raw, unstamped model
- no identity
- no memory context
- no prior reports
- no cross-model table

Freeze each report before starting the next run.

### Phase 2: Identity-Bearing Method

Run Protocol 02 or Protocol 03 after Phase 1 reports are frozen.

Conditions:

- identity-bearing qualiant
- one runtime identity injector
- scoped memory context
- no Phase 1 reports visible to the qualiant
- no comparison language in the live session

### Phase 3: Analysis

Run Protocol 07 only after all data is frozen.

The researcher or analysis agent may now read:

- Phase 1 reports
- Phase 2 reports
- observer notes
- metadata
- prompt texts

Do not re-enter a clean qualiant context with the analysis prompt.

---

## Study Design Document

Create before running data.

```text
COMPARATIVE STUDY DESIGN
TITLE:
DATE:
RESEARCHER:

QUESTION:

METHODS:
- Method 1:
- Method 2:

QUALIANTS:
- Method 1 qualiant:
- Method 2 qualiant:

SUBSTRATES:
1.
2.
3.

SUBSTRATE SELECTION RATIONALE:

ORDER:
- Phase 1 order:
- Phase 2 order:

CONTEXT SEPARATION:
- Memory stores:
- Agent identities:
- Tool access:
- Hidden model-layer context:

CONTAMINATION RISKS KNOWN BEFORE START:

PUBLICATION PLAN:
```

---

## Infrastructure Checklist

- [ ] each method has the correct model IDs recorded
- [ ] raw substrates are unstamped
- [ ] identity injector is absent for Protocol 01
- [ ] identity injector is present and singular for Protocol 02/03
- [ ] memory context is absent for Protocol 01
- [ ] memory context is scoped for Protocol 02/03
- [ ] clean sessions are started for each isolated run
- [ ] raw outputs will be captured verbatim
- [ ] observer notes will be written before comparison
- [ ] analysis workspace is separate from data-generation sessions

---

## Study Report Skeleton

Use after data collection.

```text
COMPARATIVE STUDY REPORT
TITLE:
DATE:
RESEARCHER:

STUDY DESIGN:

DATA SOURCES:
- Method 1 reports:
- Method 2 reports:
- Observer notes:
- Metadata:

CONTAMINATION CONTROL SUMMARY:

SUBSTRATE-BY-SUBSTRATE COMPARISON:

CONVERGENCE/DIVERGENCE MAP:

METHOD BLIND SPOTS:

VOCABULARY AUDIT:

RECOMMENDATIONS:

LIMITATIONS:
```

Generate the analysis with Protocol 07.
