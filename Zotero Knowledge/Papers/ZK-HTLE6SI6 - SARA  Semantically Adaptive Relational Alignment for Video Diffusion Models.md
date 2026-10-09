---
type: "literature-note"
title: "SARA: Semantically Adaptive Relational Alignment for Video Diffusion Models"
aliases: ["SARA: Semantically Adaptive Relational Alignment for Video Diffusion Models"]
zotero_keys: ["HTLE6SI6"]
year: 2026
authors: ["Jiesong Lian", "Zixiang Zhou", "Ruizhe Zhong", "Yuan Zhou", "Qinglin Lu", "Rui Wang", "Long Hu", "Yixue Hao", "Baoru Huang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2605.07800"
url: "http://arxiv.org/abs/2605.07800"
collections: ["06 Alignment & Reliability/Representation Alignment"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature", "concept/物理一致性与表征对齐", "concept-primary/物理一致性与表征对齐"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# SARA: Semantically Adaptive Relational Alignment for Video Diffusion Models

[Zotero 条目 HTLE6SI6](zotero://select/library/items/HTLE6SI6)

[DOI 原文](https://doi.org/10.48550/arxiv.2605.07800)

[来源网页](http://arxiv.org/abs/2605.07800)

## 主题与知识联系

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]]

概念地图：[[Zotero Knowledge/Concepts/物理一致性与表征对齐|物理一致性与表征对齐]]

## 原始摘要

Recent video diffusion models (VDMs) synthesize visually convincing clips, yet still drop entities, mis-bind attributes, and weaken the interactions specified in the prompt. Representation-alignment objectives such as VideoREPA and MoAlign improve fine-grained text following by distilling spatio-temporal token relations from a frozen visual foundation model, but their pairwise supervision budget is allocated by visual or motion cues rather than by how relevant each pair is to the prompt. We present SARA, Semantically Adaptive Relational Alignment, which keeps token-relation distillation (TRD) on a frozen VFM target and adds a text-conditioned saliency that decides which token pairs carry supervision. A lightweight Stage~1 aligner is trained with per-entity SAM~3.1 mask supervision and an InfoNCE regulariser, and its continuous saliency is fused into TRD through a pair-routing operator that assigns each token pair a weight whenever either of its two endpoints is salient, thereby routing supervision toward subject-subject and subject-background pairs and away from background-background ones. In the Wan2.2 continual-training setting, SARA improves both text alignment and motion quality over SFT, VideoREPA, and MoAlign on a 13-dimension VLM rubric, on the public VBench benchmarks, and in a blind user study. Project page: https://saradit.github.io/.

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/EJCINZKK)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/BCZ9MP8C)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-7TDQKU5X - VideoREPA  Learning Physics for Video Generation through Relational Alignment with Fo|VideoREPA: Learning Physics for Video Generation through Relational Alignment with Foundation Models]] — 强关联；本篇摘要提到模型 VideoREPA（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-VAQCDKF8 - MoAlign  Motion-Centric Representation Alignment for Video Diffusion Models|MoAlign: Motion-Centric Representation Alignment for Video Diffusion Models]] — 强关联；本篇摘要提到模型 MoAlign（仅确认名称提及）。

<!-- content-relations:end -->
