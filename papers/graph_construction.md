LLM-Assisted Graph Construction
This page accompanies our survey:
Integrating Graphs, Large Language Models, and Agents: Reasoning and Retrieval
Graph construction is one of the foundational paradigms for integrating Large Language Models (LLMs) and graph-based representations. Unlike traditional graph construction pipelines that rely on multiple specialized NLP components, recent LLM-based approaches can directly extract entities, relationships, schemas, and graph structures from unstructured text.
________________________________________
Taxonomy
LLM-Assisted Graph Construction
•	Knowledge Graph Extraction from Text
•	Ontology Engineering and Schema Construction
•	Iterative and Zero-Shot Graph Construction
________________________________________
Knowledge Graph Extraction from Text
These methods focus on transforming unstructured documents into structured graph representations by extracting entities, relationships, and attributes.
Method	Year	Main Task	Paper	Code
Text2KG	2024	Knowledge graph extraction from text	https://dl.acm.org/doi/abs/10.1145/3701716.3715309	https://github.com/AI4WA/Docs2KG
Prompt-based KG Construction	2024	Triple extraction using LLM prompting	https://ieeexplore.ieee.org/abstract/document/10387715	https://github.com/zjukg/KG-LLM-Papers/blob/main/README.md
LLM-driven Graph Generation	2024	End-to-end graph construction	https://arxiv.org/abs/2403.14358	Not publicly available
Key Research Directions
•	Entity and relation extraction
•	Triple generation
•	Structured graph generation
•	Multi-document graph construction
•	Hallucination mitigation during extraction
________________________________________
Ontology Engineering and Schema Construction
Ontology engineering focuses on designing graph schemas, classes, entity types, and relationship structures. Recent work explores how LLMs can automate portions of ontology creation and refinement.
Method	Year	Main Task	Paper	Code
Ontology Construction with RAG	2024	Automated ontology generation	https://arxiv.org/abs/2403.08345	https://github.com/fusion-jena/automatic-KG-creation-with-LLM
Knowledge Graph Engineering with ChatGPT	2024	KG engineering assistance	https://link.springer.com/chapter/10.1007/978-3-658-43705-3_8	https://github.com/AKSW/AI-Tomorrow-2023-KG-ChatGPT-Experiments

Ontology Alignment using LLMs	2024	Semantic schema alignment	https://ceur-ws.org/Vol-4144/om2025-STpaper1.pdf	https://github.com/AdritaBarua/Complex-Ontology-Alignment-using-LLMs

Key Research Directions
•	Automated ontology creation
•	Schema refinement
•	Ontology alignment
•	Competency-question generation
•	Domain adaptation
________________________________________
Iterative and Zero-Shot Graph Construction
These methods reduce dependence on manually curated ontologies and labeled datasets by leveraging iterative prompting and self-refinement strategies.
Method	Year	Main Task	Paper	Code
Zero-Shot KG Construction	2024	Graph generation without annotations	https://arxiv.org/abs/2307.01128	Not publicly  available
GraphCorrect	2024	Graph-based hallucination correction	https://arxiv.org/abs/2407.10793	Not publicly  available
LLM-KG-Bench	2024	KG construction benchmarking	https://arxiv.org/abs/2504.07087	Not publicly  available
Key Research Directions
•	Zero-shot graph generation
•	Self-refinement
•	Graph validation
•	Hallucination detection
•	Graph quality assessment
________________________________________
Open Challenges
Despite significant progress, several challenges remain:
1.	Hallucinated entities and relationships.
2.	Maintaining schema consistency at scale.
3.	Cross-document entity resolution.
4.	Continuous graph updating.
5.	Graph quality evaluation.
6.	Domain-specific adaptation.
7.	Scalable graph construction for large corpora.
________________________________________
Related Survey Section
This repository page corresponds to:
Section 3 – LLM-Assisted Graph Construction
Subsections:
•	Knowledge Graph Extraction from Text
•	Ontology Engineering and Schema Construction
•	Iterative and Zero-Shot Graph Construction
________________________________________
Contributing
If you are aware of relevant graph construction papers, datasets, or open-source implementations that are missing from this list, please submit a pull request or open an issue.
________________________________________
Citation
If you find this repository useful, please cite:
Jelodar et al.
Integrating Graphs, Large Language Models, and Agents: Reasoning and Retrieval.
Information Fusion (under review).
