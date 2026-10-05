---
type: "literature-note"
title: "Learning Latent Dynamics for Planning from Pixels"
aliases: ["Learning Latent Dynamics for Planning from Pixels"]
zotero_keys: ["ILDZSE8T"]
year: 2019
authors: ["Danijar Hafner", "Timothy Lillicrap", "Ian Fischer", "Ruben Villegas", "David Ha", "Honglak Lee", "James Davidson"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.1811.04551"
url: "http://arxiv.org/abs/1811.04551"
collections: ["05 Robot Learning/Model-Based RL & Imagination"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Machine Learning", "Statistics - Machine Learning"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Learning Latent Dynamics for Planning from Pixels

[Zotero 条目 ILDZSE8T](zotero://select/library/items/ILDZSE8T)

[DOI 原文](https://doi.org/10.48550/arxiv.1811.04551)

[来源网页](http://arxiv.org/abs/1811.04551)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Model-Based RL & Imagination/索引|05 Robot Learning/Model-Based RL & Imagination]]

概念地图：[[Zotero Knowledge/Concepts/想象中的规划与强化学习|想象中的规划与强化学习]]

补充阅读入口：[[Zotero Knowledge/Topics/05 Robot Learning/Planning & Inverse Control/索引|05 Robot Learning/Planning & Inverse Control]]

## 原始摘要

Planning has been very successful for control tasks with known environment dynamics. To leverage planning in unknown environments, the agent needs to learn the dynamics from interactions with the world. However, learning dynamics models that are accurate enough for planning has been a long-standing challenge, especially in image-based domains. We propose the Deep Planning Network (PlaNet), a purely model-based agent that learns the environment dynamics from images and chooses actions through fast online planning in latent space. To achieve high performance, the dynamics model must accurately predict the rewards ahead for multiple time steps. We approach this using a latent dynamics model with both deterministic and stochastic transition components. Moreover, we propose a multi-step variational inference objective that we name latent overshooting. Using only pixel observations, our agent solves continuous control tasks with contact dynamics, partial observability, and sparse rewards, which exceed the difficulty of tasks that were previously solved by planning with learned models. PlaNet uses substantially fewer episodes and reaches final performance close to and sometimes higher than strong model-free algorithms.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### 笔记

[在 Zotero 查看](zotero://select/library/items/MGA2MSLQ)

[原笔记中的图片：请在 Zotero 查看]

## 附件与批注

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/YL6WP32A)

[批注 4ZRSU8SL · 第 3 页](zotero://open-pdf/library/items/YL6WP32A?annotation=4ZRSU8SL&page=3)

> Recurrent State Space Model

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/ASE7MN2A)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
