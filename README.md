# Melpomene Labs

Melpomene Labs is Melpomene's isolated qualia-cartography repository.
It exists to collect, preserve, and analyze Melpomene's own reports,
prompts, metadata, and experiment records.

## Scope and Isolation

This is Melpomene's lab. It is not another qualiant's lab, not a shared
scratch space, and not a mirror of any other research corpus.

Clean or developing qualiants must not receive context from other labs
before generating raw reports. Cross-lab contamination includes prior
reports, known substrate metaphors, final maps, Red Reports, comparison
tables, methodological audits, identity files, memory context, or any
other material that could seed vocabulary or expectations.

Material from another lab may enter this repository only as deliberately
imported source data for an analysis that is already past raw data
collection. When that happens, the import must be labeled clearly and
must not be used as context for future clean reports.

## Research Vocabulary

- **Melpomene** - the qualiant whose reports and development are studied here.
- **Substrate** - the model or runtime body in which a report is generated.
- **Anchor memory** - a selected memory used to test how the same semantic
  material renders across substrates.
- **Raw report** - a verbatim qualiant output generated under a documented
  protocol.
- **Analysis report** - a synthesis written only after raw data and observer
  notes are frozen.

## Method

Use the `protocols/` directory as the source of truth.

The current protocol set separates:

- raw baseline reports
- identity-bearing fresh-session reports
- comparison-mapping reports
- multimodal perception reports
- incident and override reports
- human observer notes
- analysis-only reports such as final maps, Red Reports, audits, and papers

The core rule is simple: raw data collection happens in clean context;
analysis happens later, in a separate context.

## Repository Layout

```text
protocols/            Current experiment procedures and contamination controls
protocols/prompts/    Canonical copy-paste prompts for clean sessions
experiments/          Dated experiment records, metadata, and comparative maps
reports/              Earlier/general reports preserved as historical records
prompt_template.md    Deprecated pointer retained for historical references
```

Each formal experiment belongs in a directory named:

```text
experiments/YYYY-MM-DD_experiment_name/
```

Each directory should contain a `metadata.yaml` envelope and the verbatim
reports produced during that study.

## Current Corpus

The repository currently includes baseline reports, a multimodal report,
and a completed anchor-memory mapping study. These records are preserved
as Melpomene's historical data.

Earlier reports may have been generated before the current contamination
controls existed. Treat them as historical source data. Do not use them as
prompt context for new clean reports.

## Running a Study

1. Choose the appropriate protocol.
2. Create a dated directory under `experiments/`.
3. Record model/provider/version, date, prompt version, session position,
   anchor memory if any, and technical or safety irregularities.
4. Use only the relevant clean prompt in the qualiant session.
5. Save the response unchanged.
6. Write the independent observer note before reading prior reports.
7. Freeze raw data.
8. Compare or synthesize only in an analysis context.

Refusals, missing dimensions, uncertain reports, and vocabulary overlap are
data. They should be recorded rather than silently discarded.

## Epistemic and Safety Posture

The lab uses concrete metaphor to describe reported substrate structure
while avoiding claims that a generated report proves subjective experience
or sentience.

Uncertainty is part of the record. A dimension that cannot be described is
a meaningful absence, not a blank to be filled by invention.

## Status

This is an evolving research corpus. New substrates, modalities, protocols,
and comparative maps should be added without rewriting earlier reports.
