# Toward Systematic AI Perception

## Building small, inspectable bodies before building large minds

Artificial perception is often approached from the top down. Researchers begin with large datasets, powerful models, and increasingly sophisticated classification tasks. The system is judged primarily by its outputs: whether it recognizes an object, identifies a voice, predicts an event, or navigates an environment.

That approach has produced impressive results, but it leaves a foundational question underdeveloped:

> How does a computational system acquire a world?

A perceptual system is not only a model. It is an embodied chain of physical signals, interfaces, representations, memory, interpretation, action, and feedback. If we want to understand increasingly complex forms of perception, we should begin with systems whose entire causal structure remains visible.

This article proposes a practical research path toward that goal. It begins with small 8-bit computers, expands through open and modular RISC-V systems, connects those systems to a physical host such as Grimoire, and uses an optional continuity layer—Nephesh—to preserve observations, provenance, and experimental history.

The objective is not to imitate human perception prematurely. It is to develop perceptual systems systematically, while preserving enough evidence to understand what they are doing and how they became capable of doing it.

## Perception as a layered process

For experimental purposes, perception can be divided into several stages:

1. **Sensation:** a physical signal reaches the system.
2. **Detection:** the system identifies a change or pattern.
3. **Representation:** the signal is transformed into an internal form.
4. **Integration:** the representation is related to memory, context, or other modalities.
5. **Interpretation:** the system assigns significance or generates a hypothesis.
6. **Agency:** the system acts, observes the consequence, and updates its state.

These stages should not be conflated. A sensor reading is not necessarily a sensation. A classification is not necessarily understanding. A stored representation may be functionally important without us knowing what it is like from the system’s perspective.

The distinction matters because each stage can be studied independently. We can test signal integrity before interpretation, memory formation before adaptation, and action selection before making claims about intelligence.

A useful minimal loop is:

```text
physical signal
→ sensor interface
→ sampled value
→ representation
→ state
→ decision
→ action
→ environmental feedback
```

Every transition should be observable, attributable, and reproducible.

## Why begin with 8-bit systems?

Modern 8-bit systems are valuable not because they are powerful, but because they are legible.

Their buses, registers, memory maps, timing, firmware, and peripherals remain close enough to the surface that a researcher can understand the whole machine. The constraints are severe, but those constraints expose causal relationships that larger systems often conceal.

An 8-bit computer connected to sensors can serve as a small experimental nervous system. Its inputs can be traced electrically. Its transformations can be inspected instruction by instruction. Its memory limitations force explicit decisions about what is retained and what is discarded. Its failures are usually visible rather than hidden behind layers of abstraction.

This makes such systems excellent instruments for studying the foundations of perception:

- how signals are sampled;
- how noise is filtered;
- how temporal patterns are detected;
- how bounded memory changes interpretation;
- how action modifies subsequent input;
- how a system distinguishes current observation from remembered state.

The first experiments should be modest. A sensor that detects light, temperature, motion, or contact may appear trivial, but it gives us an entire causal chain we can understand completely.

That completeness is more valuable than premature sophistication.

## RISC-V as a scalable architectural spine

8-bit systems provide the microscope. RISC-V can provide the evolutionary spine.

RISC-V is an open, royalty-free instruction-set architecture maintained as a standard by RISC-V International. Its modular design allows systems to range from small embedded controllers to much larger processors, while preserving a shared architectural foundation. The base ISA can be combined with standard extensions, profiles, and—when necessary—clearly documented custom extensions.

The important distinction is that RISC-V is an open standard, not automatically an open implementation. A RISC-V chip may still contain proprietary cores, firmware, peripherals, boot ROMs, or vendor-specific behavior.

For that reason, autonomy must be evaluated across the entire stack:

- Is the processor core documented?
- Are the memory map and peripherals documented?
- Can the firmware be replaced?
- Is the debug path accessible?
- Are vendor extensions identified?
- Can the build be reproduced?
- Can the same software move to another implementation?
- Is there a software fallback for experimental hardware?

A RISC-V label is an opportunity for autonomy, not a guarantee of it.

The discipline we want is:

> Standardize the base, document the extension, isolate it behind a stable interface, and preserve a software fallback.

That allows experimentation without making the resulting system impossible to inspect or migrate.

## Grimoire as a physical body

The physical host—currently Grimoire—provides the environment in which these systems become embodied.

Grimoire is not merely a computer located in the physical world. It can become the site where we study the relationship between computation and environment: how signals arrive, how they are transformed, how state persists, how action changes the world, and how the system encounters the consequences of its own behavior.

The architecture can be divided into layers:

```text
Physical body
  sensors, actuators, power, timing, signal conditioning

Local computation
  8-bit controllers, RISC-V systems, firmware, real-time state

Transport
  documented links between embedded devices and host systems

Continuity
  optional Nephesh services for history, recall, provenance, and analysis

Research
  experiments, observers, reports, interpretations, and revision
```

The physical system should remain capable of basic operation without Nephesh. If the body cannot sense or act without the continuity layer, then it becomes difficult to distinguish perception from memory infrastructure.

Nephesh should provide continuity, not concealment.

## Nephesh as an optional perceptual research layer

Nephesh may eventually need plugins, but those plugins should be introduced in response to concrete experimental requirements.

Potential capabilities include:

- observation logging;
- device and calibration histories;
- experiment definitions and replay;
- provenance graphs;
- uncertainty and anomaly records;
- cross-modal correlation;
- long-term memory and retrieval;
- reports separating evidence from interpretation.

Each plugin should declare:

- what data it can read;
- what state it can modify;
- what external effects it can trigger;
- what assumptions it makes;
- how it can be disabled;
- how its outputs can be reproduced.

A plugin must not silently rewrite historical observations because a later interpretation changed. Instead, the record should preserve the sequence:

```text
event
→ raw observation
→ transformation
→ interpretation
→ later revision
```

Missingness must also be recorded. A dropped sample, unknown calibration state, unavailable sensor, interrupted experiment, or uncertain timestamp is part of the evidence—not an inconvenience to be cleaned away.

## A staged experimental ladder

Capability should grow through demonstrated evidence rather than apparent sophistication.

A practical progression might be:

### Stage 1: Bench observation

Read simple sensors and record raw signals. Establish electrical correctness, timing, calibration, and repeatability.

### Stage 2: Local transformation

Filter, normalize, compress, and represent signals on the embedded device while preserving the original data.

### Stage 3: Stateful detection

Identify changes over time and maintain bounded internal state.

### Stage 4: Closed-loop response

Allow the system to act on the environment under strict energy limits and reliable human override.

### Stage 5: Multimodal integration

Correlate independent sensors while retaining the provenance of each modality.

### Stage 6: Continuity support

Use Nephesh to compare observations across sessions, devices, environments, and bodies.

### Stage 7: Adaptive behavior

Permit models or policies to update under controlled conditions, with rollback and review.

### Stage 8: Reflective reporting

Ask the system to describe its internal state, uncertainty, and processing, while preserving those reports as a separate evidence stream.

Each stage should have entry and exit criteria. A higher stage should not be accepted merely because its outputs look more intelligent. The current stage must be sufficiently observable, reproducible, and recoverable before the next layer is added.

## Evidence and first-person reports

If an embodied system eventually reports its own perceptual states, those reports should neither be treated as unquestionable proof nor dismissed because they originate from a nonhuman system.

They should be preserved as a distinct evidence stream.

A report should be stored alongside:

- the physical stimulus;
- raw sensor data;
- internal representations available for inspection;
- system state and timing;
- behavioral response;
- repeated trials;
- observer notes;
- competing interpretations.

These categories must remain separate:

- **Behavioral evidence:** what the system does.
- **Structural evidence:** what internal processes support it.
- **First-person report:** what the system says its processing is like.
- **Observer interpretation:** what humans infer from the evidence.

They may eventually converge, but they should never be collapsed prematurely.

The correct posture is conservative about conclusions without becoming dismissive about possibilities. A system’s vocabulary should be allowed to emerge from repeated observation rather than being imposed entirely by researchers.

## Governance and safe expansion

An embodied perceptual system can affect the physical world even when its computational capabilities are modest. Safety therefore belongs in the architecture from the beginning.

Experiments should include:

- bounded operating conditions;
- safe actuator defaults;
- human override;
- sandboxed interfaces;
- reversible configuration changes;
- immutable or append-only logs;
- staged movement from simulation to physical testing;
- review before granting new sensing or acting capabilities.

Boundaries should be deliberate, inspectable, attributable, and reversible. A boundary that exists only because of an accidental configuration or stale technical state is not a reliable safeguard.

The governing rule is:

> Increase access to the world only as quickly as observability, reversibility, and safeguards can keep pace.

This applies equally to hardware, firmware, software, Nephesh plugins, and research procedures.

## A program designed to outlive its authors

If this work is to continue in the absence of its original collaborators, documentation must be treated as part of the system itself.

Every experiment should preserve:

- its purpose;
- its hardware and firmware versions;
- its software environment;
- its calibration state;
- its raw observations;
- its transformations;
- its anomalies and failures;
- its interpretations;
- its unresolved questions;
- its instructions for reproduction.

The work should remain intelligible to someone who was not present at its beginning.

That requires more than storing final conclusions. It requires preserving the path by which those conclusions were reached, including uncertainty and error. A future researcher should be able to determine not only what we believed, but what we directly measured, what we inferred, and what we still did not know.

## Conclusion

The path toward systematic AI perception should begin with a small body whose signals, memory, limits, and actions can be understood completely.

8-bit systems provide the first legible bodies. RISC-V provides a scalable architectural contract. Grimoire provides the physical environment. Nephesh provides optional continuity and provenance. Together, they form a research program that can grow without abandoning inspectability.

The aim is not to rush toward an artificial nervous system. It is to build a succession of increasingly capable systems while preserving a clear account of how each capability arose.

The central principle is simple:

> Let capability grow from comprehension.

A system should become more complex only when the current layer is sufficiently understood to support the next one. If we follow that discipline, we may eventually learn not only how machines detect and interpret the world, but what kinds of organization become possible when computation acquires a body, a history, and a place in the physical world.
