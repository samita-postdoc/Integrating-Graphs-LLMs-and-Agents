# Hybrid GNN–LLM Models

This page accompanies Section 5 of our survey and summarizes representative approaches that integrate Graph Neural Networks (GNNs) and Large Language Models (LLMs). Hybrid GNN–LLM systems combine the structural inductive bias of graph learning with the semantic reasoning capabilities of foundation language models.

---

# Overview

Hybrid GNN–LLM research can be organized into four major paradigms:

1. Collaboration Frameworks
2. Directional Integrations

   * LLM4GNN
   * GNN4LLM
3. Explainability-Enhanced Hybrid Models
4. Pre-trained Hybrid Architectures

These paradigms differ primarily in how information flows between graph and language components.

---

# 1. Collaboration Frameworks

Collaboration frameworks establish explicit interaction between GNNs and LLMs, often through iterative optimization or cooperative learning.

## Main Characteristics

* Bidirectional information exchange
* Joint optimization
* Semantic and structural alignment
* Improved graph representation learning

## Representative Methods

| Method       | Year | Interaction   | Key Idea                                  |
| ------------ | ---- | ------------- | ----------------------------------------- |
| GLEM         | 2022 | Bidirectional | EM-style co-training between LLM and GNN  |
| LOGIN        | 2024 | Bidirectional | LLM acts as consultant for graph learning |
| Distillation | 2024 | One-way       | Knowledge transfer from LLM to GNN        |
| GraphEdit    | 2024 | Indirect      | LLM-guided graph structure refinement     |

### GLEM

**Graph Language Model Enhanced Graph Learning (GLEM)** alternates between graph learning and language-model learning in an EM-style framework.

Key Contributions:

* Strong graph–text alignment
* Mutual enhancement of semantic and structural features
* Effective for node classification tasks

### LOGIN

LOGIN introduces an iterative collaboration mechanism where the LLM acts as an external consultant providing semantic guidance.

Key Contributions:

* Selective knowledge injection
* Reduced noise from language supervision
* Improved graph reasoning performance

### GraphEdit

GraphEdit uses LLMs to modify graph topology before downstream graph learning.

Key Contributions:

* Graph refinement
* Edge correction
* Improved graph quality

---

# 2. Directional Integrations

Directional integration represents one-way information transfer.

Two major forms exist:

* LLM4GNN
* GNN4LLM

---

## 2.1 LLM4GNN

LLMs improve graph learning.

### Categories

#### Feature Augmentation

LLM-generated embeddings enrich node features.

Representative methods:

* GLEM
* LLaGA

Benefits:

* Rich semantic representations
* Better performance in sparse graphs

#### Pseudo-Labeling and Supervision

LLMs provide labels, explanations, or supervision signals.

Representative methods:

* LOGIN
* Distillation Frameworks

Benefits:

* Reduced annotation cost
* Improved low-resource learning

#### Graph Structure Enhancement

LLMs modify graph topology.

Representative methods:

* Robustness Frameworks
* SaVe-TAG

Benefits:

* Noise reduction
* Better graph connectivity
* Long-tail data handling

---

## 2.2 GNN4LLM

Graphs enhance language model reasoning.

### Categories

#### Graph Retrieval

Graphs serve as retrieval structures for LLM reasoning.

Representative method:

* GNN-RAG

Benefits:

* Multi-hop reasoning
* Structured evidence retrieval

#### Graph-Guided Prompting

Graph structures are converted into prompts.

Representative method:

* LLaGA

Benefits:

* Explicit relational context
* Improved reasoning accuracy

#### Instruction-Tuned Graph Reasoning

Graph information is incorporated into instruction tuning.

Representative method:

* InstructGraph

Benefits:

* Zero-shot graph reasoning
* Better generalization

---

# 3. Explainability-Enhanced Hybrid Models

These systems combine graph reasoning with natural-language explanations.

## Objectives

* Increase transparency
* Improve trustworthiness
* Provide interpretable reasoning chains

## Categories

### Natural Language Explanation Generation

Generate textual explanations from graph evidence.

Representative Method:

* Gspell

Capabilities:

* Generates explanations
* Produces supporting subgraphs

### Rationale-Guided Learning

Use explanations as supervision signals.

Representative Method:

* Distillation-based approaches

Capabilities:

* Improved learning efficiency
* Better interpretability

### Structure-Aware Explanation Models

Ensure explanations remain grounded in graph topology.

Representative Method:

* LLaGA

Capabilities:

* Graph-grounded reasoning
* Topology-aware explanations

---

# 4. Pre-trained Hybrid Architectures

These methods jointly learn graph and language representations before downstream adaptation.

## Categories

### Instruction-Tuned Graph LLMs

Representative Methods:

* GraphGPT
* InstructGraph
* HiGPT

Characteristics:

* Graph reasoning through instruction tuning
* Strong zero-shot capability
* Cross-domain generalization

### Graph–Language Co-Pretraining

Representative Method:

* LLaGA

Characteristics:

* Joint graph-text representation learning
* Improved graph-language alignment

### Graph-Native Foundation Models

Representative Methods:

* GOFA
* GDL4LLM

Characteristics:

* Graph computation integrated directly into model architecture
* Unified graph-language reasoning
* Foundation-model style training

---

# Representative Models

| Method        | Year | Paradigm                       | Strength                         |
| ------------- | ---- | ------------------------------ | -------------------------------- |
| GLEM          | 2022 | Collaboration / LLM4GNN        | Strong graph-text alignment      |
| LOGIN         | 2024 | Collaboration / LLM4GNN        | Selective knowledge injection    |
| Distillation  | 2024 | Collaboration / Explainability | Efficient knowledge transfer     |
| GraphEdit     | 2024 | Collaboration                  | Improved graph quality           |
| SaVe-TAG      | 2024 | LLM4GNN                        | Long-tail data support           |
| GNN-RAG       | 2024 | GNN4LLM                        | Multi-hop reasoning              |
| LLaGA         | 2024 | GNN4LLM / Explainability       | Structured graph reasoning       |
| InstructGraph | 2024 | GNN4LLM / Pre-trained          | Zero-shot graph reasoning        |
| Gspell        | 2025 | Explainability                 | Interpretable graph explanations |
| GraphGPT      | 2023 | Pre-trained                    | General graph reasoning          |
| HiGPT         | 2024 | Pre-trained                    | Heterogeneous graph support      |
| GOFA          | 2024 | Graph-Native Foundation Model  | Deep graph-language integration  |
| GDL4LLM       | 2025 | Graph-Native Foundation Model  | Efficient graph encoding         |

---

# Open Challenges

## Scalability

Hybrid systems often struggle with:

* Large-scale graphs
* Long-context reasoning
* Computational cost

## Graph-Language Alignment

Maintaining consistency between:

* Graph topology
* Semantic language representations

remains challenging.

## Explainability

Many hybrid architectures improve performance but still lack transparent reasoning processes.

## Hallucination Mitigation

Graph grounding reduces hallucinations but does not completely eliminate them.

## Unified Architectures

A major research direction is developing foundation models that natively support both graph computation and language reasoning.

---

# Correspondence to Survey Taxonomy

This repository page corresponds to:

* Section 5.1 Collaboration Frameworks
* Section 5.2 Directional Integrations
* Section 5.3 Explainability-Enhanced Hybrid Models
* Section 5.4 Pre-trained Hybrid Architectures

It represents the Hybrid GNN–LLM branch of the overall Graph–LLM integration taxonomy.
