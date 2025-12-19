# LLM Foundations and Systems (Exam Prep Repo)

This repository is a structured, reproducible study project covering:

- LLM Foundations & Prompting
- Data Preparation & Fine-Tuning
- Optimization & Acceleration
- Deployment & Monitoring
- Evaluation & Responsible AI

It is designed to work on **macOS Catalina (10.15)** with **Python 3.10.x** and **uv**.

---

## Why this repo exists

The exam topics are broad. Instead of reading notes, this repo creates **evidence** of understanding:

- Clear notes (Markdown) for revision
- Notebooks for hands-on experiments (prompting, tokenization, evaluation)
- Systems thinking docs (deployment, monitoring, performance)
- Reproducible setup using `uv` + lockfile

---

## Repository Structure

llm-foundations-and-systems/
├── 00_env/
│ ├── README.md
│ └── setup.md
├── 01_llm_foundations_prompting/
│ ├── README.md
│ ├── prompting_patterns.ipynb
│ └── prompt_evaluation.md
├── 02_data_and_finetuning/
│ ├── README.md
│ ├── dataset_curation.ipynb
│ ├── tokenization_analysis.ipynb
│ └── finetuning_notes.md
├── 03_optimization_and_acceleration/
│ ├── README.md
│ ├── inference_optimizations.md
│ └── training_optimizations.md
├── 04_deployment_and_monitoring/
│ ├── README.md
│ ├── inference_pipeline.md
│ └── monitoring_and_drift.md
├── 05_evaluation_and_responsible_ai/
│ ├── README.md
│ ├── evaluation_framework.ipynb
│ └── responsible_ai.md
├── pyproject.toml
├── uv.lock
└── README.md



---

## Requirements

- macOS Catalina (10.15) supported
- Python: **3.10.x**
- uv installed and available in PATH

Why specific pins matter on Catalina:
- `numpy<2` + `pyarrow<12` avoids binary incompatibilities on older macOS.
- `datasets<2.19` avoids forcing newer `pyarrow` versions.

---

## Quickstart (recommended)

From the repo root:

```bash
uv venv --python 3.10
source .venv/bin/activate
uv pip install -e ".[notebooks,llm,data,dev]"

