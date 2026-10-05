---
type: "literature-note"
title: "RoboTwin 2.0: A Scalable Data Generator and Benchmark with Strong Domain Randomization for Robust Bimanual Robotic Manipulation"
aliases: ["RoboTwin 2.0: A Scalable Data Generator and Benchmark with Strong Domain Randomization for Robust Bimanual Robotic Manipulation"]
zotero_keys: ["84JCUMH6"]
year: 2025
authors: ["Tianxing Chen", "Zanxin Chen", "Baijun Chen", "Zijian Cai", "Yibin Liu", "Zixuan Li", "Qiwei Liang", "Xianliang Lin", "Yiheng Ge", "Zhenyu Gu", "Weiliang Deng", "Yubin Guo", "Tian Nian", "Xuanbing Xie", "Qiangyu Chen", "Kailun Su", "Tianling Xu", "Guodong Liu", "Mengkang Hu", "Huan-ang Gao", "Kaixuan Wang", "Zhixuan Liang", "Yusen Qin", "Xiaokang Yang", "Ping Luo", "Yao Mu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2506.18088"
url: "http://arxiv.org/abs/2506.18088"
collections: ["07 Evaluation & Data/Robot & Multiview Data"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computation and Language", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Multiagent Systems", "Computer Science - Robotics"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# RoboTwin 2.0: A Scalable Data Generator and Benchmark with Strong Domain Randomization for Robust Bimanual Robotic Manipulation

[Zotero 条目 84JCUMH6](zotero://select/library/items/84JCUMH6)

[DOI 原文](https://doi.org/10.48550/arxiv.2506.18088)

[来源网页](http://arxiv.org/abs/2506.18088)

## 主题与知识联系

- [[Zotero Knowledge/Topics/07 Evaluation & Data/Robot & Multiview Data/索引|07 Evaluation & Data/Robot & Multiview Data]]

概念地图：[[Zotero Knowledge/Concepts/世界模型评测与功能有效性|世界模型评测与功能有效性]]

## 原始摘要

Simulation-based data synthesis has emerged as a powerful paradigm for advancing real-world robotic manipulation. Yet existing datasets remain insufficient for robust bimanual manipulation due to (1) the lack of scalable task generation methods and (2) oversimplified simulation environments. We present RoboTwin 2.0, a scalable framework for automated, large-scale generation of diverse and realistic data, together with unified evaluation protocols for dual-arm manipulation. At its core is RoboTwin-OD, an object library of 731 instances across 147 categories with semantic and manipulation-relevant annotations. Building on this, we design an expert data synthesis pipeline that leverages multimodal language models (MLLMs) and simulation-in-the-loop refinement to automatically generate task-level execution code. To improve sim-to-real transfer, RoboTwin 2.0 applies structured domain randomization along five axes: clutter, lighting, background, tabletop height, and language, enhancing data diversity and policy robustness. The framework is instantiated across 50 dual-arm tasks and five robot embodiments. Empirically, it yields a 10.9% gain in code generation success rate. For downstream policy learning, a VLA model trained with synthetic data plus only 10 real demonstrations achieves a 367% relative improvement over the 10-demo baseline, while zero-shot models trained solely on synthetic data obtain a 228% gain. These results highlight the effectiveness of RoboTwin 2.0 in strengthening sim-to-real transfer and robustness to environmental variations. We release the data generator, benchmark, dataset, and code to support scalable research in robust bimanual manipulation. Project Page: https://robotwin-platform.github.io/, Code: https://github.com/robotwin-Platform/robotwin/.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project Page: https://robotwin-platform.github.io/, Code: https://github.com/robotwin-Platform/robotwin, Doc: h

[在 Zotero 查看](zotero://select/library/items/EJ753N9Y)

Comment: Project Page: https://robotwin-platform.github.io/, Code: https://github.com/robotwin-Platform/robotwin, Doc: https://robotwin-platform.github.io/doc/

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/WKNL3R49)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/D7QATKUJ)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
