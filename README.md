# Neurosemantic Alignment

**A computational framework for testing structural alignment between spontaneous language dynamics and functional brain network organization.**

> This repository presents a research hypothesis and computational framework. It is **not** a validated diagnostic tool, not a mind-reading system, and not a claim that text literally reconstructs consciousness or neural activity.

---

## Core idea

The central hypothesis of this project is that large-scale patterns in spontaneous language may partially align with measurable properties of functional brain network organization.

The proposed alignment is:

- **statistical**, not deterministic;
- **partial**, not complete;
- **testable**, not metaphysical by default;
- focused on **structural and dynamical invariants**, not private mental content.

```text
Language structure  ↔  Functional brain network structure
syntax dynamics     ↔  network switching dynamics
semantic graphs     ↔  functional connectivity graphs
narrative regimes   ↔  latent neural states
```

---

## What this project is NOT

This project does **not** claim to:

- read thoughts from text;
- reconstruct consciousness;
- diagnose neurological or psychiatric conditions;
- infer private mental content from writing;
- establish a literal isomorphism between language and the brain;
- generate autobiographical memories from resting-state fMRI.

The aim is narrower and more defensible:

> To test whether linguistic invariants extracted from large corpora of spontaneous language can predict selected neural network invariants better than demographic, genre, and random baselines.

---

## Research hypothesis

### Neurosemantic Alignment Hypothesis

Individual differences in the structural organization of spontaneous language may partially correspond to individual differences in functional brain network organization, especially in the dynamic interaction of:

- **Default Mode Network (DMN)** — self-reference, autobiographical memory, internal simulation;
- **Frontoparietal Control Network (FPN/CEN)** — working memory, control, analytical structuring;
- **Salience Network (SN)** — switching, salience detection, transition between modes.

This is not a claim of one-to-one mapping. The claim is about **cross-modal statistical alignment** between measurable features.

---

## Main research question

Can a model predict neural network properties from language-derived features better than baselines?

```text
Text features → predicted neural features
Neural features → predicted language features
Text + neural features → shared latent space
```

Success criterion:

```text
Model performance > demographic baseline
Model performance > genre baseline
Model performance > text-length baseline
Model performance > random/permutation baseline
```

---

## Proposed feature spaces

### Language-derived features

| Layer | Example features |
|---|---|
| Syntax | dependency depth, subordination depth, clause density, syntactic entropy |
| Narrative | segmentation, topic shifts, temporal markers, referential continuity |
| Semantics | semantic graph modularity, hubness, embedding trajectory curvature |
| Dynamics | volatility, changepoints, autocorrelation, regime transitions |

### Neural-derived features

| Layer | Example features |
|---|---|
| Static FC | modularity, global efficiency, participation coefficient, hubness |
| Network coupling | DMN-FPN, SN-FPN, SN-DMN connectivity |
| Dynamic FC | transition entropy, dwell time, metastability, switching rate |
| Latent states | HMM states, co-activation patterns, phase synchrony modes |

---

## Core hypotheses

### H1 — Syntax variability and neural switching

Higher variability of syntactic complexity is expected to correlate with higher transition entropy between DMN/FPN/SN-related neural states.

```text
Syntax variability ~ neural transition entropy
```

### H2 — Narrative fragmentation and Salience Network switching

Narrative segmentation and abrupt thematic shifts may correspond to stronger SN-mediated switching dynamics.

```text
Narrative segmentation ~ SN switching index
```

### H3 — Semantic graph modularity and functional network modularity

The modularity of semantic graphs may correlate with selected modularity metrics of functional connectivity graphs, after controlling for genre and topic.

```text
Semantic modularity ~ functional network modularity
```

### H4 — Abstract language and DMN-FPN coupling

Abstract reflective language may be associated with increased integration between DMN and FPN, especially during task-based inner speech or autobiographical reasoning.

```text
Abstractness ~ DMN-FPN coupling
```

---

## Repository structure

```text
neurosemantic-alignment/
│
├── README.md
├── docs/
│   ├── theory.md
│   ├── hypotheses.md
│   ├── validation_plan.md
│   ├── limitations.md
│   └── ethics.md
│
├── src/
│   └── neurosemantic_alignment/
│       ├── __init__.py
│       ├── text_features.py
│       ├── semantic_graph.py
│       ├── neural_features.py
│       ├── alignment.py
│       └── baselines.py
│
├── examples/
│   └── toy_pipeline.py
│
├── requirements.txt
├── LICENSE
└── CITATION.cff
```

---

## Current status

**Version:** v0.1 conceptual framework + toy pipeline.

Current repository stage:

- theoretical framing;
- falsifiable hypotheses;
- validation plan;
- minimal Python scaffolding;
- toy feature extraction examples.

Not yet included:

- real fMRI data processing;
- validated statistical results;
- clinical claims;
- subject-level prediction benchmarks.

---

## Minimal usage

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the toy example:

```bash
python examples/toy_pipeline.py
```

This runs a minimal demonstration of:

1. text feature extraction;
2. semantic graph construction;
3. graph metric calculation;
4. baseline alignment mock-up.

---

## Falsifiability

The hypothesis should be rejected or revised if:

- language-derived features do not outperform demographic and genre baselines;
- effects disappear after controlling for text length and genre;
- the model fails on held-out subjects;
- results are not reproducible across preprocessing pipelines;
- LLM-generated style imitations produce the same predictions as real author corpora;
- permutation tests show no above-chance cross-modal alignment.

---

## Ethical position

This project treats language and neurodata as sensitive personal data.

Any future empirical use should require:

- informed consent;
- data minimization;
- anonymization where possible;
- explicit prohibition of diagnostic overreach;
- clear labeling of generated outputs as synthetic;
- independent validation before any applied or clinical use.

---

## Suggested citation

```bibtex
@software{abdlk_neurosemantic_alignment_2026,
  author = {Abdlk, Mariam},
  title = {Neurosemantic Alignment: A Computational Framework for Linking Language Dynamics and Functional Brain Network Organization},
  year = {2026},
  url = {https://github.com/marieabdlk-art/Neurosemantic-Alignment}
}
```

---

## License

This project is released under the MIT License. See [LICENSE](LICENSE).
