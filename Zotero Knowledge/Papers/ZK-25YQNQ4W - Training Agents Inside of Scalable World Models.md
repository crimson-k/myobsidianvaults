---
type: "literature-note"
title: "Training Agents Inside of Scalable World Models"
aliases: ["Training Agents Inside of Scalable World Models"]
zotero_keys: ["25YQNQ4W"]
year: 2025
authors: ["Danijar Hafner", "Wilson Yan", "Timothy Lillicrap"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2509.24527"
url: "http://arxiv.org/abs/2509.24527"
collections: ["05 Robot Learning/Model-Based RL & Imagination"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Machine Learning", "Computer Science - Robotics", "Statistics - Machine Learning"]
tags: ["zotero", "literature", "concept/想象中的规划与强化学习", "concept-primary/想象中的规划与强化学习"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Training Agents Inside of Scalable World Models

[Zotero 条目 25YQNQ4W](zotero://select/library/items/25YQNQ4W)

[DOI 原文](https://doi.org/10.48550/arxiv.2509.24527)

[来源网页](http://arxiv.org/abs/2509.24527)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Model-Based RL & Imagination/索引|05 Robot Learning/Model-Based RL & Imagination]]

概念地图：[[Zotero Knowledge/Concepts/想象中的规划与强化学习|想象中的规划与强化学习]]

## 原始摘要

World models learn general knowledge from videos and simulate experience for training behaviors in imagination, offering a path towards intelligent agents. However, previous world models have been unable to accurately predict object interactions in complex environments. We introduce Dreamer 4, a scalable agent that learns to solve control tasks by reinforcement learning inside of a fast and accurate world model. In the complex video game Minecraft, the world model accurately predicts object interactions and game mechanics, outperforming previous world models by a large margin. The world model achieves real-time interactive inference on a single GPU through a shortcut forcing objective and an efficient transformer architecture. Moreover, the world model learns general action conditioning from only a small amount of data, allowing it to extract the majority of its knowledge from diverse unlabeled videos. We propose the challenge of obtaining diamonds in Minecraft from only offline data, aligning with practical applications such as robotics where learning from environment interaction can be unsafe and slow. This task requires choosing sequences of over 20,000 mouse and keyboard actions from raw pixels. By learning behaviors in imagination, Dreamer 4 is the first agent to obtain diamonds in Minecraft purely from offline data, without environment interaction. Our work provides a scalable recipe for imagination training, marking a step towards intelligent agents.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Website: https://danijar.com/dreamer4/

[在 Zotero 查看](zotero://select/library/items/YLF5NPGH)

Comment: Website: https://danijar.com/dreamer4/

## 附件与批注

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/G5D7BJDB)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/SUY86G4T)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-QR2DUKWD - Mastering Atari with Discrete World Models|Mastering Atari with Discrete World Models]] — 中关联；共同研究内容：想象与模型式强化学习。
- [[Zotero Knowledge/Papers/ZK-XRENB5FA - Mastering Diverse Domains through World Models|Mastering Diverse Domains through World Models]] — 中关联；共同研究内容：想象与模型式强化学习。
- [[Zotero Knowledge/Papers/ZK-4MHFRDYK - Ctrl-World  A Controllable Generative World Model for Robot Manipulation|Ctrl-World: A Controllable Generative World Model for Robot Manipulation]] — 中关联；共同研究内容：动作条件预测、想象与模型式强化学习。

<!-- content-relations:end -->
