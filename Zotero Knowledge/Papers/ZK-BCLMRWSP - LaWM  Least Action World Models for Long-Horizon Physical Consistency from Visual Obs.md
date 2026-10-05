---
type: "literature-note"
title: "LaWM: Least Action World Models for Long-Horizon Physical Consistency from Visual Observations"
aliases: ["LaWM: Least Action World Models for Long-Horizon Physical Consistency from Visual Observations"]
zotero_keys: ["BCLMRWSP"]
year: 2026
authors: ["Qixin Xiao", "Maani Ghaffari"]
venue: "arXiv.org"
venue_field: "websiteTitle"
doi: ""
url: "https://arxiv.org/abs/2605.08279v1"
collections: ["04 World Models/Latent & Object-Centric Dynamics"]
source_tags: []
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# LaWM: Least Action World Models for Long-Horizon Physical Consistency from Visual Observations

[Zotero 条目 BCLMRWSP](zotero://select/library/items/BCLMRWSP)

[来源网页](https://arxiv.org/abs/2605.08279v1)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Latent & Object-Centric Dynamics/索引|04 World Models/Latent & Object-Centric Dynamics]]

## 原始摘要

Learning predictive world models from visual observations is a core problem in embodied AI, with applications to model-based reinforcement learning and robotic planning. Existing latent world models typically generate future states with unconstrained neural transition functions, while modern video generation systems often prioritize perceptual plausibility or introduce physical structure through auxiliary losses, external guidance, or separate dynamics modules. As a result, long-horizon rollouts can remain weakly grounded in the physical principles that govern real dynamics, leading to compounding error, energy drift, and physically inconsistent futures. We propose Least Action World Models (LaWM), a latent world-modeling framework that operationalizes the Principle of Least Action in learned visual latent space: future rollouts are governed by a learned Lagrangian action functional rather than produced only by an unconstrained transition predictor. Our main technical realization is a latent variational integrator: LaWM encodes observations into learned generalized coordinates, learns a latent discrete Lagrangian over consecutive latent states, constructs a discrete action functional, and advances prediction by solving the corresponding discrete integration condition. Thus, physical structure is not merely used to score, regularize, or constrain a completed trajectory; it defines the latent transition rule itself. Because the transition is induced by a discrete variational principle, LaWM provides a structure-preserving bias for long-horizon visual prediction. Across physics-clean synthetic dynamics and embodied robot interaction benchmarks, LaWM improves physical invariance, background consistency, motion smoothness, and appearance and geometric prediction metrics over video-generation and world-model baselines.

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/T4DBKZJ4)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
