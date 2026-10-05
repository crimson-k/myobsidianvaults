---
type: "literature-note"
title: "Video Motion Transfer with Diffusion Transformers"
aliases: ["Video Motion Transfer with Diffusion Transformers"]
zotero_keys: ["EDKKKAFE"]
year: null
authors: ["Alexander Pondaven", "Aliaksandr Siarohin", "Sergey Tulyakov", "Philip Torr", "Fabio Pizzati"]
venue: ""
venue_field: null
doi: ""
url: ""
collections: ["03 Visual Generation/Camera & Motion Control"]
source_tags: []
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Video Motion Transfer with Diffusion Transformers

[Zotero 条目 EDKKKAFE](zotero://select/library/items/EDKKKAFE)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Camera & Motion Control/索引|03 Visual Generation/Camera & Motion Control]]

## 原始摘要

We propose DiTFlow, a method for transferring the motion of a reference video to a newly synthesized one, designed specifically for Diffusion Transformers (DiT). We first process the reference video with a pre-trained DiT to analyze cross-frame attention maps and extract a patch-wise motion signal called the Attention Motion Flow (AMF). We guide the latent denoising process in an optimization-based, training-free, manner by optimizing latents with our AMF loss to generate videos reproducing the motion of the reference one. We also apply our optimization strategy to transformer positional embeddings, granting us a boost in zero-shot motion transfer capabilities. We evaluate DiTFlow against recently published methods, outperforming all across multiple metrics and human evaluation.

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/2ZWNTPN9)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
