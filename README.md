# multiagent-governance-eval

This repository contains the complete experimental notebook for the paper submitted to the **5th International Conference on AI Research (ICAIR)**:

**Title**: *"Where Should Control Reside in Multi-Agent Language-Model Systems?"*

## Overview

This work explores how different governance strategies—**centralized**, **distributed**, and **hybrid**—affect the reliability, accuracy, and transparency of multi-agent systems powered by large language models (LLMs).

The core logic, experiments, and evaluation are all contained in one Jupyter notebook:

> `agents/goverance_mechanisms_multi_agent_system.ipynb`

The notebook includes:

* A modular agentic workflow (Classifier, RAG, and Summarizer agents)
* Control architectures for centralized, distributed, and hybrid governance
* Evaluation setup using DeepEval[(https://deepeval.com/docs/metrics-llm-evals)] and custom `GEval` metrics
* Comparison of performance using the SQuAD dataset (subset of 50 questions)

## Getting Started

1. **Install dependencies**
   pip install -r requirements.txt


2. **Launch the notebook**
   Open the notebook using Jupyter:

   jupyter notebook governance_mechanisms_multi_agent_system.ipynb

## Evaluation Setup

We use:

* **DeepEval** for automated evaluation of answer relevancy and task success.
* **GEval** for custom metrics: transparency and helpfulness.

Agents are configured to log reasoning and tool use. Guardrails (quality checks) are triggered in the distributed mode using retry logic and confidence thresholds. Details on how these checks are applied are provided in-code and also described in our paper.

Due to space limitations in the publication, we’ve included full implementation details, evaluation settings, and outputs in this notebook.

## Paper & License

The research is under review at ICAIR 2025. Final citation and DOI will be updated here after acceptance.

This code is open-sourced under the MIT License.

