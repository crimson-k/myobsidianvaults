---
type: "literature-note"
title: "The Best of Both Worlds: Integrating Language Models and Diffusion Models for Video Generation"
aliases: ["The Best of Both Worlds: Integrating Language Models and Diffusion Models for Video Generation"]
zotero_keys: ["6CEJBRP2"]
year: 2025
authors: ["Aoxiong Yin", "Kai Shen", "Yichong Leng", "Xu Tan", "Xinyu Zhou", "Juncheng Li", "Siliang Tang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2503.04606"
url: "http://arxiv.org/abs/2503.04606"
collections: ["03 Visual Generation/General Video Generation"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computation and Language", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning"]
tags: ["zotero", "literature", "concept/视频生成的因果化与流式推理", "concept-primary/视频生成的因果化与流式推理"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# The Best of Both Worlds: Integrating Language Models and Diffusion Models for Video Generation

[Zotero 条目 6CEJBRP2](zotero://select/library/items/6CEJBRP2)

[DOI 原文](https://doi.org/10.48550/arxiv.2503.04606)

[来源网页](http://arxiv.org/abs/2503.04606)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/General Video Generation/索引|03 Visual Generation/General Video Generation]]

概念地图：[[Zotero Knowledge/Concepts/视频生成的因果化与流式推理|视频生成的因果化与流式推理]]

## 原始摘要

Recent advancements in text-to-video (T2V) generation have been driven by two competing paradigms: autoregressive language models and diffusion models. However, each paradigm has intrinsic limitations: language models struggle with visual quality and error accumulation, while diffusion models lack semantic understanding and causal modeling. In this work, we propose LanDiff, a hybrid framework that synergizes the strengths of both paradigms through coarse-tofine generation. Our architecture introduces three key innovations: (1) a semantic tokenizer that compresses 3D visual features into compact 1D discrete representations through efficient semantic compression, achieving a ∼14,000× compression ratio; (2) a language model that generates semantic tokens with high-level semantic relationships; (3) a streaming diffusion model that refines coarse semantics into high-fidelity videos. Experiments show that LanDiff, a 5B model, achieves a score of 85.43 on the VBench T2V benchmark, surpassing the state-of-the-art open-source models Hunyuan Video (13B) and other commercial models such as Sora, Kling, and Hailuo. Furthermore, our model also achieves state-of-the-art performance in long video generation, surpassing other open-source models in this field. Our demo can be viewed at https: //landiff.github.io/.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Our code is available at https://github.com/LanDiff/LanDiff

[在 Zotero 查看](zotero://select/library/items/2ZQ53Y2X)

Comment: Our code is available at https://github.com/LanDiff/LanDiff

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/JBZXBKT9)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
