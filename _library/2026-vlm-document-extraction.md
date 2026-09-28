---
title: "Beyond Accuracy: Robustness, Cost, and Governance Trade-offs for Vision-Language Models in Templated Document Extraction"
year: 2026
type: publication
venue: "arXiv preprint"
org_unit: "Manulife AI"
domains: ["operational-tasks"]
authors: "Kushal Patel, Pushkal Shrivastava, Mackenzie Lees, Qirui Lu, Bhargobjyoti Saikia, Liying Li, Junlin Jiang"
external_url: https://arxiv.org/abs/2609.15706v2
pdf_url: https://arxiv.org/pdf/2609.15706v2
summary: "This paper benchmarks eleven commercial, reasoning, and open-source vision-language models on templated document field extraction and introduces a selection framework that maps task requirements to the most cost-effective, governance-compliant approach."
---

This paper evaluates vision-language models (VLMs) for extracting structured fields from templated business documents, moving beyond accuracy-only benchmarks to also measure robustness, cost, and governance trade-offs.

**Problem:** Most VLM evaluations report accuracy on clean benchmarks alone, giving practitioners little guidance on choosing a document-extraction approach that balances quality, latency, governance, and cost for a given task.

**Approach:** Eleven systems — three commercial models, two reasoning models, five open-source VLMs (pretrained and fine-tuned), and a non-LLM OCR-to-regex baseline — are scored on a 750-document held-out pool of synthetic checks, and results are synthesized into a practitioner-oriented selection framework.

**Results:** Fine-tuning on 3K samples lifts the best open-source VLMs above F1 0.98, surpassing every zero-shot commercial system on this task, while GPT-5 leads the zero-shot commercial pool and Claude Sonnet 4.5 collapses on date-field extraction; the paper illustrates cost-minimizing model selection on a hypothetical mid-volume document-extraction scenario.
