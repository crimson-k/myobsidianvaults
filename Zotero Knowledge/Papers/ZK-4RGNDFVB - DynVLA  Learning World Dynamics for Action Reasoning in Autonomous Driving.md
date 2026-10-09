---
type: "literature-note"
title: "DynVLA: Learning World Dynamics for Action Reasoning in Autonomous Driving"
aliases: ["DynVLA: Learning World Dynamics for Action Reasoning in Autonomous Driving"]
zotero_keys: ["4RGNDFVB"]
year: 2026
authors: ["Shuyao Shang", "Bing Zhan", "Yunfei Yan", "Yuqi Wang", "Yingyan Li", "Yasong An", "Xiaoman Wang", "Jierui Liu", "Lu Hou", "Lue Fan", "Zhaoxiang Zhang", "Tieniu Tan"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2603.11041"
url: "http://arxiv.org/abs/2603.11041"
collections: ["05 Robot Learning/Vision-Language Policies"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Robotics"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# DynVLA: Learning World Dynamics for Action Reasoning in Autonomous Driving

[Zotero 条目 4RGNDFVB](zotero://select/library/items/4RGNDFVB)

[DOI 原文](https://doi.org/10.48550/arxiv.2603.11041)

[来源网页](http://arxiv.org/abs/2603.11041)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Vision-Language Policies/索引|05 Robot Learning/Vision-Language Policies]]

## 原始摘要

We propose DynVLA, a driving VLA model that introduces a new CoT paradigm termed Dynamics CoT. DynVLA forecasts compact world dynamics before action generation, enabling more informed and physically grounded decision-making. To obtain compact dynamics representations, DynVLA introduces a Dynamics Tokenizer that compresses future evolution into a small set of dynamics tokens. Considering the rich environment dynamics in interaction-intensive driving scenarios, DynVLA decouples ego-centric and environment-centric dynamics, yielding more accurate world dynamics modeling. We then train DynVLA to generate dynamics tokens before actions through SFT and RFT, improving decision quality while maintaining latency-efficient inference. Compared to Textual CoT, which lacks fine-grained spatiotemporal understanding, and Visual CoT, which introduces substantial redundancy due to dense image prediction, Dynamics CoT captures the evolution of the world in a compact, interpretable, and efficient form. Extensive experiments on NAVSIM, Bench2Drive, and a large-scale in-house dataset demonstrate that DynVLA consistently outperforms Textual CoT and Visual CoT methods, validating the effectiveness and practical value of Dynamics CoT. Project Page: https://yaoyao-jpg.github.io/dynvla.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: 18 pages, 10 figures. Project Page: https://yaoyao-jpg.github.io/dynvla

[在 Zotero 查看](zotero://select/library/items/LVLZYU3Q)

Comment: 18 pages, 10 figures. Project Page: https://yaoyao-jpg.github.io/dynvla

## 附件与批注

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/YNR5ZLQA)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/TF5Y6PKT)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-FTHILNAK - Epona  Autoregressive Diffusion World Model for Autonomous Driving|Epona: Autoregressive Diffusion World Model for Autonomous Driving]] — 中关联；共同研究内容：自动驾驶。

<!-- content-relations:end -->
