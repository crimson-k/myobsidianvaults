---
type: "literature-note"
title: "Pelican-Unify 1.0: A Unified Embodied Intelligence Model for Understanding, Reasoning, Imagination and Action"
aliases: ["Pelican-Unify 1.0: A Unified Embodied Intelligence Model for Understanding, Reasoning, Imagination and Action"]
zotero_keys: ["G4MM75HL"]
year: 2026
authors: ["Yi Zhang", "Yinda Chen", "Che Liu", "Zeyuan Ding", "Jin Xu", "Shilong Zou", "Junwei Liao", "Jiayu Hu", "Xiancong Ren", "Xiaopeng Zhang", "Yechi Liu", "Haoyuan Shi", "Zecong Tang", "Haosong Sun", "Renwen Cui", "Kuishu Wu", "Wenhai Liu", "Yang Xu", "Yingji Zhang", "Yidong Wang", "Senkang Hu", "Jinpeng Lu", "Nga Teng Chan", "Yechen Wu", "Zeting Liu", "Xianzhou Hou", "Yong Dai", "Jian Tang", "Xiaozhu Ju"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2605.15153"
url: "https://arxiv.org/abs/2605.15153"
collections: ["05 Robot Learning/World-Action Models"]
source_tags: ["Artificial Intelligence (cs.AI)", "FOS: Computer and information sciences", "Robotics (cs.RO)", "notion"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Pelican-Unify 1.0: A Unified Embodied Intelligence Model for Understanding, Reasoning, Imagination and Action

[Zotero 条目 G4MM75HL](zotero://select/library/items/G4MM75HL)

[DOI 原文](https://doi.org/10.48550/arxiv.2605.15153)

[来源网页](https://arxiv.org/abs/2605.15153)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/World-Action Models/索引|05 Robot Learning/World-Action Models]]

## 原始摘要

We present Pelican-Unify 1.0, the first embodied foundation model trained according to the principle of unification. Pelican-Unify 1.0 uses a single VLM as a unified understanding module, mapping scenes, instructions, visual contexts, and action histories into a shared semantic space. The same VLM also serves as a unified reasoning module, autoregressively producing task-, action-, and future-oriented chains of thought in a single forward pass and projecting the final hidden state into a dense latent variable. A Unified Future Generator (UFG) then conditions on this latent variable and jointly generates future videos and future actions through two modality-specific output heads within the same denoising process. The language, video, and action losses are all backpropagated into the shared representation, enabling the model to jointly optimize understanding, reasoning, imagination, and action during training, rather than training three isolated expert systems.
 Experiments demonstrate that unification does not imply compromise. With a single checkpoint, Pelican-Unify 1.0 achieves strong performance across all three capabilities: 64.7 on eight VLM benchmarks, the best among comparable-scale models; 66.03 on WorldArena, ranking first; and 93.5 on RoboTwin, the second-best average among compared action methods. These results show that the unified paradigm succeeds in preserving specialist strength while bringing understanding, reasoning, imagination, and action into one model.

## 附件与批注

### Notion

[在 Zotero 查看附件](zotero://select/library/items/K3DH5RRQ)

附件笔记：

## Do not modify or delete!

This link attachment serves as a reference for
[Notero](https://github.com/dvanoni/notero)
so that it can properly update the Notion page for this item.

Last synced: 2026/5/27 20:11:35

### PDF

[打开 PDF](zotero://open-pdf/library/items/W4D94A4U)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
