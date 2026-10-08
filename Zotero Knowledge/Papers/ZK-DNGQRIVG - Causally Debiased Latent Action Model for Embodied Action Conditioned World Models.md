---
type: "literature-note"
title: "Causally Debiased Latent Action Model for Embodied Action Conditioned World Models"
aliases: ["Causally Debiased Latent Action Model for Embodied Action Conditioned World Models"]
zotero_keys: ["DNGQRIVG"]
year: 2026
authors: ["Yufan Wei", "Kun Zhou", "Lingjun Mao", "Zijun Zhang", "Ziming Xu", "Ziqiao Xi", "Shuang Liang", "Ruobing Han", "Yuchen Yan", "Xinyue Wang", "Fan Feng", "Biwei Huang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2607.09185"
url: "http://arxiv.org/abs/2607.09185"
collections: ["06 Alignment & Reliability/Physics Grounding & Rollout Verification"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Robotics"]
tags: ["zotero", "literature", "concept/动作接口与逆动力学", "concept-primary/动作接口与逆动力学"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Causally Debiased Latent Action Model for Embodied Action Conditioned World Models

[Zotero 条目 DNGQRIVG](zotero://select/library/items/DNGQRIVG)

[DOI 原文](https://doi.org/10.48550/arxiv.2607.09185)

[来源网页](http://arxiv.org/abs/2607.09185)

## 主题与知识联系

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Physics Grounding & Rollout Verification/索引|06 Alignment & Reliability/Physics Grounding & Rollout Verification]]

概念地图：[[Zotero Knowledge/Concepts/动作接口与逆动力学|动作接口与逆动力学]]

补充阅读入口：[[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

## 原始摘要

Action-conditioned world models (ACWMs) aim to simulate future observations conditioned on embodied actions, offering a promising foundation for robot planning, policy evaluation, and data augmentation. However, learning controllable ACWMs requires large-scale action-labeled data, which remains costly to collect in the real world. Latent action models (LAMs) mitigate this bottleneck by inferring latent actions from unlabeled videos, but existing LAMs are typically trained with reconstruction-only objectives and therefore entangle action-relevant dynamics with action-irrelevant visual factors such as backgrounds and untouched objects. In this work, we identify this action-irrelevant bias as a key obstacle to controllable ACWMs and introduce evaluation metrics to measure latent-action bias, action following, and robustness. We propose CD-LAM, a causally debiased framework for LAM-based ACWMs. CD-LAM introduces three efficient fine-tuning objectives: embodiment-centric reconstruction, action-centric contrastive learning, and latent space calibration, which together encourage embodiment-focused, action-aware, and calibrated non-collapsed latent action representations. Experiments on 2B and 14B ACWM backbones show that CD-LAM substantially improves latent-action controllability, downstream robot-action following, visual fidelity, and adaptation efficiency, requiring only 6k fine-tuning steps and more than 12$\times$ fewer robot-action adaptation updates than the baseline.

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/VLXRX3WK)

[批注 TFAPN9WL · 第 1 页](zotero://open-pdf/library/items/VLXRX3WK?annotation=TFAPN9WL&page=1)

> embodiment-centric reconstruction, action-centric contrastive learning, and latent space calibration

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/I8Q8YY9C)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
