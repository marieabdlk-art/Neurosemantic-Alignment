# Hypotheses

This document defines the initial falsifiable hypotheses for Neurosemantic Alignment v0.1.

The hypotheses are intentionally conservative. They do not assume literal reconstruction of thought, consciousness, or private mental content.

---

## H1 — Syntax variability and neural switching

### Hypothesis

Subjects with higher variability of syntactic complexity will show higher transition entropy between functional brain states involving DMN, FPN, and SN.

### Language features

- variance of dependency depth;
- variance of sentence length;
- variance of clause density;
- syntactic entropy;
- autocorrelation of syntactic complexity;
- changepoints in syntactic complexity trajectory.

### Neural features

- transition entropy between latent FC states;
- dwell time variability;
- SN-mediated switching index;
- dynamic FC variability;
- metastability index.

### Expected relationship

```text
syntax_variability ~ neural_transition_entropy
```

### Conservative expected effect

```text
r > 0.25 after controls
```

---

## H2 — Narrative segmentation and Salience Network switching

### Hypothesis

Narrative fragmentation and abrupt thematic shifts will correlate with stronger Salience Network involvement in switching between neural states.

### Language features

- narrative segmentation score;
- topic shift frequency;
- abrupt changes in emotional valence;
- abrupt changes in temporal orientation;
- transition markers such as “but”, “however”, “stop”, “then”, “suddenly”.

### Neural features

- SN-FPN coupling;
- SN-DMN coupling;
- anterior insula participation coefficient;
- ACC participation coefficient;
- transition probability through SN-dominant states.

### Expected relationship

```text
narrative_segmentation ~ SN_switching_index
```

---

## H3 — Semantic graph modularity and functional network modularity

### Hypothesis

Subjects whose semantic graphs show stronger modular organization may also show stronger modularity in functional brain network organization.

### Language features

- semantic graph modularity;
- concept community structure;
- semantic hubness;
- effective semantic diameter;
- entropy of degree distribution.

### Neural features

- functional network modularity;
- participation coefficient;
- global efficiency;
- local efficiency;
- hub structure.

### Expected relationship

```text
semantic_graph_modularity ~ functional_network_modularity
```

### Required controls

This hypothesis is highly vulnerable to topic and genre confounds. It must be tested:

- within genre;
- across genres;
- with topic-matched corpora;
- against shuffled semantic graphs;
- against LLM-generated style imitation.

---

## H4 — Abstract language and DMN-FPN coupling

### Hypothesis

Abstract reflective language may be associated with increased integration between DMN and FPN, especially during task-based inner speech or autobiographical reasoning.

### Language features

- abstractness score;
- epistemic modality;
- self-reference;
- metacognitive markers;
- causal and conditional constructions;
- long-range discourse dependencies.

### Neural features

- DMN-FPN coupling;
- mPFC-DLPFC connectivity;
- PCC-FPN coupling;
- angular gyrus participation coefficient;
- integrated DMN-FPN latent state probability.

### Expected relationship

```text
abstract_reflective_language ~ DMN_FPN_coupling
```

---

## H5 — Language regime transitions and neural latent states

### Hypothesis

Transitions between latent language modes may align above chance with transitions between latent neural states during task-based inner speech or spontaneous narrative.

### Language modes

- analytical;
- reflective;
- perceptual;
- transition / salience;
- abstract-integrative.

### Neural states

- FPN-dominant;
- DMN-dominant;
- SN-transition;
- sensory-motor;
- integrated DMN-FPN.

### Methods

- hidden Markov models;
- hidden semi-Markov models;
- dynamic time warping;
- sequence alignment;
- permutation testing.

### Expected relationship

```text
alignment(language_state_sequence, neural_state_sequence) > permutation_baseline
```

---

## Negative controls

The project must include negative controls.

### Control 1 — Shuffled author labels

Randomly reassign language profiles to neural profiles.

Expected result:

```text
alignment ≈ chance
```

### Control 2 — Shuffled text order

Keep the same words and sentences but destroy temporal order.

Expected result:

```text
dynamic features should degrade
```

### Control 3 — Genre-only baseline

Use only genre labels to predict neural features.

Expected result:

```text
full language model > genre baseline
```

### Control 4 — LLM imitation baseline

Generate style imitations of author text using an LLM.

If LLM imitations predict neural features as well as real texts, the model may be capturing superficial style rather than subject-level neurosemantic structure.

---

## Rejection criteria

The framework should be rejected or substantially revised if:

- no hypothesis outperforms baseline models;
- effects disappear after controlling for genre and text length;
- effects are unstable across preprocessing pipelines;
- effects fail leave-one-subject-out validation;
- LLM imitations produce equivalent alignment;
- permutation tests show no above-chance structure.
