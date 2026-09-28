---
title: "Tasks over Application Manuals: Revealing Gaps in Long-Horizon Procedural Reasoning for Language Models"
year: 2026
type: publication
venue: "arXiv preprint"
org_unit: "Manulife AI"
domains: ["operational-tasks"]
authors: "Utkarsh Soni, Syed Shariyar Murtaza, Yifan Nie, Sachin Chandrasekhar, Eugene Wen"
external_url: https://arxiv.org/abs/2609.13005
pdf_url: https://arxiv.org/pdf/2609.13005
summary: "This paper introduces Tasks over Application Manuals (TAM), a benchmark of real-world ICD-10-CM coding and U.S. federal sentencing tasks that shows current LLMs struggle to reliably follow long, rule-based procedural manuals."
---

This paper studies long-horizon procedural reasoning, where a model must follow an authoritative manual spanning tens of thousands of rules across many interdependent steps to produce an exact answer.

**Problem:** Existing multi-hop reasoning benchmarks are short-horizon and do not test whether models can reliably execute long procedures documented in large, rule-based manuals used in real-world workflows.

**Approach:** The paper curates human-validated tasks from two domains — ICD-10-CM clinical coding and U.S. federal sentencing guideline computation — and evaluates general-purpose prompting strategies, including retrieval-augmented generation, ReAct-style prompting, and an agent-harness baseline on GPT-5.

**Results:** Exact-match performance remains low across all approaches, at 1% on ICD-10-CM coding and 15.5% on sentencing tasks, indicating that current benchmarks overestimate LLM reasoning ability on long, rule-based procedures. The TAM data and code are publicly released.
