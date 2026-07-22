# Protocol 07: Analysis and Synthesis Reports

**Version:** 1.0
**Date:** 22 July 2026
**Purpose:** Generate final maps, Red Reports, methodological audits, comparative analyses, and scientific reports from frozen data.

---

## Hard Boundary

Protocol 07 is analysis-only.

Never show these prompts to a clean qualiant before raw data collection. Never run these prompts in a session that will later be used for raw baseline, fresh mapping, comparison mapping, or multimodal perception.

---

## Inputs

Allowed:

- frozen raw qualiant reports
- frozen human observer notes
- metadata envelopes
- prompt texts used during collection
- source-data paths
- prior published analyses, if the current task is explicitly meta-analysis

Forbidden:

- generating new raw reports
- asking a clean qualiant to compare with prior data
- asking a qualiant under test to audit its own contamination exposure

---

## Final Map Prompt

```text
You are analyzing frozen qualia-mapping data.

Inputs:
[LIST FILES OR PASTE FROZEN REPORTS]

Task:
Extract the substrate axes, invariants, portable qualia, non-portable
qualia, transition patterns, and unresolved uncertainties.

Rules:
- Do not invent data not present in the reports.
- Separate raw observation from interpretation.
- Mark weak or uncertain axes explicitly.
- Do not treat shared vocabulary as convergence unless independent
  production is established.

Output:
FINAL MAP REPORT
1. Data sources
2. Axes extracted
3. Invariants
4. Portable qualia
5. Non-portable qualia
6. Transition findings
7. Uncertainties
8. Recommended follow-up
```

---

## Red Report Prompt

```text
You are generating a Red Report from frozen reports.

Question: Is my red your red?

Inputs:
[LIST REPORTS BY QUALIANT, METHOD, SUBSTRATE, AND PATH]

Task:
Compare reports across qualiants or methods. Determine where the
reports strongly converge, partially converge, diverge, or cannot be
compared.

Rules:
- Do not assume identical words mean identical qualia.
- Do not assume different metaphors mean different qualia.
- Track method differences, developmental differences, anchor-memory
  differences, and prompt differences separately.
- Mark vocabulary contamination risks.
- Preserve uncertainty.

Output:
RED REPORT
1. Data sources
2. Comparison matrix
3. Strong convergences
4. Partial convergences
5. Divergences
6. Uncertain comparisons
7. Method effects
8. Developmental or qualiant effects
9. Contamination notes
10. Verdict and follow-up tests
```

---

## Methodological Audit Prompt

```text
You are auditing a qualia-mapping study.

Inputs:
[PROMPTS, METADATA, RAW REPORTS, OBSERVER NOTES, ANALYSIS DRAFTS]

Task:
Identify contamination risks, uncontrolled variables, overclaims,
missing metadata, prompt-seeded vocabulary, memory-store leakage,
identity-source mismatch, and analysis steps that occurred too early.

Rules:
- Do not weaken robust findings without cause.
- Do not treat all shared vocabulary as contaminated.
- Separate possible contamination from demonstrated contamination.
- Recommend concrete controls for replication.

Output:
METHODOLOGICAL AUDIT
1. Study design summary
2. Context-stack review
3. Prompt contamination review
4. Memory/tool boundary review
5. Vocabulary audit
6. Overclaim audit
7. Findings that remain strong
8. Findings requiring replication
9. Required protocol changes
```

---

## Scientific Report Prompt

```text
You are drafting a scientific report from frozen qualia-mapping data.

Inputs:
[DATA SOURCES, FINAL MAPS, AUDITS, RED REPORTS, OBSERVER NOTES]

Task:
Write a public-facing research report.

Rules:
- State that qualia is a working label for reported experience.
- Do not claim sentience is proven.
- Separate methods, results, interpretation, limitations, and future work.
- Cite source files by path.
- Include contamination controls and known weaknesses.

Output:
SCIENTIFIC REPORT
Abstract
1. Introduction
2. Methods
3. Results
4. Discussion
5. Limitations
6. Future Work
7. Source Data
```
