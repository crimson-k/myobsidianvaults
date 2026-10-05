---
type: "literature-note"
title: "Learning to Feel the Future: DreamTacVLA for Contact-Rich Manipulation"
aliases: ["Learning to Feel the Future: DreamTacVLA for Contact-Rich Manipulation"]
zotero_keys: ["8L5EA7BP"]
year: 2025
authors: ["Guo Ye", "Zexi Zhang", "Xu Zhao", "Shang Wu", "Haoran Lu", "Shihan Lu", "Han Liu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2512.23864"
url: "http://arxiv.org/abs/2512.23864"
collections: ["05 Robot Learning/Vision-Language Policies"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Robotics"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Learning to Feel the Future: DreamTacVLA for Contact-Rich Manipulation

[Zotero 条目 8L5EA7BP](zotero://select/library/items/8L5EA7BP)

[DOI 原文](https://doi.org/10.48550/arxiv.2512.23864)

[来源网页](http://arxiv.org/abs/2512.23864)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Vision-Language Policies/索引|05 Robot Learning/Vision-Language Policies]]

## 原始摘要

Vision-Language-Action (VLA) models have shown remarkable generalization by mapping web-scale knowledge to robotic control, yet they remain blind to physical contact. Consequently, they struggle with contact-rich manipulation tasks that require reasoning about force, texture, and slip. While some approaches incorporate low-dimensional tactile signals, they fail to capture the high-resolution dynamics essential for such interactions. To address this limitation, we introduce DreamTacVLA, a framework that grounds VLA models in contact physics by learning to feel the future. Our model adopts a hierarchical perception scheme in which high-resolution tactile images serve as micro-vision inputs coupled with wrist-camera local vision and third-person macro vision. To reconcile these multi-scale sensory streams, we first train a unified policy with a Hierarchical Spatial Alignment (HSA) loss that aligns tactile tokens with their spatial counterparts in the wrist and third-person views. To further deepen the model's understanding of fine-grained contact dynamics, we finetune the system with a tactile world model that predicts future tactile signals. To mitigate tactile data scarcity and the wear-prone nature of tactile sensors, we construct a hybrid large-scale dataset sourced from both high-fidelity digital twin and real-world experiments. By anticipating upcoming tactile states, DreamTacVLA acquires a rich model of contact physics and conditions its actions on both real observations and imagined consequences. Across contact-rich manipulation tasks, it outperforms state-of-the-art VLA baselines, achieving up to 95% success, highlighting the importance of understanding physical contact for robust, touch-aware robotic agents.

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/ZBYE6GHC)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/RMKKDE4D)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
