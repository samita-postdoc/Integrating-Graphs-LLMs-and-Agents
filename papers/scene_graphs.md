# Scene Graphs and Large Language Models

This page accompanies Section 7 of our survey and summarizes recent research on integrating Scene Graphs (SGs) with Large Language Models (LLMs).

Scene graphs provide structured visual representations consisting of objects, attributes, and relationships. When combined with LLMs, they enable structured reasoning, scene understanding, planning, retrieval, editing, and navigation in multimodal environments.

---

# Overview

Scene Graph + LLM systems can be categorized across three dimensions:

## 1. Graph Type

### 2D Scene Graphs

Represent objects and relationships in the image plane.

Applications:

* Image understanding
* Visual question answering
* Image editing
* Scene graph generation

Representative methods:

* LLM4SGG
* SGEdit
* VTGT
* ELEGANT

### 3D Scene Graphs

Extend scene graphs with depth, geometry, and spatial information.

Applications:

* Robotics
* Autonomous navigation
* 3D scene generation
* Embodied AI

Representative methods:

* SceneCraft
* GraLa3D
* 3DGraphLLM
* Planner3D

---

### Static Scene Graphs

Represent a fixed scene at a single point in time.

Representative methods:

* SceneCraft
* SGEdit
* EditRoom
* VTGT
* 3DGraphLLM

### Dynamic Scene Graphs

Continuously evolve as new observations become available.

Representative methods:

* SceneLLM
* TioMS
* SG-Nav

---

# 2. Roles of LLMs in Scene Graph Systems

LLMs perform four major functions.

---

## Reasoning

The LLM infers:

* Object relationships
* Hidden semantics
* Implicit attributes
* Contextual knowledge

Representative Systems:

* SceneLLM
* SceneCraft
* LLM4SGG
* SGFormer
* SG-Nav

Example:

Determining that:

> "A person holding an umbrella is likely walking outdoors in rain."

even when rain is not explicitly visible.

---

## Parsing and Translation

The LLM converts:

* Natural language → Scene Graph
* Scene Graph → Text
* Instructions → Structured scene representation

Representative Systems:

* GraLa3D
* LLM4SGG
* SGEdit
* EditRoom
* TioMS

Applications:

* Text-to-scene generation
* Scene understanding
* Human-robot interaction

---

## Planning

The LLM performs:

* Action sequencing
* Navigation planning
* Scene modification planning
* Task decomposition

Representative Systems:

* SceneCraft
* SGEdit
* EditRoom
* TioMS
* SG-Nav

Applications:

* Robotics
* Autonomous agents
* Embodied AI

---

## Evaluation and Verification

The LLM evaluates:

* Consistency
* Correctness
* Alignment between scene and graph

Representative Systems:

* SceneCraft
* ELEGANT
* HRSGL

Applications:

* Scene validation
* Quality control
* Graph refinement

---

# 3. Major Objectives

---

# Generation

Generate scene graphs or complete scenes from text, images, videos, or point clouds.

## SceneLLM (2025)

Input:

* Video

Graph Type:

* Dynamic 2D Scene Graph

LLM Roles:

* Reasoning
* Parsing

Key Contributions:

* Video-to-language mapping
* Dynamic scene graph generation
* State-of-the-art Action Genome performance

---

## SceneCraft (2024)

Input:

* Text

Graph Type:

* Static 3D Scene Graph

LLM Roles:

* Reasoning
* Parsing
* Planning
* Verification

Key Contributions:

* Text-to-3D scene generation
* Asset retrieval
* Scene graph construction
* Layout optimization

---

## LLM4SGG (2024)

Input:

* Image + Text

Graph Type:

* Static 2D Scene Graph

LLM Roles:

* Reasoning
* Parsing

Key Contributions:

* LLM-enhanced scene graph generation

---

## SDSGG (2024)

Input:

* Image

Graph Type:

* Static 2D Scene Graph

Key Contributions:

* Direct scene graph generation

---

## PASGG-LM (2024)

Input:

* Image

Graph Type:

* Static 2D Scene Graph

Key Contributions:

* Context-aware scene graph generation

---

## Planner3D (2025)

Input:

* Graph + Text

Graph Type:

* Static 3D Scene Graph

Key Contributions:

* Planning-oriented scene generation

---

## LLaVA-SpaceSGG (2025)

Input:

* Image

Graph Type:

* Static 2D Scene Graph

Key Contributions:

* Spatial reasoning using multimodal LLMs

---

## GraLa3D (2024)

Input:

* Text

Graph Type:

* Static 3D Scene Graph

LLM Roles:

* Parsing
* Planning

Key Contributions:

* Graph-language alignment for 3D scene generation

---

## IntegraPSG (2025)

Input:

* Image

Graph Type:

* Static 2D Scene Graph

Key Contributions:

* Panoptic scene graph generation

---

## SGFormer (2024)

Input:

* Point Cloud

Graph Type:

* Static 3D Scene Graph

Key Contributions:

* Transformer-based scene graph generation

---

## ELEGANT (2023)

Input:

* Image

Graph Type:

* Static 2D Scene Graph

LLM Roles:

* Reasoning
* Parsing
* Verification

Key Contributions:

* Explainable scene graph generation

---

# Editing

Modify existing scenes or scene graphs using natural language instructions.

## SGEdit (2024)

Input:

* Image

Graph Type:

* Static 2D

Capabilities:

* Scene modification
* Object replacement
* Layout editing

Key Idea:

Uses LLMs as both parser and planner.

---

## EditRoom (2025)

Input:

* 3D Scene + Text

Graph Type:

* Static 3D

Capabilities:

* Rotate
* Translate
* Scale
* Replace
* Add
* Remove

Key Idea:

Uses graph diffusion models for scene editing.

---

## HRSGL (2024)

Input:

* 3D Scene

Graph Type:

* Static 3D

Capabilities:

* Scene optimization
* Structure-aware editing

---

## ScanEdit (2025)

Input:

* 3D Scene + Text

Graph Type:

* Static 3D

Capabilities:

* Text-driven scene editing

---

## SAKR-Edit (2025)

Input:

* Image + Text

Graph Type:

* Static 2D

Capabilities:

* Knowledge-guided image editing

---

# Retrieval

Scene graphs serve as structured indexes for retrieval tasks.

---

## VTGT (2025)

Visual Triplet-based Graph Transformation

Input:

* Image

Graph Type:

* Static 2D

Key Contributions:

* Triplet graph construction
* Graph attention retrieval
* Semantic image retrieval

---

## 3DGraphLLM (2025)

Input:

* 3D Scene

Graph Type:

* Static 3D

Key Contributions:

* Point-cloud reasoning
* Object retrieval from natural language queries
* Spatial relation encoding

---

# Navigation

Scene graphs guide embodied agents through environments.

---

## TioMS (2024)

Time is in my Sight

Input:

* Video

Graph Type:

* Dynamic 3D

LLM Roles:

* Parsing
* Planning

Key Contributions:

* Robot navigation
* Dynamic scene graph updates
* Semantic map generation

---

## OSGP (2024)

Online Scene Graph Planner

Input:

* Scene Graph

Graph Type:

* Static 3D

Key Contributions:

* Scene-graph-based planning

---

## SG-Nav (2024)

Input:

* Video

Graph Type:

* Dynamic 3D

LLM Roles:

* Reasoning
* Planning

Key Contributions:

* Online scene graph construction
* Frontier-based exploration
* Zero-shot object-goal navigation

---

# Comprehensive Comparison

| Method     | Year | Objective  | Graph Type | LLM Roles                                  |
| ---------- | ---- | ---------- | ---------- | ------------------------------------------ |
| SceneLLM   | 2025 | Generation | Dynamic-2D | Reasoning, Parsing                         |
| SceneCraft | 2024 | Generation | Static-3D  | Reasoning, Parsing, Planning, Verification |
| LLM4SGG    | 2024 | Generation | Static-2D  | Reasoning, Parsing                         |
| GraLa3D    | 2024 | Generation | Static-3D  | Parsing, Planning                          |
| SGEdit     | 2024 | Editing    | Static-2D  | Reasoning, Parsing, Planning               |
| EditRoom   | 2025 | Editing    | Static-3D  | Parsing, Planning                          |
| VTGT       | 2025 | Retrieval  | Static-2D  | Reasoning                                  |
| 3DGraphLLM | 2025 | Retrieval  | Static-3D  | Reasoning                                  |
| TioMS      | 2024 | Navigation | Dynamic-3D | Parsing, Planning                          |
| SG-Nav     | 2024 | Navigation | Dynamic-3D | Reasoning, Planning                        |

---

# Open Challenges

## Scalability

Large scenes produce extremely large graph structures.

Challenges:

* Memory consumption
* Real-time inference
* Dynamic updates

---

## Hallucination in Multimodal Reasoning

LLMs may infer:

* Incorrect relationships
* Non-existent objects
* Invalid spatial constraints

---

## Long-Horizon Navigation

Embodied agents require:

* Persistent memory
* Temporal reasoning
* Multi-step planning

---

## 3D Spatial Understanding

Many LLMs still struggle with:

* Precise geometry
* Depth reasoning
* Physical constraints

---

## Unified Multimodal Graph Foundation Models

Future systems are expected to jointly model:

* Language
* Images
* Videos
* 3D environments
* Scene graphs

within a single foundation architecture.

---

# Correspondence to Survey Taxonomy

This repository page corresponds to:

* Section 7.1 Graph Type
* Section 7.2 LLM Roles
* Section 7.3 Generation
* Section 7.3 Editing
* Section 7.3 Retrieval
* Section 7.3 Navigation

and represents the Scene Graph + LLM branch of the overall Graph–LLM integration taxonomy.
