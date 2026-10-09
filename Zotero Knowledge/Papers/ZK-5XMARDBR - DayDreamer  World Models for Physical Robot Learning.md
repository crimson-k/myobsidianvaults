---
type: "literature-note"
title: "DayDreamer: World Models for Physical Robot Learning"
aliases: ["DayDreamer: World Models for Physical Robot Learning"]
zotero_keys: ["5XMARDBR"]
year: 2022
authors: ["Philipp Wu", "Alejandro Escontrela", "Danijar Hafner", "Ken Goldberg", "Pieter Abbeel"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2206.14176"
url: "http://arxiv.org/abs/2206.14176"
collections: ["05 Robot Learning/Model-Based RL & Imagination"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Machine Learning", "Computer Science - Robotics"]
tags: ["zotero", "literature", "concept/想象中的规划与强化学习", "concept-primary/想象中的规划与强化学习"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# DayDreamer: World Models for Physical Robot Learning

[Zotero 条目 5XMARDBR](zotero://select/library/items/5XMARDBR)

[DOI 原文](https://doi.org/10.48550/arxiv.2206.14176)

[来源网页](http://arxiv.org/abs/2206.14176)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Model-Based RL & Imagination/索引|05 Robot Learning/Model-Based RL & Imagination]]

概念地图：[[Zotero Knowledge/Concepts/想象中的规划与强化学习|想象中的规划与强化学习]]

## 原始摘要

To solve tasks in complex environments, robots need to learn from experience. Deep reinforcement learning is a common approach to robot learning but requires a large amount of trial and error to learn, limiting its deployment in the physical world. As a consequence, many advances in robot learning rely on simulators. On the other hand, learning inside of simulators fails to capture the complexity of the real world, is prone to simulator inaccuracies, and the resulting behaviors do not adapt to changes in the world. The Dreamer algorithm has recently shown great promise for learning from small amounts of interaction by planning within a learned world model, outperforming pure reinforcement learning in video games. Learning a world model to predict the outcomes of potential actions enables planning in imagination, reducing the amount of trial and error needed in the real environment. However, it is unknown whether Dreamer can facilitate faster learning on physical robots. In this paper, we apply Dreamer to 4 robots to learn online and directly in the real world, without simulators. Dreamer trains a quadruped robot to roll off its back, stand up, and walk from scratch and without resets in only 1 hour. We then push the robot and find that Dreamer adapts within 10 minutes to withstand perturbations or quickly roll over and stand back up. On two different robotic arms, Dreamer learns to pick and place multiple objects directly from camera images and sparse rewards, approaching human performance. On a wheeled robot, Dreamer learns to navigate to a goal position purely from camera images, automatically resolving ambiguity about the robot orientation. Using the same hyperparameters across all experiments, we find that Dreamer is capable of online learning in the real world, establishing a strong baseline. We release our infrastructure for future applications of world models to robot learning.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Website: https://danijar.com/daydreamer

[在 Zotero 查看](zotero://select/library/items/9MF29X42)

Comment: Website: https://danijar.com/daydreamer

## 附件与批注

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/KQWIDK82)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/IWSQBCNC)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-STEFAJQY - Dream to Control  Learning Behaviors by Latent Imagination|Dream to Control: Learning Behaviors by Latent Imagination]] — 强关联；本篇摘要提到模型 Dreamer（仅确认名称提及）。

<!-- content-relations:end -->
