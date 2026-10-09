---
type: "literature-note"
title: "Collaborative Face Experts Fusion in Video Generation: Boosting Identity Consistency Across Large Face Poses"
aliases: ["Collaborative Face Experts Fusion in Video Generation: Boosting Identity Consistency Across Large Face Poses"]
zotero_keys: ["E3MAYR9A"]
year: 2025
authors: ["Yuji Wang", "Moran Li", "Xiaobin Hu", "Ran Yi", "Jiangning Zhang", "Chengming Xu", "Weijian Cao", "Yabiao Wang", "Chengjie Wang", "Lizhuang Ma"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2508.09476"
url: "http://arxiv.org/abs/2508.09476"
collections: ["03 Visual Generation/Editing & Identity Control"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Collaborative Face Experts Fusion in Video Generation: Boosting Identity Consistency Across Large Face Poses

[Zotero 条目 E3MAYR9A](zotero://select/library/items/E3MAYR9A)

[DOI 原文](https://doi.org/10.48550/arxiv.2508.09476)

[来源网页](http://arxiv.org/abs/2508.09476)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Editing & Identity Control/索引|03 Visual Generation/Editing & Identity Control]]

## 原始摘要

Current video generation models struggle with identity preservation under large face poses, primarily facing two challenges: the difficulty in exploring an effective mechanism to integrate identity features into DiT architectures, and the lack of targeted coverage of large face poses in existing open-source video datasets. To address these, we present two key innovations. First, we propose Collaborative Face Experts Fusion (CoFE), which dynamically fuses complementary signals from three specialized experts within the DiT backbone: an identity expert that captures cross-pose invariant features, a semantic expert that encodes high-level visual context, and a detail expert that preserves pixel-level attributes such as skin texture and color gradients. Second, we introduce a data curation pipeline comprising three key components: Face Constraints to ensure diverse large-pose coverage, Identity Consistency to maintain stable identity across frames, and Speech Disambiguation to align textual captions with actual speaking behavior. This pipeline yields LaFID-180K, a large-scale dataset of pose-annotated video clips designed for identity-preserving video generation. Experimental results on several benchmarks demonstrate that our approach significantly outperforms state-of-the-art methods in face similarity, FID, and CLIP semantic alignment. Project page: https://rain152.github.io/CoFE/.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project page: https://rain152.github.io/CoFE/

[在 Zotero 查看](zotero://select/library/items/CTK4NM6E)

Comment: Project page: https://rain152.github.io/CoFE/

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/83MRY29R)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/928WP32S)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-CDHTS2WR - Learning Transferable Visual Models From Natural Language Supervision|Learning Transferable Visual Models From Natural Language Supervision]] — 强关联；本篇摘要提到模型 CLIP（仅确认名称提及）。

<!-- content-relations:end -->
