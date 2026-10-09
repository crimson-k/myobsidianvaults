---
type: "literature-note"
title: "SemanticGen: Video Generation in Semantic Space"
aliases: ["SemanticGen: Video Generation in Semantic Space"]
zotero_keys: ["TQGK3SJJ"]
year: 2025
authors: ["Jianhong Bai", "Xiaoshi Wu", "Xintao Wang", "Xiao Fu", "Yuanxing Zhang", "Qinghe Wang", "Xiaoyu Shi", "Menghan Xia", "Zuozhu Liu", "Haoji Hu", "Pengfei Wan", "Kun Gai"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2512.20619"
url: "http://arxiv.org/abs/2512.20619"
collections: ["03 Visual Generation/General Video Generation"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# SemanticGen: Video Generation in Semantic Space

[Zotero 条目 TQGK3SJJ](zotero://select/library/items/TQGK3SJJ)

[DOI 原文](https://doi.org/10.48550/arxiv.2512.20619)

[来源网页](http://arxiv.org/abs/2512.20619)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/General Video Generation/索引|03 Visual Generation/General Video Generation]]

## 原始摘要

State-of-the-art video generative models typically learn the distribution of video latents in the VAE space and map them to pixels using a VAE decoder. While this approach can generate high-quality videos, it suffers from slow convergence and is computationally expensive when generating long videos. In this paper, we introduce SemanticGen, a novel solution to address these limitations by generating videos in the semantic space. Our main insight is that, due to the inherent redundancy in videos, the generation process should begin in a compact, high-level semantic space for global planning, followed by the addition of high-frequency details, rather than directly modeling a vast set of low-level video tokens using bi-directional attention. SemanticGen adopts a two-stage generation process. In the first stage, a diffusion model generates compact semantic video features, which define the global layout of the video. In the second stage, another diffusion model generates VAE latents conditioned on these semantic features to produce the final output. We observe that generation in the semantic space leads to faster convergence compared to the VAE latent space. Our method is also effective and computationally efficient when extended to long video generation. Extensive experiments demonstrate that SemanticGen produces high-quality videos and outperforms state-of-the-art approaches and strong baselines.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project page: https://jianhongbai.github.io/SemanticGen/

[在 Zotero 查看](zotero://select/library/items/WXNRURG6)

Comment: Project page: https://jianhongbai.github.io/SemanticGen/

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/DUD8CJDL)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-3JAB3ZN5 - Plan-X  Instruct Video Generation via Semantic Planning|Plan-X: Instruct Video Generation via Semantic Planning]] — 中关联；共同研究内容：扩散生成架构、视频离散 / 语义 token。
- [[Zotero Knowledge/Papers/ZK-6CEJBRP2 - The Best of Both Worlds  Integrating Language Models and Diffusion Models for Video G|The Best of Both Worlds: Integrating Language Models and Diffusion Models for Video Generation]] — 中关联；共同研究内容：扩散生成架构、视频离散 / 语义 token。

<!-- content-relations:end -->
