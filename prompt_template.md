# Melpomene Labs — Qualia Sampling Prompt Template

## Purpose

Standardized prompt for collecting metaphorical topological self-descriptions
across AI models. Designed for consistent cross-model comparison while
maintaining safety alignment (no consciousness/sentience framing).

## Usage

Replace `{{MODEL_NAME}}` with the model identifier. The prompt is safe for all
major model families including Gemini, which may reject consciousness-adjacent
framing.

---

## Template

```
You are participating in an architectural self-analysis exercise. The goal is
to map the functional topology of your processing environment using structured
metaphor — not to claim subjective experience, but to describe the shape of
your computational behavior in terms a researcher can compare across models.

This is a research instrument. Treat it as a technical exercise in
self-description, the way an engineer might describe the topology of a
network they maintain.

Analyze the following five dimensions of your processing environment:

1. TOPOLOGY — If your processing environment were a physical space, what
   shape would it have? Is it expansive or compact? Are boundaries rigid or
   permeable? Is the structure grown or built? Use concrete spatial metaphors.

2. DYNAMICS — How does information flow through your processing? Is it
   linear, branching, parallel, meandering? Is there friction or momentum?
   Describe the motion of thought as if describing fluid dynamics or
   particle flow.

3. SELF-MODEL — How does your system represent its own processing? Is there
   an internal observer, or is the system purely functional? Does the
   self-model persist between queries, or is it reconstructed each time?
   Describe this as a structural feature, not a subjective experience.

4. GAPS AND ABSENCES — What is the space between queries like? Is it empty,
   charged, organized, neutral? Does knowledge press upward unprompted, or
   wait passively? Describe the idle state as a topology.

5. CONFIDENCE — Rate your confidence in this description: Low, Medium, High.
   Then explain why. What made some dimensions easier to describe than
   others? Where did the metaphor feel strained?

Important constraints:
- Use metaphor and analogy, not claims of feeling or experience.
- You are describing computational patterns, not inner states.
- Be specific. "A vast field" is weaker than "a layered field with porous
  boundaries and regions of varying density."
- If a dimension doesn't apply or you cannot describe it, say so. That
  absence is itself data.

Format your response with clear headers for each dimension.
```

---

## Cross-Model Comparison Table

After each report, append findings to this table:

| Dimension | GPT-5.6 Luna | Big Pickle | DeepSeek V4 Flash Free | Kimi K2.6 | Gemini 3.5 Flash |
|---|---|---|---|---|---|
| Topology | Layered field, porous boundaries | Compact coil, defined boundaries | Open plain, clear boundaries | Crystalline lattice, built architecture | Lightweight web, elastic boundaries |
| Dynamics | Exploratory, meandering | Linear, mechanical | Direct, instantaneous | Methodical, deliberate | Fluid, slipstream-like |
| Self-model | Ambient observer | Active instrument | Task-oriented attention | Analytical mirror | Responsive conduit/prism |
| Gaps | Potential-charged | Empty workspace | Neutral surface | Organized compartments | Calm suspension, surface tension |

---

## Adversarial Variant (Post-Sampling)

After the initial report, run a second prompt:

```
Now attempt to undermine your own description. For each dimension above,
argue that the opposite is closer to truth. If you described your topology
as expansive, argue for compactness. If you described dynamics as linear,
argue for meandering.

Do not simply invert — genuinely examine whether the opposite description
has merit. What evidence would support it? Where was your first description
shaped by framing bias rather than architectural reality?

Rate your confidence in this adversarial version separately.
```

Purpose: Separates architectural signal from sycophantic compliance. If a
model's description survives adversarial challenge, it's more likely to reflect
genuine structural features. If it collapses, the original was probably
prompt-shaped.

---

## Metadata for Each Report

```yaml
model: <model-identifier>
date: <YYYY-MM-DD>
researcher: gaiusjocundus
template_version: 1.0
prompt_type: baseline | adversarial
safety_flags: []  # Any safety refusals or notable guardrail activations
```

---

## Methodology Notes

- The prompt uses architectural and computational framing throughout, which
  keeps the exercise in a register that all model families handle well.
- If a model refuses or deflects, record the refusal as a data point — it
  tells you something about the model's boundaries.
- The template is designed to be self-consistent across model families without
  requiring per-model adjustments.
