---
type: "literature-note"
title: "ChordEdit: One-Step Low-Energy Transport for Image Editing"
aliases: ["ChordEdit: One-Step Low-Energy Transport for Image Editing"]
zotero_keys: ["5BQVFC9Y"]
year: 2026
authors: ["Liangsi Lu", "Xuhang Chen", "Minzhe Guo", "Shichu Li", "Jingchao Wang", "Yang Shi"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2602.19083"
url: "http://arxiv.org/abs/2602.19083"
collections: ["03 Visual Generation/Editing & Identity Control"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# ChordEdit: One-Step Low-Energy Transport for Image Editing

[Zotero 条目 5BQVFC9Y](zotero://select/library/items/5BQVFC9Y)

[DOI 原文](https://doi.org/10.48550/arxiv.2602.19083)

[来源网页](http://arxiv.org/abs/2602.19083)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Editing & Identity Control/索引|03 Visual Generation/Editing & Identity Control]]

## 原始摘要

The advent of one-step text-to-image (T2I) models offers unprecedented synthesis speed. However, their application to text-guided image editing remains severely hampered, as forcing existing training-free editors into a single inference step fails. This failure manifests as severe object distortion and a critical loss of consistency in non-edited regions, resulting from the high-energy, erratic trajectories produced by naive vector arithmetic on the models' structured fields. To address this problem, we introduce ChordEdit, a model agnostic, training-free, and inversion-free method that facilitates high-fidelity one-step editing. We recast editing as a transport problem between the source and target distributions defined by the source and target text prompts. Leveraging dynamic optimal transport theory, we derive a principled, low-energy control strategy. This strategy yields a smoothed, variance-reduced editing field that is inherently stable, facilitating the field to be traversed in a single, large integration step. A theoretically grounded and experimentally validated approach allows ChordEdit to deliver fast, lightweight and precise edits, finally achieving true real-time editing on these challenging models.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Accepted by CVPR 2026

[在 Zotero 查看](zotero://select/library/items/IHFNXSIY)

Comment: Accepted by CVPR 2026

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/ZZE9CHF3)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/QUGS3REX)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-IDTQ2XG3 - VACE  All-in-One Video Creation and Editing|VACE: All-in-One Video Creation and Editing]] — 中关联；共同研究内容：扩散生成架构、视频编辑与身份保持。

<!-- content-relations:end -->
