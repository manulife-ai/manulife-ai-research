---
title: "Control-Data Flow Separation: Stable Prompt Optimization in Multi-Agent LLMs"
year: 2026
type: publication
venue: "EMNLP 2026 Findings"
org_unit: "Manulife AI"
domains: ["virtual-assistants", "underwriting"]
authors: "Wentao Zhang, Syed Shariyar Murtaza, Junaid Ahmad Bhatti, Utkarsh Soni, Yifan Nie, Eugene Wen, Yuntian Deng"
external_url: https://arxiv.org/abs/2609.00621
pdf_url: https://arxiv.org/pdf/2609.00621
summary: "This paper proposes control-data flow separation, representing execution-critical protocol as typed program objects distinct from the optimizable natural-language content in multi-agent LLM prompts, achieving 100% protocol validity while improving task performance."
---

This paper addresses a failure mode in multi-agent LLM prompt optimization where prompts serve two entangled roles — generating task content and specifying execution-critical protocols such as message routing, output formatting, and termination — so that edits meant to improve content can silently corrupt the protocol and break the agent pipeline.

**Problem:** Execution-critical control information and task-relevant content are optimized together in the same prompt, so protocol drift caused by content edits can cause entire multi-agent pipelines to fail.

**Approach:** The paper proposes control-data flow separation: execution-critical control is represented as typed, validated program objects, while task-relevant language remains the optimizable data flow for agent communication, preventing optimizers from drifting the routing or formatting interface.

**Results:** Across synthetic reasoning, collaborative review generation, and insurance rating workflows, the framework achieves 100% eventual protocol validity while consistently improving task performance over baseline prompt optimization.
