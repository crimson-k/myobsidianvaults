---
type: "literature-note"
title: "MIND-V: Hierarchical World Model for Long-Horizon Robotic Manipulation with RL-based Physical Alignment"
aliases: ["MIND-V: Hierarchical World Model for Long-Horizon Robotic Manipulation with RL-based Physical Alignment"]
zotero_keys: ["6AVL3P5T"]
year: 2026
authors: ["Ruicheng Zhang", "Mingyang Zhang", "Jun Zhou", "Xiaofan Liu", "Zunnan Xu", "Zhizhou Zhong", "Puxin Yan", "Haocheng Luo", "Xiu Li"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2512.06628"
url: "http://arxiv.org/abs/2512.06628"
collections: ["05 Robot Learning/Simulation for Training & Evaluation"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Robotics"]
tags: ["zotero", "literature", "highlight"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# MIND-V: Hierarchical World Model for Long-Horizon Robotic Manipulation with RL-based Physical Alignment

[Zotero 条目 6AVL3P5T](zotero://select/library/items/6AVL3P5T)

[DOI 原文](https://doi.org/10.48550/arxiv.2512.06628)

[来源网页](http://arxiv.org/abs/2512.06628)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Simulation for Training & Evaluation/索引|05 Robot Learning/Simulation for Training & Evaluation]]

补充阅读入口：[[Zotero Knowledge/Topics/06 Alignment & Reliability/Physics Grounding & Rollout Verification/索引|06 Alignment & Reliability/Physics Grounding & Rollout Verification]]

## 原始摘要

Scalable embodied intelligence is constrained by the scarcity of diverse, long-horizon robotic manipulation data. Existing video world models in this domain are limited to synthesizing short clips of simple actions and often rely on manually defined trajectories. To this end, we introduce MIND-V, a cognitive hierarchical world model designed to synthesize physically plausible and logically coherent videos of long-horizon robotic manipulation. Inspired by cognitive science, MIND-V bridges high-level reasoning with pixel-level synthesis through three core components: a Semantic Reasoning Hub (SRH) that leverages a pre-trained vision-language model for task planning; a Behavioral Semantic Bridge (BSB) that translates abstract instructions into domain-invariant representations; and a Motor Video Generator (MVG) for conditional video rendering. MIND-V employs Staged Visual Future Rollouts, a test-time optimization strategy to enhance long-horizon robustness. To enforce adherence to physical laws, we introduce a GRPO reinforcement learning post-training phase guided by a novel Physical Foresight Coherence (PFC) reward. PFC leverages the V-JEPA2 world model as a physics referee to penalize implausible dynamics in the latent feature space. Experiments confirm MIND-V's SOTA performance in long-horizon simulation and its significant value for policy learning, introducing a scalable and fully autonomous framework for embodied data synthesis.

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/3L86D9J5)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/HXS6QZKI)

[批注 W9DE7TCP · 第 1 页](zotero://open-pdf/library/items/HXS6QZKI?annotation=W9DE7TCP&page=1)

> MIND-V  MIND-V bridges high-level reasoning with pixel-level synthesis via three components: a Semantic Reasoning Hub (SRH) that leverages a pretrained vision-language model for task planning; a Behavioral Semantic Bridge (BSB) that converts abstract instructions into domain-invariant representations; and a Motor Video Generator (MVG) for conditional video rendering.

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
