---
type: "literature-note"
title: "From Slow Bidirectional to Fast Autoregressive Video Diffusion Models"
aliases: ["From Slow Bidirectional to Fast Autoregressive Video Diffusion Models"]
zotero_keys: ["UNNWY4C6", "V8WTJ656"]
year: 2024
authors: ["Tianwei Yin", "Qiang Zhang", "Richard Zhang", "William T. Freeman", "Fredo Durand", "Eli Shechtman", "Xun Huang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2412.07772"
url: "https://arxiv.org/abs/2412.07772"
collections: ["03 Visual Generation/General Video Generation"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences"]
tags: ["zotero", "literature", "concept/视频生成的因果化与流式推理", "concept-primary/视频生成的因果化与流式推理"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# From Slow Bidirectional to Fast Autoregressive Video Diffusion Models

[Zotero 条目 UNNWY4C6](zotero://select/library/items/UNNWY4C6) · [Zotero 条目 V8WTJ656](zotero://select/library/items/V8WTJ656)

[DOI 原文](https://doi.org/10.48550/arxiv.2412.07772)

[来源网页](https://arxiv.org/abs/2412.07772)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/General Video Generation/索引|03 Visual Generation/General Video Generation]]

概念地图：[[Zotero Knowledge/Concepts/视频生成的因果化与流式推理|视频生成的因果化与流式推理]]

## 原始摘要

Current video diffusion models achieve impressive generation quality but struggle in interactive applications due to bidirectional attention dependencies. The generation of a single frame requires the model to process the entire sequence, including the future. We address this limitation by adapting a pretrained bidirectional diffusion transformer to an autoregressive transformer that generates frames on-the-fly. To further reduce latency, we extend distribution matching distillation (DMD) to videos, distilling 50-step diffusion model into a 4-step generator. To enable stable and high-quality distillation, we introduce a student initialization scheme based on teacher's ODE trajectories, as well as an asymmetric distillation strategy that supervises a causal student model with a bidirectional teacher. This approach effectively mitigates error accumulation in autoregressive generation, allowing long-duration video synthesis despite training on short clips. Our model achieves a total score of 84.27 on the VBench-Long benchmark, surpassing all previous video generation models. It enables fast streaming generation of high-quality videos at 9.4 FPS on a single GPU thanks to KV caching. Our approach also enables streaming video-to-video translation, image-to-video, and dynamic prompting in a zero-shot manner.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/CVQHKXR5)

## Other
CVPR 2025. Project Page: https://causvid.github.io/

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/32IJ5KPJ)

### PDF

[打开 PDF](zotero://open-pdf/library/items/VA5CXFBD)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

> 本笔记合并了相同 DOI 的 2 条记录；Zotero 原条目均保留。
