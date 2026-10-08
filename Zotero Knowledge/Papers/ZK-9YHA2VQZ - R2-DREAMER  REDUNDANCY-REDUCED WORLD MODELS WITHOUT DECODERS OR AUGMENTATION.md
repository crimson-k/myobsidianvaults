---
type: "literature-note"
title: "R2-DREAMER: REDUNDANCY-REDUCED WORLD MODELS WITHOUT DECODERS OR AUGMENTATION"
aliases: ["R2-DREAMER: REDUNDANCY-REDUCED WORLD MODELS WITHOUT DECODERS OR AUGMENTATION"]
zotero_keys: ["9YHA2VQZ"]
year: 2026
authors: ["Naoki Morihira", "Amal Nahar", "Kartik Bharadwaj", "Yasuhiro Kato", "Akinobu Hayashi", "Tatsuya Harada"]
venue: ""
venue_field: null
doi: ""
url: ""
collections: ["05 Robot Learning/Model-Based RL & Imagination"]
source_tags: []
tags: ["zotero", "literature", "highlight", "concept/想象中的规划与强化学习", "concept-primary/想象中的规划与强化学习"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# R2-DREAMER: REDUNDANCY-REDUCED WORLD MODELS WITHOUT DECODERS OR AUGMENTATION

[Zotero 条目 9YHA2VQZ](zotero://select/library/items/9YHA2VQZ)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Model-Based RL & Imagination/索引|05 Robot Learning/Model-Based RL & Imagination]]

概念地图：[[Zotero Knowledge/Concepts/想象中的规划与强化学习|想象中的规划与强化学习]]

补充阅读入口：[[Zotero Knowledge/Topics/04 World Models/Latent & Object-Centric Dynamics/索引|04 World Models/Latent & Object-Centric Dynamics]]

## 原始摘要

A central challenge in image-based Model-Based Reinforcement Learning (MBRL) is to learn representations that distill essential information from irrelevant visual details. While promising, reconstruction-based methods often waste capacity on large task-irrelevant regions. Decoder-free methods instead learn robust representations by leveraging Data Augmentation (DA), but reliance on such external regularizers limits versatility. We propose R2-Dreamer, a decoder-free MBRL framework with a self-supervised objective that serves as an internal regularizer, preventing representation collapse without resorting to DA. The core of our method is a redundancy-reduction objective inspired by Barlow Twins, which can be easily integrated into existing frameworks. On DeepMind Control Suite and Meta-World, R2-Dreamer is competitive with strong baselines such as DreamerV3 and TD-MPC2 while training 1.59× faster than DreamerV3, and yields substantial gains on DMC-Subtle with tiny task-relevant objects. These results suggest that an effective internal regularizer can enable versatile, high-performance decoder-free MBRL. Code is available at https://github.com/NM512/r2dreamer.

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/SXI8WTJM)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
