---
type: "literature-note"
title: "Masked Visual Actions for Unified World Modeling"
aliases: ["Masked Visual Actions for Unified World Modeling"]
zotero_keys: ["YFP6L7BZ"]
year: 2026
authors: ["Hadi Alzayer", "Wenlong Huang", "Haonan Chen", "Christopher Luey", "Lvmin Zhang", "Maneesh Agrawala", "Gordon Wetzstein", "Li Fei-Fei", "Yilun Du", "Jiajun Wu", "Jia-Bin Huang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2607.19343"
url: "http://arxiv.org/abs/2607.19343"
collections: ["04 World Models/Video-Based Interactive Simulation"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Robotics"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Masked Visual Actions for Unified World Modeling

[Zotero 条目 YFP6L7BZ](zotero://select/library/items/YFP6L7BZ)

[DOI 原文](https://doi.org/10.48550/arxiv.2607.19343)

[来源网页](http://arxiv.org/abs/2607.19343)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

概念地图：[[Zotero Knowledge/Concepts/动作接口与逆动力学|动作接口与逆动力学]]

## 原始摘要

Video models absorb rich priors over how the visual world moves, interacts, and responds to contact, making them promising substrates for robotic world modeling. The central challenge is how to communicate action to such models in a form aligned with the visual space in which they learned these interaction priors, yet still grounded in physical manipulation. We introduce Masked Visual Actions, a pixel-space control interface that expresses action as a partially revealed trajectory of an arbitrary entity in a video. Revealing robot motion makes the model act as a forward dynamics model that predicts the scene's response to low-level robot actions, while revealing desired object motion makes the same model recover robot behavior consistent with that outcome. Finetuned with only 15 hours of masked examples from real videos and simulation, a single checkpoint achieves strong visual fidelity and controllability across diverse scenes and multiple embodiments. In downstream manipulation settings, the model produces imagined rollouts whose outcomes correlate with real-world execution for policy evaluation, improves decision making by ranking candidate futures in model-based planning, and supports inverse modeling by synthesizing robot motion from desired object motion.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project webpage: https://masked-visual-actions.github.io

[在 Zotero 查看](zotero://select/library/items/574MF8BA)

Comment: Project webpage: https://masked-visual-actions.github.io

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/IJM4P3NT)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/AMFX5U8F)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
