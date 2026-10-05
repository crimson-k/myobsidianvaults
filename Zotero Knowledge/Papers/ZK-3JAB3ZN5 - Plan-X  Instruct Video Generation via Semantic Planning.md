---
type: "literature-note"
title: "Plan-X: Instruct Video Generation via Semantic Planning"
aliases: ["Plan-X: Instruct Video Generation via Semantic Planning"]
zotero_keys: ["3JAB3ZN5"]
year: 2025
authors: ["Lun Huang", "You Xie", "Hongyi Xu", "Tianpei Gu", "Chenxu Zhang", "Guoxian Song", "Zenan Li", "Xiaochen Zhao", "Linjie Luo", "Guillermo Sapiro"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2511.17986"
url: "http://arxiv.org/abs/2511.17986"
collections: ["03 Visual Generation/General Video Generation"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Plan-X: Instruct Video Generation via Semantic Planning

[Zotero 条目 3JAB3ZN5](zotero://select/library/items/3JAB3ZN5)

[DOI 原文](https://doi.org/10.48550/arxiv.2511.17986)

[来源网页](http://arxiv.org/abs/2511.17986)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/General Video Generation/索引|03 Visual Generation/General Video Generation]]

## 原始摘要

Diffusion Transformers have demonstrated remarkable capabilities in visual synthesis, yet they often struggle with high-level semantic reasoning and long-horizon planning. This limitation frequently leads to visual hallucinations and mis-alignments with user instructions, especially in scenarios involving complex scene understanding, human-object interactions, multi-stage actions, and in-context motion reasoning. To address these challenges, we propose Plan-X, a framework that explicitly enforces high-level semantic planning to instruct video generation process. At its core lies a Semantic Planner, a learnable multimodal language model that reasons over the user's intent from both text prompts and visual context, and autoregressively generates a sequence of text-grounded spatio-temporal semantic tokens. These semantic tokens, complementary to high-level text prompt guidance, serve as structured "semantic sketches" over time for the video diffusion model, which has its strength at synthesizing high-fidelity visual details. Plan-X effectively integrates the strength of language models in multimodal in-context reasoning and planning, together with the strength of diffusion models in photorealistic video synthesis. Extensive experiments demonstrate that our framework substantially reduces visual hallucinations and enables fine-grained, instruction-aligned video generation consistent with multimodal context.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: The project page is at https://byteaigc.github.io/Plan-X

[在 Zotero 查看](zotero://select/library/items/LIFHJ5T3)

Comment: The project page is at https://byteaigc.github.io/Plan-X

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/JI7DXQDX)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
