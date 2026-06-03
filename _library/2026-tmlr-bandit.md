---
title: "A Practical Algorithm for Feature-Rich, Non-Stationary Bandit Problems"
year: 2026
type: publication
venue: "Transactions on Machine Learning Research"
org_unit: "University of Waterloo Partnership"
domains: ["advice"]
authors: "Wei Min Loh, Sajib Kumer Sinha, Ankur Agarwal, Pascal Poupart"
external_url: https://openreview.net/forum?id=tRbwfej9uY
code_url: https://github.com/wmloh/c3
pdf_url: https://openreview.net/pdf?id=tRbwfej9uY
summary: "This paper introduces conditionally coupled contextual (C3) Thompson Sampling, a method for non‑linear, time‑varying contextual bandits that improves regret and click‑through performance over existing algorithms."
---

This paper introduces conditionally coupled contextual (C3) Thompson Sampling, a method that handles non‑linear, time‑varying contextual bandits with correlated rewards by combining embedding‑based kernel estimation with online Thompson sampling, achieving substantially lower regret and higher click‑through rates than existing approaches.

**Problem:** This paper devises a more realistic problem that combines contextual bandits with dense arm features, non-linear reward functions, and a generalization of correlated bandits where reward distributions change over time but the degree of correlation maintains. 

**Approach:** This paper introduces conditionally coupled contextual (C3) Thompson sampling for Bernoulli bandits. It combines an improved Nadaraya-Watson estimator on an embedding space with Thompson sampling that allows online learning without retraining. 

**Results:** Empirical results show that C3 outperforms the next best algorithm by 5.7% lower average cumulative regret on four OpenML tabular datasets as well as demonstrating a 12.4% click lift on Microsoft News Dataset (MIND) compared to other algorithms.

