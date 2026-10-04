# Agentic AI Workshop 2026 — Hands-on Labs

**Beyond Automation: Build AI Agents That Think, Decide, and Act**
Lab notebooks from the two-day industry masterclass held at the University of Essex, Colchester, on 1–2 October 2026.

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Runs on](https://img.shields.io/badge/Runs%20on-Google%20Colab%20(T4%20GPU)-orange)
![Frameworks](https://img.shields.io/badge/Frameworks-LangChain%20%7C%20LangGraph-purple)

> © 2026 **Sensiwise AI Ltd**. All rights reserved except as granted under the licence below.
> These materials are the intellectual property of Sensiwise AI Ltd. **Any use, in any form or for any purpose, must acknowledge Sensiwise AI** (see [Attribution](#attribution)).

---

## Overview

Four progressive labs that take you from retrieval-augmented generation to a supervised team of cooperating agents. Every lab runs end to end in Google Colab on a free T4 GPU, using a small open model (`Qwen/Qwen3.5-4B`) so that no paid API keys are required. Each pipeline step prints its own banner, so you can see exactly where the model makes a decision and where code takes over.

| # | Lab | Day | What you build | Open |
|---|---|---|---|---|
| 1 | **RAG Pipeline** | 1 | Retrieval-augmented assistant over a real company handbook: cleaning, four chunking strategies measured side by side, metadata filters, a similarity gate and cited answers | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sensiwise-ai/agentic-ai-workshop2026-labs/blob/main/Lab1_RAG_Pipeline_Day1.ipynb) |
| 2 | **SQL Data Analyst** | 1 | Plain English → SQL → answer: table selection, schema injection, `sqlglot` validation, self-repair on error, plain-English explanation; compared with LangChain's SQL chain | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sensiwise-ai/agentic-ai-workshop2026-labs/blob/main/Lab2_SQL_Data_Analyst_Day1.ipynb) |
| 3 | **Research Agent** | 2 | An agent that plans searches over live arXiv, selects and reads papers, judges its own coverage, loops, and writes a citation-checked briefing; rebuilt as a LangGraph cycle | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sensiwise-ai/agentic-ai-workshop2026-labs/blob/main/Lab3_Research_Agent_Day2.ipynb) |
| 4 | **Agent Team** | 2 | Triage, policy and account specialists, a writer, an independent reviewer and a supervisor with a budget and a human hand-off; expressed as a LangGraph `StateGraph` | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sensiwise-ai/agentic-ai-workshop2026-labs/blob/main/Lab4_Agent_Team_Day2.ipynb) |

Each lab ends with a **"Your turn"** section where you point the same pipeline at your own documents or spreadsheets, plus exercises for going further.

## Learning outcomes

By the end of the four labs you will be able to:

- Explain how agentic systems differ from fixed pipelines and rule-based automation
- Build and **measure** a RAG pipeline, including chunking choices and refusal thresholds
- Give a model safe, validated access to a relational database
- Build an agent that decides what to do next, bounded by budgets and code-level checks
- Orchestrate multiple specialised agents and represent their control flow as a graph

## Getting started

**Requirements**

- A Google account (for Colab)
- Runtime set to **T4 GPU**: *Runtime → Change runtime type → T4 GPU*
- Basic Python; no local installation needed

**Steps**

1. Click an **Open in Colab** badge above.
2. Set the runtime to T4 GPU.
3. Run the cells top to bottom. The first cell installs dependencies and downloads the model (~9 GB, a few minutes on first run).

To run locally instead, you need Python 3.10+, a CUDA GPU with at least 12 GB of memory, and the packages listed in each notebook's first cell.

## Repository structure

```
agentic-ai-workshop2026-labs/
├── Lab1_RAG_Pipeline_Day1.ipynb
├── Lab2_SQL_Data_Analyst_Day1.ipynb
├── Lab3_Research_Agent_Day2.ipynb
├── Lab4_Agent_Team_Day2.ipynb
├── LICENSE
└── README.md
```

## Technology

| Purpose | Library / model |
|---|---|
| Language model | `Qwen/Qwen3.5-4B` via Hugging Face `transformers` (fallback `Qwen/Qwen3-4B`) |
| Embeddings | `sentence-transformers` — `all-MiniLM-L6-v2` |
| Vector store | ChromaDB (in-memory) |
| SQL | SQLite, `sqlglot`, pandas, LangChain `SQLDatabase` |
| Agent orchestration | LangGraph |
| Documents | `pypdf`, `arxiv` |

---

## Licence

This repository — notebooks, code, text, diagrams and exercises — is licensed under the
**[Creative Commons Attribution-NonCommercial 4.0 International Licence (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/)**. See [`LICENSE`](LICENSE).

**You may**

- Use the materials for personal learning, teaching, academic research and non-commercial training
- Share, copy and redistribute them in any medium or format
- Adapt, remix and build upon them

**On these conditions**

- **Attribution** — you must credit Sensiwise AI Ltd, link to the licence, and indicate if changes were made. This applies to every use, including adapted and partial versions.
- **NonCommercial** — you may not use the materials for commercial purposes, including paid courses, paid training, consultancy deliverables or commercial products, without prior written permission.

**Commercial use.** To use these materials commercially, or under different terms, contact Sensiwise AI at **hello@sensiwise.ai** for a commercial licence.

The licence covers only material authored by Sensiwise AI Ltd. Third-party content is listed below and remains under its own terms.

## Attribution

Any use of these materials — in teaching, publications, presentations, derived notebooks or software — must acknowledge Sensiwise AI. Please use:

> *Agentic AI Workshop 2026 Labs* © 2026 Sensiwise AI Ltd (https://sensiwise.ai), licensed under CC BY-NC 4.0.

When adapting the materials, add: *"Adapted from the original by Sensiwise AI Ltd; changes were made."*

### Citing this work

```bibtex
@misc{sensiwise2026agenticlabs,
  author       = {{Sensiwise AI Ltd}},
  title        = {Agentic AI Workshop 2026: Hands-on Labs},
  year         = {2026},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/sensiwise-ai/agentic-ai-workshop2026-labs}},
  note         = {Licensed under CC BY-NC 4.0}
}
```

## Third-party content

The notebooks download or call the following at run time. None of it is redistributed in this repository, and each item stays under its owner's licence.

| Resource | Used in | Terms |
|---|---|---|
| GitLab Handbook (fixed commit) | Lab 1 | © GitLab Inc., [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) |
| Chinook sample database | Lab 2 | See [lerocha/chinook-database](https://github.com/lerocha/chinook-database) |
| arXiv papers via the arXiv API | Lab 3 | Each paper under its own licence; see [arXiv](https://arxiv.org) |
| `jamescalam/ai-arxiv2` dataset (fallback) | Lab 3 | See its [Hugging Face page](https://huggingface.co/datasets/jamescalam/ai-arxiv2) |
| Qwen models | All labs | See the model card on Hugging Face |
| `all-MiniLM-L6-v2` | Labs 1, 3, 4 | See the model card on Hugging Face |
| Open-source Python libraries | All labs | Each under its own licence |

The Brightwave Energy customers, messages and policies in Lab 4 are fictional and were written for this workshop.

## Disclaimer

These materials are provided for education, **as is**, without warranty of any kind. The example agents are teaching implementations and are not intended for production use without independent review, testing and appropriate safeguards. Model outputs can be incorrect.

---

## About Sensiwise AI

**Sensiwise AI Ltd** builds and teaches practical, trustworthy AI systems for industry and the public sector.
ISO 27001 · ISO 9001 certified.

- Web: [sensiwise.ai](https://sensiwise.ai)
- Email: [hello@sensiwise.ai](mailto:hello@sensiwise.ai)
- Registered in England and Wales, Company No. 15173736
- 85 Great Portland Street, First Floor, London, W1W 7LT

These labs were developed for *Beyond Automation: Build AI Agents That Think, Decide, and Act*, a two-day industry masterclass held at the University of Essex, 1–2 October 2026.

© 2026 Sensiwise AI Ltd.
