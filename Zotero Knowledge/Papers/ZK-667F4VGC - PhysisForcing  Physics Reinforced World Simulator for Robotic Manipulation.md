---
type: "literature-note"
title: "PhysisForcing: Physics Reinforced World Simulator for Robotic Manipulation"
aliases: ["PhysisForcing: Physics Reinforced World Simulator for Robotic Manipulation"]
zotero_keys: ["667F4VGC"]
year: 2026
authors: ["Peiwen Zhang", "Yufan Deng", "Shangkun Sun", "Juncheng Ma", "Duomin Wang", "Jonas Du", "Zilin Pan", "Ye Huang", "Hao Liang", "Songyan Huang", "Ruihua Zhang", "Enze Xie", "Ming-Yu Liu", "Daquan Zhou"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2606.28128"
url: "http://arxiv.org/abs/2606.28128"
collections: ["06 Alignment & Reliability/Physics Grounding & Rollout Verification"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Robotics"]
tags: ["zotero", "literature", "highlight", "concept/物理一致性与表征对齐", "concept-primary/物理一致性与表征对齐"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# PhysisForcing: Physics Reinforced World Simulator for Robotic Manipulation

[Zotero 条目 667F4VGC](zotero://select/library/items/667F4VGC)

[DOI 原文](https://doi.org/10.48550/arxiv.2606.28128)

[来源网页](http://arxiv.org/abs/2606.28128)

## 主题与知识联系

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Physics Grounding & Rollout Verification/索引|06 Alignment & Reliability/Physics Grounding & Rollout Verification]]

概念地图：[[Zotero Knowledge/Concepts/物理一致性与表征对齐|物理一致性与表征对齐]]

补充阅读入口：[[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

## 原始摘要

Video generation models have emerged as a promising paradigm for embodied world simulation. However, both general-domain video generators and robot-specific data fine-tuned models can still produce physically implausible manipulations, including discontinuous motion trajectories and inconsistent robot-object interactions, which limits their reliability as world simulators. Through extensive experiments, we find that such physical instability mainly arises from two factors: deformation of moving objects and implausible spatio-temporal correlations among interacting entities, particularly during contact. Building on this observation, we propose PhysisForcing, a scalable training framework that strengthens physical consistency by focusing supervision on physics-informative regions through joint optimization of pixel-level and semantic-level features. The framework consists of a pixel-level trajectory alignment loss, which supervises DiT features using reference point trajectories, and a semantic-level relational alignment loss, which aligns DiT features with inter-region relations extracted from a frozen video understanding encoder. Extensive experiments on R-Bench, PAI-Bench, and EZS-Bench show that PhysisForcing consistently improves embodied video generation over strong baselines, improving the Wan2.2-I2V-A14B and Cosmos3-Nano base models on R-Bench by 22.3\% and 9.2\% (7.1\% and 3.7\% over vanilla finetuning), with the Cosmos3-Nano variant attaining the best overall score. Beyond generation, as a world model under the WorldArena action-planner protocol it raises the closed-loop success rate from 16.0\% to 24.0\% and further improves downstream policy success, indicating that physically aligned video models yield stronger representations for robotic manipulation.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Github: https://github.com/DAGroup-PKU/PhysisForcing Project website: https://dagroup-pku.github.io/PhysisForci

[在 Zotero 查看](zotero://select/library/items/DNZXFC2F)

Comment: Github: https://github.com/DAGroup-PKU/PhysisForcing Project website: https://dagroup-pku.github.io/PhysisForcing.github.io/#

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/XSQNDAYD)

[批注 TDVC2X6K · 第 1 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=TDVC2X6K&page=1)

> deformation of moving objects and implausible spatio-temporal correlations among interacting entities,

[批注 23SBG9HY · 第 1 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=23SBG9HY&page=1)

> a scalable training framework that strengthens physical consistency by focusing supervision on physics-informative regions through joint optimization of pixel-level and semantic-level features

[批注 HFV5DDU6 · 第 1 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=HFV5DDU6&page=1)

> Wan2.2-I2V-A14B and Cosmos3-Nano

[批注 MSZXMIPC · 第 2 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=MSZXMIPC&page=2)

> At the semantic level, object relations should evolve according to the interaction semantics

[批注 TVMLX2F4 · 第 2 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=TVMLX2F4&page=2)

> first identifies physics2 informative regions

[批注 FNJ55UDR · 第 3 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=FNJ55UDR&page=3)

> two complementary alignment losses to these regions during backbone training.

[批注 2HR4U3RZ · 第 3 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=2HR4U3RZ&page=3)

> pixel-level physics alignment module uses point tracking

[批注 HMBY5LE4 · 第 3 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=HMBY5LE4&page=3)

> emantic-level physics alignment module instead aligns the pairwise token-similarity matrix of the DiT feature with that of a frozen video understanding encoder

[批注 EVHBARQ2 · 第 5 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=EVHBARQ2&page=5)

> off-the-shelf point tracker

[批注 7R9X8QRA · 第 5 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=7R9X8QRA&page=5)

> depth-aware foreground weight

[批注 PLURHCZH · 第 5 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=PLURHCZH&page=5)

> a pixel-level trajectory alignment loss

[批注 84VVQDJB · 第 5 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=84VVQDJB&page=5)

> an intermediate DiT block (i.e., l is a middle layer of the DiT, which we empirically find to carry the most informative motion and structure cues

[批注 XDDM6L2R · 第 5 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=XDDM6L2R&page=5)

> similarity map

[批注 HGUHHPI3 · 第 6 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=HGUHHPI3&page=6)

> CoTracker3

[批注 JYEGXUUX · 第 6 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=JYEGXUUX&page=6)

> masked mean squared error

[批注 CFQQPQUG · 第 6 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=CFQQPQUG&page=6)

> frozen self-supervised video understanding encoders

[批注 K35PZQP3 · 第 6 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=K35PZQP3&page=6)

> project it into the same representation space with a lightweight MLP

[批注 EB55UXZ7 · 第 6 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=EB55UXZ7&page=6)

> spatio-temporal tokens from both representations:

[批注 7QMQ8H56 · 第 6 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=7QMQ8H56&page=6)

> DiT-side and encoder-side relational matrices

[批注 I66DZAIE · 第 6 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=I66DZAIE&page=6)

> semantic-level physics alignment loss

[批注 KYJMCV58 · 第 6 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=KYJMCV58&page=6)

> PhysisForcing is applied during the fine-tuning of a pre-trained DiT-based video generation backbone [

[批注 LVW88MXT · 第 14 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=LVW88MXT&page=14)

> we take the hidden feature of a single DiT block (block 20, width 5120), map it into V-JEPA 2’s feature space with a lightweight MLP, and trilinearly resample it from its native DiT patch grid to the same 32×16×16 grid,

[批注 NBIPII9E · 第 14 页](zotero://open-pdf/library/items/XSQNDAYD?annotation=NBIPII9E&page=14)

> CoTracker3 [25] in its offline variant

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/AUZ3U3VP)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-IX4MEYSF - WorldArena  A Unified Benchmark for Evaluating Perception and Functional Utility of E|WorldArena: A Unified Benchmark for Evaluating Perception and Functional Utility of Embodied World Models]] — 强关联；本篇摘要提到模型 WorldArena（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-NUQYHFKH - ABot-PhysWorld  Interactive World Foundation Model for Robotic Manipulation with Phys|ABot-PhysWorld: Interactive World Foundation Model for Robotic Manipulation with Physics Alignment]] — 中关联；共同研究内容：扩散生成架构、机器人操作、物理可信度。

<!-- content-relations:end -->
