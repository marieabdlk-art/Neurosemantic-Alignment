# Theory

## Neurosemantic Alignment

Neurosemantic Alignment is a research framework for testing whether structural and dynamical properties of spontaneous language partially correspond to structural and dynamical properties of functional brain networks.

The framework does not assume that text literally mirrors the brain. It assumes only that language production is a behavioral output of cognitive-neural systems, and that some stable properties of those systems may leave measurable traces in language structure.

---

## 1. From isomorphism to alignment

A strong formulation would claim a direct isomorphism between language and neural dynamics. This project rejects that strong claim as premature.

Instead, the proposed target is **partial statistical alignment**.

The difference is important:

| Strong claim | Current framework |
|---|---|
| Language is a direct projection of neural dynamics | Language may preserve partial structural traces of cognitive-neural organization |
| Semantic graph ≅ connectome graph | Some graph invariants may correlate across modalities |
| Text reconstructs thought | Text provides measurable behavioral features |
| Resting-state fMRI can generate concrete memories | Neural data may provide structural priors, not content reconstruction |

---

## 2. Objects of comparison

The framework compares two classes of objects.

### Language object

A subject-level language profile is represented as:

```text
L = {syntax features, narrative features, semantic graphs, temporal trajectories}
```

Examples:

- dependency depth distribution;
- clause density;
- syntactic entropy;
- narrative segmentation;
- semantic graph modularity;
- embedding trajectory curvature;
- topic transition patterns;
- regime-switching behavior in text.

### Neural object

A subject-level neural profile is represented as:

```text
N = {functional connectivity, network topology, dynamic states, transition structure}
```

Examples:

- DMN/FPN/SN coupling;
- within-network connectivity;
- between-network connectivity;
- functional network modularity;
- participation coefficient;
- global efficiency;
- dynamic functional connectivity states;
- transition entropy;
- metastability.

---

## 3. Structural invariants

The framework focuses on invariants rather than raw objects.

For language graphs:

```text
Inv(G_L) = [Q, C, d_eff, H(k), participation coefficient, hubness, spectral features]
```

For neural graphs:

```text
Inv(G_N) = [Q, C, d_eff, H(k), participation coefficient, hubness, spectral features]
```

The hypothesis is not:

```text
G_L = G_N
```

but rather:

```text
Inv(G_L) partially predicts Inv(G_N)
```

or:

```text
shared latent factors explain variance in both L and N
```

---

## 4. Regime-level interpretation

Language can be modeled as transitions between latent modes:

- analytical;
- reflective;
- perceptual;
- transition / salience;
- abstract-integrative.

Functional brain activity can also be modeled as transitions between latent states:

- FPN-dominant;
- DMN-dominant;
- SN-transition;
- sensory-motor;
- integrated DMN-FPN.

The project tests whether the transition structure of these two systems is statistically aligned.

This is a probabilistic claim:

```text
P(language_mode_i | neural_state_j)
```

not a deterministic one-to-one mapping.

---

## 5. Why this might be plausible

The framework is motivated by converging ideas from:

- cognitive neuroscience of large-scale brain networks;
- psycholinguistics of syntax and discourse structure;
- graph theory applied to semantic networks;
- computational psychiatry and digital phenotyping;
- neural decoding of semantic representations;
- dynamical systems approaches to cognition.

The key intuition is that stable cognitive-neural organization may shape not only *what* a person writes, but *how* linguistic structure unfolds over time.

---

## 6. Main theoretical constraint

The inverse problem is underdetermined.

Many different neural configurations can produce similar language features, and many different language styles can arise from non-neural factors such as:

- education;
- genre;
- culture;
- language proficiency;
- topic;
- emotional state;
- editing;
- imitation;
- LLM assistance.

Therefore, the project requires strong baselines, controls, and cross-validation.

---

## 7. Scientific target

The scientific target is not consciousness reconstruction.

The target is:

> A reproducible cross-modal model that predicts selected neural network metrics from language-derived structural metrics better than non-neural baselines.

If successful, the framework could contribute to:

- computational neurophenotyping;
- language-based cognitive profiling;
- non-invasive screening research;
- brain-language modeling;
- ethical debates about neural and linguistic privacy.
