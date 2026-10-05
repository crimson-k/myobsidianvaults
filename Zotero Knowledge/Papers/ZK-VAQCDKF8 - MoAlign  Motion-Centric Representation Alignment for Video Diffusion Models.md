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
tags: ["zotero", "literature", "highlight"]
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
