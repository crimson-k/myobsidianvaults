---
type: "literature-note"
title: "MoAlign: Motion-Centric Representation Alignment for Video Diffusion Models"
aliases: ["MoAlign: Motion-Centric Representation Alignment for Video Diffusion Models"]
zotero_keys: ["VAQCDKF8"]
year: 2025
authors: ["Aritra Bhowmik", "Denis Korzhenkov", "Cees G. M. Snoek", "Amirhossein Habibian", "Mohsen Ghafoorian"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2510.19022"
url: "https://arxiv.org/abs/2510.19022"
collections: ["06 Alignment & Reliability/Representation Alignment"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences"]
tags: ["zotero", "literature", "highlight", "concept/物理一致性与表征对齐", "concept-primary/物理一致性与表征对齐"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# MoAlign: Motion-Centric Representation Alignment for Video Diffusion Models

[Zotero 条目 VAQCDKF8](zotero://select/library/items/VAQCDKF8)

[DOI 原文](https://doi.org/10.48550/arxiv.2510.19022)

[来源网页](https://arxiv.org/abs/2510.19022)

## 主题与知识联系

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]]

概念地图：[[Zotero Knowledge/Concepts/物理一致性与表征对齐|物理一致性与表征对齐]]

## 原始摘要

Text-to-video diffusion models have enabled high-quality video synthesis, yet often fail to generate temporally coherent and physically plausible motion. A key reason is the models’ insufficient understanding of complex motions that natural videos often entail. Recent works tackle this problem by aligning diffusion model features with those from pretrained video encoders. However, these encoders mix video appearance and dynamics into entangled features, limiting the benefit of such alignment. In this paper, we propose a motion-centric alignment framework that learns a disentangled motion subspace from a pretrained video encoder. This subspace is optimized to predict ground-truth optical flow, ensuring it captures true motion dynamics. We then align the latent features of a text-to-video diffusion model to this new subspace, enabling the generative model to internalize motion knowledge and generate more plausible videos. Our method improves the physical commonsense in a state-of-the-art video diffusion model, while preserving adherence to textual prompts, as evidenced by empirical evaluations on VideoPhy, VideoPhy2, VBench, and VBench-2.0, along with a user study.

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/P6CNJ32S)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-7TDQKU5X - VideoREPA  Learning Physics for Video Generation through Relational Alignment with Fo|VideoREPA: Learning Physics for Video Generation through Relational Alignment with Foundation Models]] — 强关联；均把视频编码器表征对齐到生成模型；比较 token 关系与运动子空间监督。
- [[Zotero Knowledge/Papers/ZK-HTLE6SI6 - SARA  Semantically Adaptive Relational Alignment for Video Diffusion Models|SARA: Semantically Adaptive Relational Alignment for Video Diffusion Models]] — 强关联；对方摘要提到模型 MoAlign（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-AWA338G8 - Representation Alignment for Generation  Training Diffusion Transformers Is Easier Th|Representation Alignment for Generation: Training Diffusion Transformers Is Easier Than You Think]] — 强关联；比较生成模型的外部表征监督与视频运动专属对齐。
- [[Zotero Knowledge/Papers/ZK-3X7CKIBU - Motion Forcing  A Decoupled Framework for Robust Video Generation in Motion Dynamics|Motion Forcing: A Decoupled Framework for Robust Video Generation in Motion Dynamics]] — 强关联；都聚焦运动动力学与物理合理性，比较运动/外观解耦与运动子空间对齐。

<!-- content-relations:end -->
