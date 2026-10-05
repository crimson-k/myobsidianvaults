---
type: "literature-note"
title: "HeteroGenManip: Generalizable Manipulation For Heterogeneous Object Interactions"
aliases: ["HeteroGenManip: Generalizable Manipulation For Heterogeneous Object Interactions"]
zotero_keys: ["YJJJPGKS"]
year: 2026
authors: ["Zhenhao Shen", "Zeming Yang", "Yue Chen", "Yuran Wang", "Shengqiang Xu", "Mingleyang Li", "Hao Dong", "Ruihai Wu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2605.10201"
url: "http://arxiv.org/abs/2605.10201"
collections: ["05 Robot Learning/Planning & Inverse Control"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Robotics"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# HeteroGenManip: Generalizable Manipulation For Heterogeneous Object Interactions

[Zotero 条目 YJJJPGKS](zotero://select/library/items/YJJJPGKS)

[DOI 原文](https://doi.org/10.48550/arxiv.2605.10201)

[来源网页](http://arxiv.org/abs/2605.10201)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Planning & Inverse Control/索引|05 Robot Learning/Planning & Inverse Control]]

## 原始摘要

Generalizable manipulation involving cross-type object interactions is a critical yet challenging capability in robotics. To reliably accomplish such tasks, robots must address two fundamental challenges: ``where to manipulate'' (contact point localization) and ``how to manipulate'' (subsequent interaction trajectory planning). Existing foundation-model-based approaches often adopt end-to-end learning that obscures the distinction between these stages, exacerbating error accumulation in long-horizon tasks. Furthermore, they typically rely on a single uniform model, which fails to capture the diverse, category-specific features required for heterogeneous objects. To overcome these limitations, we propose HeteroGenManip, a task-conditioned, two-stage framework designed to decouple initial grasp from complex interaction execution. First, Foundation-Correspondence-Guided Grasp module leverages structural priors to align the initial contact state, thereby significantly reducing the pose uncertainty of grasping. Subsequently, Multi-Foundation-Model Diffusion Policy (MFMDP) routes objects to category-specialized foundation models, integrating fine-grained geometric information with highly-variable part features via a dual-stream cross-attention mechanism. Experimental evaluations demonstrate that HeteroGenManip achieves robust intra-category shape and pose generalization. The framework achieves an average 31\% performance improvement in simulation tasks with broad type setting, alongside a 36.7\% gain across four real-world tasks with different interaction types.

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/FQRRJSLJ)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/A7P7CSZ8)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
