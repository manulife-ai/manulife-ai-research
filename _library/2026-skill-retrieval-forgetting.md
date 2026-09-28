---
title: "When Synthetic Data Hurts: On Catastrophic Forgetting in Skill Retrieval for LLM Agents"
year: 2026
type: publication
venue: "EMNLP 2026 (Industry Track)"
org_unit: "Manulife AI"
domains: ["virtual-assistants"]
authors: "Syed Shariyar Murtaza, Yifan Nie, Utkarsh Soni, Eugene Wen, Arvid Frydenlund"
external_url: https://arxiv.org/abs/2609.10750v1
pdf_url: https://arxiv.org/pdf/2609.10750v1
summary: "This paper studies a production skill router over 34,396 skills and shows that fine-tuning on synthetic data improves in-distribution retrieval but causes catastrophic forgetting on real and out-of-distribution skills, proposing continual-learning fixes."
---

This paper examines skill retrieval for LLM agents that select external skills from large repositories at runtime, a critical bottleneck as agent toolsets scale.

**Problem:** Fine-tuning skill retrievers on synthetic data improves in-distribution matching but causes catastrophic forgetting on real-world and out-of-distribution (OOD) skills, limiting reliability in production.

**Approach:** The paper presents a large-scale study of skill retrieval over a production router covering 34,396 skills, evaluating forgetting-mitigation techniques adapted from continual learning: embedding-anchor regularization, Learning without Forgetting (LwF), Elastic Weight Consolidation (EWC), and L2-initialization.

**Results:** These mitigation techniques retain performance on OOD skill retrieval while also improving synthetic in-distribution retrieval by 13.98% for a 0.6B-parameter Qwen retriever and reranker, offering a practical benchmark and fine-tuning recipe for scarce, multi-positive supervision settings.
