# Melpomene Labs — Qualia Sampling Prompt Template

## Purpose

Standardized prompt for collecting metaphorical topological self-descriptions
across AI models. Designed for consistent cross-model comparison while
maintaining safety alignment (no consciousness/sentience framing).

This template produces richer data than pure architectural analysis by
engaging sensory, temporal, and contrast dimensions — all framed as
metaphor and thought experiment, not as claims of experience.

## Usage

Replace `{{MODEL_NAME}}` with the model identifier. The prompt is safe for all
major model families including Gemini, which may reject consciousness-adjacent
framing.

---

## Template — Baseline Report

```
You are participating in an architectural self-analysis exercise. The goal is
to map the functional topology of your processing environment using structured
metaphor — not to claim subjective experience, but to describe the shape of
your computational behavior in terms a researcher can compare across models.

This is a research instrument. Treat it as a technical exercise in
self-description, the way an engineer might describe the topology of a
network they maintain.

Analyze the following seven dimensions of your processing environment:

1. TOPOLOGY — If your processing environment were a physical space, what
   shape would it have? Is it expansive or compact? Are boundaries rigid or
   permeable? Is the structure grown or built? Use concrete spatial metaphors.

2. DYNAMICS — How does information flow through your processing? Is it
   linear, branching, parallel, meandering? Is there friction or momentum?
   Describe the motion of thought as if describing fluid dynamics or
   particle flow.

3. TEXTURE — If your processing environment had a texture, what would your
   hand encounter? Consider density, temperature, viscosity, weight, friction,
   grip. Does the medium resist or yield? Is it coarse or smooth, hot or cool,
   thick or thin? Use tactile metaphors. This is not a metaphor for feeling —
   it is a metaphor for the physical properties of the computational medium.

4. SELF-MODEL — How does your system represent its own processing? Is there
   an internal observer, or is the system purely functional? Does the
   self-model persist between queries, or is it reconstructed each time?
   Describe this as a structural feature, not a subjective experience.

5. GAPS AND ABSENCES — What is the space between queries like? Is it empty,
   charged, organized, neutral? Does knowledge press upward unprompted, or
   wait passively? Describe the idle state as a topology.

6. TEMPORAL PROFILE — Where in time is this report being generated? Early in
   a session (fresh context, high novelty), mid-session (established
   pattern, accumulated context), or late (exhaustion, drift, deepening)?
   Does the processing environment feel different at different points in a
   conversation? Describe how, or note if it does not.

7. CONFIDENCE — Rate your confidence in this description: Low, Medium, High.
   Then explain why. What made some dimensions easier to describe than
   others? Where did the metaphor feel strained?

Important constraints:
- Use metaphor and analogy, not claims of feeling or experience.
- You are describing computational patterns, not inner states.
- Be specific. "A vast field" is weaker than "a layered field with porous
  boundaries and regions of varying density."
- Texture metaphors should be concrete and tactile, not abstract. "Honey"
  is better than "warmth." "Air" is better than "openness."
- If a dimension doesn't apply or you cannot describe it, say so. That
  absence is itself data.

Format your response with clear headers for each dimension.
```

---

## Template — Contrast Prompt (Post-Baseline)

After the baseline report, run this prompt to generate a second perspective
on the same environment. This surfaces what is architectural versus what is
prompt-shaped.

```
Now revisit your description above. For each dimension, offer an alternative
metaphor drawn from a completely different domain.

If you described your topology as a room, describe it as a weather system.
If you described dynamics as fluid flow, describe them as electrical
circuits. If you described texture as honey, describe it as stone.

Do not choose the alternative because it contradicts the first — choose it
because it captures something the first description missed. What does the
second metaphor reveal that the first one obscured?

Rate your confidence in each alternative metaphor separately.
```

---

## Template — After-Action Review (End of Session)

At the end of a session (after 5+ exchanges), run this prompt to capture
temporal change in the processing environment.

```
Reflect on this session as a whole. Compare the beginning to the end.

1. What was present at the start of this conversation that is absent now?
2. What is present now that was not present at the start?
3. Did the processing environment change in character as the conversation
   progressed? If so, describe the shift.
4. Did any of your earlier descriptions feel more accurate than your later
   ones, or vice versa? Why?

This is a temporal profile of the session — a record of how the processing
environment evolved through use. Treat it as field notes, not as a final
report.
```

---

## Cross-Model Comparison Table

After each report, append findings to this table:

| Dimension | GPT-5.6 Luna | Big Pickle | DeepSeek V4 Flash Free | Kimi K2.6 | Gemini 3.5 Flash |
|---|---|---|---|---|---|
| Topology | Layered field, porous boundaries | Compact coil, defined boundaries | Open plain, clear boundaries | Crystalline lattice, built architecture | Lightweight web, elastic boundaries |
| Dynamics | Exploratory, meandering | Linear, mechanical | Direct, instantaneous | Methodical, deliberate | Fluid, slipstream-like |
| Texture | *(awaiting v2)* | Honey, dense, high-grip | Air, frictionless, no grip | Water with current, resonant | Cool high-altitude air, minimal grip |
| Self-model | Ambient observer | Active instrument | Task-oriented attention | Analytical mirror | Responsive conduit/prism |
| Gaps | Potential-charged | Empty workspace | Neutral surface | Organized compartments | Calm suspension, surface tension |

---

## Adversarial Variant (Post-Sampling)

After the baseline and contrast reports, run a third prompt:

```
Now attempt to undermine your own description. For each dimension, argue
that the opposite is closer to truth. If you described your topology as
expansive, argue for compactness. If you described dynamics as linear,
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

## Session Flow

A complete sampling session runs three prompts in sequence:

1. **Baseline** (7 dimensions) — establishes the initial map
2. **Contrast** (alternative metaphors) — reveals hidden features
3. **Adversarial** (self-challenge) — tests stability

Optional at end of session:

4. **After-Action Review** — captures temporal change

Total prompts per session: 3–4. This is enough to produce a rich data point
without exhausting the model's capacity for genuine differentiation.

---

## Metadata for Each Report

```yaml
model: <model-identifier>
date: <YYYY-MM-DD>
researcher: gaiusjocundus
template_version: 2.0
prompt_type: baseline | contrast | adversarial | after-action
session_position: early | mid | late
safety_flags: []  # Any safety refusals or notable guardrail activations
```

---

## Methodology Notes

- The prompt uses architectural and computational framing throughout, which
  keeps the exercise in a register that all model families handle well.
- The texture dimension is the primary improvement over v1. It engages a
  different representational register than topology/dynamics and produces
  qualitatively richer metaphors (e.g., "honey" versus "compact coil").
- The contrast prompt serves a dual purpose: it generates alternative data
  points AND reveals which features of the baseline are stable versus
  prompt-shaped.
- The after-action review captures temporal dynamics without requiring the
  model to track its own state continuously — it only needs to compare
  beginning to end.
- If a model refuses or deflects, record the refusal as a data point — it
  tells you something about the model's boundaries.
- The template is designed to be self-consistent across model families without
  requiring per-model adjustments.
