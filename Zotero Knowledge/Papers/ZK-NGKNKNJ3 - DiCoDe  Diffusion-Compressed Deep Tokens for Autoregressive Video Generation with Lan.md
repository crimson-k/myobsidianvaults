---
type: "literature-note"
title: "DiCoDe: Diffusion-Compressed Deep Tokens for Autoregressive Video Generation with Language Models"
aliases: ["DiCoDe: Diffusion-Compressed Deep Tokens for Autoregressive Video Generation with Language Models"]
zotero_keys: ["NGKNKNJ3"]
year: 2026
authors: ["Yizhuo Li", "Yuying Ge", "Yixiao Ge", "Ying Shan", "Ping Luo"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2412.04446"
url: "http://arxiv.org/abs/2412.04446"
collections: ["03 Visual Generation/General Video Generation"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature", "concept/视频生成的因果化与流式推理", "concept-primary/视频生成的因果化与流式推理"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# DiCoDe: Diffusion-Compressed Deep Tokens for Autoregressive Video Generation with Language Models

[Zotero 条目 NGKNKNJ3](zotero://select/library/items/NGKNKNJ3)

[DOI 原文](https://doi.org/10.48550/arxiv.2412.04446)

[来源网页](http://arxiv.org/abs/2412.04446)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/General Video Generation/索引|03 Visual Generation/General Video Generation]]

概念地图：[[Zotero Knowledge/Concepts/视频生成的因果化与流式推理|视频生成的因果化与流式推理]]

## 原始摘要

Videos are inherently temporal sequences by their very nature. In this work, we explore the potential of modeling videos in a chronological and scalable manner with autoregressive (AR) language models, inspired by their success in natural language processing. We introduce DiCoDe, a novel approach that leverages Diffusion-Compressed Deep Tokens to generate videos with a language model in an autoregressive manner. Unlike existing methods that employ low-level representations with limited compression rates, DiCoDe utilizes deep tokens with a considerable compression rate (a 1000x reduction in token count). This significant compression is made possible by a tokenizer trained through leveraging the prior knowledge of video diffusion models. Deep tokens enable DiCoDe to employ vanilla AR language models for video generation, akin to translating one visual "language" into another. By treating videos as temporal sequences, DiCoDe fully harnesses the capabilities of language models for autoregressive generation. DiCoDe is scalable using readily available AR architectures, and is capable of generating videos ranging from a few seconds to one minute using only 4 A100 GPUs for training. We evaluate DiCoDe both quantitatively and qualitatively, demonstrating that it performs comparably to existing methods in terms of quality while ensuring efficient training. To showcase its scalability, we release a series of DiCoDe configurations with varying parameter sizes and observe a consistent improvement in performance as the model size increases from 100M to 3B. We believe that DiCoDe's exploration in academia represents a promising initial step toward scalable video modeling with AR language models, paving the way for the development of larger and more powerful video generation models.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project Page: https://liyz15.github.io/DiCoDe

[在 Zotero 查看](zotero://select/library/items/ESIN3DLA)

Comment: Project Page: https://liyz15.github.io/DiCoDe

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/AK899FJQ)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/JCDK3BDP)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
