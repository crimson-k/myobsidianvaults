---
type: "literature-note"
title: "RoFormer: Enhanced Transformer with Rotary Position Embedding"
aliases: ["RoFormer: Enhanced Transformer with Rotary Position Embedding"]
zotero_keys: ["KUDCFD8D"]
year: 2023
authors: ["Jianlin Su", "Yu Lu", "Shengfeng Pan", "Ahmed Murtadha", "Bo Wen", "Yunfeng Liu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2104.09864"
url: "http://arxiv.org/abs/2104.09864"
collections: ["01 Foundations"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computation and Language", "Computer Science - Machine Learning"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# RoFormer: Enhanced Transformer with Rotary Position Embedding

[Zotero 条目 KUDCFD8D](zotero://select/library/items/KUDCFD8D)

[DOI 原文](https://doi.org/10.48550/arxiv.2104.09864)

[来源网页](http://arxiv.org/abs/2104.09864)

## 主题与知识联系

- [[Zotero Knowledge/Topics/01 Foundations/索引|01 Foundations]]

## 原始摘要

Position encoding recently has shown effective in the transformer architecture. It enables valuable supervision for dependency modeling between elements at different positions of the sequence. In this paper, we first investigate various methods to integrate positional information into the learning process of transformer-based language models. Then, we propose a novel method named Rotary Position Embedding(RoPE) to effectively leverage the positional information. Specifically, the proposed RoPE encodes the absolute position with a rotation matrix and meanwhile incorporates the explicit relative position dependency in self-attention formulation. Notably, RoPE enables valuable properties, including the flexibility of sequence length, decaying inter-token dependency with increasing relative distances, and the capability of equipping the linear self-attention with relative position encoding. Finally, we evaluate the enhanced transformer with rotary position embedding, also called RoFormer, on various long text classification benchmark datasets. Our experiments show that it consistently overcomes its alternatives. Furthermore, we provide a theoretical analysis to explain some experimental results. RoFormer is already integrated into Huggingface: \url{https://huggingface.co/docs/transformers/model_doc/roformer}.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: fixed some typos

[在 Zotero 查看](zotero://select/library/items/TI7SCAGV)

Comment: fixed some typos

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/LC8937EM)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/5QZ56RR8)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
