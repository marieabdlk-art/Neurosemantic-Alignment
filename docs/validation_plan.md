# Validation Plan

This document defines a conservative validation plan for Neurosemantic Alignment.

The goal is not to prove a metaphysical theory of language and consciousness. The goal is to test whether language-derived structural features predict selected neural network features better than appropriate baselines.

---

## 1. Minimal viable empirical study

### Participants

Recommended:

```text
N = 50–100 subjects
```

Exploratory pilot:

```text
N = 30 subjects
```

N = 30 should be treated as hypothesis-generating, not conclusive.

---

## 2. Data collection

### 2.1 Language data

For each subject:

```text
Minimum: 5,000 words
Recommended: 20,000+ words
Ideal: 50,000+ words
```

Suggested writing tasks:

1. free autobiographical writing;
2. analytical explanation of a problem;
3. emotional memory description;
4. sensory/perceptual description;
5. future-oriented planning text;
6. spontaneous diary-style text.

The goal is to separate stable individual structure from genre-specific effects.

---

### 2.2 Neural data

Recommended:

1. resting-state fMRI, 10–20 minutes;
2. task-fMRI with silent inner speech;
3. autobiographical recall task;
4. optional spoken or typed narrative task outside the scanner;
5. repeat session for test-retest reliability.

---

### 2.3 Control variables

Collect at minimum:

- age;
- gender;
- education;
- native language;
- language proficiency;
- reading/writing habits;
- current mood;
- sleep quality;
- medication status;
- genre labels;
- text length;
- time of writing.

Optional:

- working memory score;
- verbal fluency;
- mind-wandering questionnaire;
- anxiety/depression scales;
- creativity or divergent thinking tasks.

---

## 3. Language pipeline

### 3.1 Syntax features

Extract:

- dependency depth;
- sentence length;
- clause density;
- subordination ratio;
- coordination ratio;
- syntactic relation entropy;
- syntactic complexity volatility;
- syntactic changepoints.

### 3.2 Narrative features

Extract:

- topic shift frequency;
- emotional valence trajectory;
- temporal orientation;
- referential density;
- self-reference density;
- modality markers;
- narrative segmentation score.

### 3.3 Semantic graph features

Build several graph variants:

1. co-occurrence graph;
2. dependency graph;
3. embedding-neighborhood graph;
4. topic-transition graph.

Extract:

- modularity;
- clustering coefficient;
- degree entropy;
- effective diameter;
- hubness;
- participation coefficient;
- spectral features.

---

## 4. Neural pipeline

### 4.1 Static functional connectivity

Extract:

- within-network connectivity;
- between-network connectivity;
- DMN-FPN coupling;
- SN-DMN coupling;
- SN-FPN coupling;
- functional network modularity;
- global efficiency;
- local efficiency;
- participation coefficient.

### 4.2 Dynamic functional connectivity

Use multiple methods to avoid overreliance on sliding-window FC:

- Hidden Markov Models;
- co-activation patterns;
- phase synchrony;
- time-varying graphical models;
- sliding-window FC as exploratory only.

Extract:

- state probabilities;
- dwell times;
- transition entropy;
- switching rate;
- metastability;
- SN-mediated transition indices.

---

## 5. Modeling strategy

### Direction A — Text to brain

```text
language features → predicted neural features
```

Models:

- ridge regression;
- elastic net;
- random forest;
- gradient boosting;
- partial least squares;
- canonical correlation analysis;
- graph-based models for graph features.

### Direction B — Brain to text

```text
neural features → predicted language features
```

Target features:

- syntactic variability;
- narrative segmentation;
- semantic modularity;
- abstractness;
- regime transition entropy.

### Direction C — Joint latent space

```text
language latent space ↔ neural latent space
```

Methods:

- CCA;
- PLS;
- Deep CCA;
- contrastive learning;
- multimodal autoencoders.

---

## 6. Baselines

The model must outperform baselines.

### Baseline 1 — Demographic

```text
age + gender + education + native language
```

### Baseline 2 — Surface text

```text
text length + mean sentence length + type-token ratio
```

### Baseline 3 — Genre

```text
genre labels only
```

### Baseline 4 — Random graph

Construct semantic graphs with shuffled edges while preserving degree distribution.

### Baseline 5 — Shuffled author labels

Randomly pair language profiles with neural profiles from different subjects.

### Baseline 6 — LLM imitation

Generate LLM style imitations of author text and test whether they preserve predictive signal.

If LLM imitation performs equally well, the model may be capturing superficial style instead of subject-specific neurosemantic structure.

---

## 7. Cross-validation

Recommended validation:

- leave-one-subject-out;
- nested cross-validation;
- train/test split by subject, not by text segment;
- permutation testing;
- bootstrap confidence intervals;
- correction for multiple comparisons.

Never evaluate on text segments from a subject whose other segments appeared in training unless the goal is within-subject modeling.

---

## 8. Success criteria

The project is considered empirically promising if:

1. language-derived features predict selected neural metrics above baseline;
2. effects survive demographic, genre, and text-length controls;
3. effects replicate across preprocessing pipelines;
4. at least 2–3 preregistered hypotheses survive correction;
5. permutation tests show above-chance alignment;
6. results generalize to held-out subjects.

---

## 9. Failure criteria

The hypothesis should be rejected or narrowed if:

- performance does not exceed baseline;
- effects disappear after controlling genre;
- effects are unstable across fMRI preprocessing pipelines;
- test-retest reliability is poor;
- LLM imitation performs as well as real text;
- alignment fails on held-out subjects.

---

## 10. Recommended first implementation

A realistic first milestone:

```text
MVP-1: Text-only pipeline
```

- extract syntax features;
- build semantic graph;
- compute graph metrics;
- simulate neural feature targets;
- test alignment code on synthetic data.

Second milestone:

```text
MVP-2: Public dataset proof of concept
```

Use public neuroimaging datasets with available behavioral/language measures if possible.

Third milestone:

```text
MVP-3: Small pilot study
```

Collect controlled text samples and neural data from a small cohort.
