---
type: "literature-note"
title: "MiraBench: Evaluating Action-Conditioned Reliability in Robotic World Models"
aliases: ["MiraBench: Evaluating Action-Conditioned Reliability in Robotic World Models"]
zotero_keys: ["IV4EJTU5"]
year: 2026
authors: ["Tianzhuo Yang", "Zihan Shen", "Zirui Mi", "Zhaoyi Zhang", "Jiayi Zhou", "Jiaming Ji", "Juntao Dai", "Jiawei Chen", "Boyuan Chen", "Yaodong Yang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2605.29360"
url: "http://arxiv.org/abs/2605.29360"
collections: ["07 Evaluation & Data/World Model Benchmarks"]
source_tags: ["Computer Science - Artificial Intelligence"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# MiraBench: Evaluating Action-Conditioned Reliability in Robotic World Models

[Zotero 条目 IV4EJTU5](zotero://select/library/items/IV4EJTU5)

[DOI 原文](https://doi.org/10.48550/arxiv.2605.29360)

[来源网页](http://arxiv.org/abs/2605.29360)

## 主题与知识联系

- [[Zotero Knowledge/Topics/07 Evaluation & Data/World Model Benchmarks/索引|07 Evaluation & Data/World Model Benchmarks]]

概念地图：[[Zotero Knowledge/Concepts/世界模型评测与功能有效性|世界模型评测与功能有效性]]

## 原始摘要

Action-conditioned world models are increasingly used as scalable simulators for robot learning, yet current evaluations provide limited evidence that their predictions are reliable under the actions they condition on. Existing benchmarks largely emphasize visual fidelity, leaving unclear whether predicted futures are physically plausible, faithful to commanded actions, and calibrated to failure when actions should not succeed. We introduce \textsc{MiraBench}, a hierarchical benchmark that defines \emph{action-conditioned reliability} as a core evaluation target for robotic world models. MiraBench decomposes this target into three progressively demanding levels: \emph{Physics Adherence}, which evaluates reference-free physical consistency; \emph{Action-Following Fidelity}, which measures whether predictions respect task-relevant action inputs; and \emph{Optimism Bias Detection}, which probes the tendency to predict successful outcomes under failure-inducing actions. To support this evaluation, we curate a human-annotated corpus with over 16,000 judgments across tasks, failure categories, and leading world models. We evaluate 12 representative model configurations spanning vector-conditioned robotic world models, text-conditioned generative world models, open-weight systems, closed-source systems, and multiple model scales. Across this broad model landscape, MiraBench reveals three central findings: visual fidelity is a poor proxy for action fidelity; increasing model scale does not reliably improve action following; and optimism bias is pervasive across current systems. By shifting evaluation from appearance to action-conditioned reliability, MiraBench provides a diagnostic foundation for assessing and improving robotic world models as faithful simulators.

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/METUWQRH)

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/CZV5D8QG)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
