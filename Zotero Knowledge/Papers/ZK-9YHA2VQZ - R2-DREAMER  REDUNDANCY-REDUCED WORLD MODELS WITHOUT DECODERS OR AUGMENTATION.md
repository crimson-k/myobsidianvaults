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

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-67T4CPZ5 - Barlow Twins  Self-Supervised Learning via Redundancy Reduction|Barlow Twins: Self-Supervised Learning via Redundancy Reduction]] — 强关联；本篇摘要提到模型 Barlow Twins（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-XRENB5FA - Mastering Diverse Domains through World Models|Mastering Diverse Domains through World Models]] — 强关联；本篇摘要提到模型 DreamerV3（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-STEFAJQY - Dream to Control  Learning Behaviors by Latent Imagination|Dream to Control: Learning Behaviors by Latent Imagination]] — 强关联；本篇摘要提到模型 Dreamer（仅确认名称提及）。

<!-- content-relations:end -->
