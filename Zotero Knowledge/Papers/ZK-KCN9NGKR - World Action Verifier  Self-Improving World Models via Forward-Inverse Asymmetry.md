---
type: "literature-note"
title: "World Action Verifier: Self-Improving World Models via Forward-Inverse Asymmetry"
aliases: ["World Action Verifier: Self-Improving World Models via Forward-Inverse Asymmetry"]
zotero_keys: ["KCN9NGKR"]
year: 2026
authors: ["Yuejiang Liu", "Fan Feng", "Lingjing Kong", "Weifeng Lu", "Jinzhou Tang", "Kun Zhang", "Kevin Murphy", "Chelsea Finn", "Yilun Du"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2604.01985"
url: "http://arxiv.org/abs/2604.01985"
collections: ["06 Alignment & Reliability/Physics Grounding & Rollout Verification"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Machine Learning", "Computer Science - Robotics"]
tags: ["zotero", "literature", "concept/物理一致性与表征对齐", "concept-primary/物理一致性与表征对齐"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# World Action Verifier: Self-Improving World Models via Forward-Inverse Asymmetry

[Zotero 条目 KCN9NGKR](zotero://select/library/items/KCN9NGKR)

[DOI 原文](https://doi.org/10.48550/arxiv.2604.01985)

[来源网页](http://arxiv.org/abs/2604.01985)

## 主题与知识联系

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Physics Grounding & Rollout Verification/索引|06 Alignment & Reliability/Physics Grounding & Rollout Verification]]

概念地图：[[Zotero Knowledge/Concepts/物理一致性与表征对齐|物理一致性与表征对齐]]

## 原始摘要

General-purpose world models promise scalable policy evaluation, optimization, and planning, yet achieving the required level of robustness remains challenging. Unlike policy learning which primarily focuses on optimal actions, a world model needs to be reliable over a vast space of suboptimal actions, which are often underrepresented in action-labeled robot interactions. To address this challenge, we propose World Action Verifier (WAV), a framework that enables world models to identify their own prediction errors and self-improve. The key idea is to decompose action-conditioned state prediction into two independently verifiable factors: state plausibility and action reachability. We show that verifying these factors is significantly more tractable than direct forward prediction due to two underlying asymmetries: the broader availability of action-free data and the lower dimensionality of action-relevant features. Leveraging these asymmetries, we augment a world model with (i) a diverse subgoal generator obtained from video corpora and (ii) a sparse inverse model that infers actions from a subset of state features. By enforcing cycle consistency among proposed subgoals, inferred actions, and forward rollouts, WAV provides an effective verification mechanism in under-explored regimes, where existing methods often fail. Across nine tasks spanning MiniGrid, RoboMimic, and ManiSkill, our method achieves 2x higher sample efficiency while improving downstream policy performance by over 22%.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project Website: https://world-action-verifier.github.io

[在 Zotero 查看](zotero://select/library/items/EIV2E3KG)

Comment: Project Website: https://world-action-verifier.github.io

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/54CV5FBM)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/UGK6T2VB)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
