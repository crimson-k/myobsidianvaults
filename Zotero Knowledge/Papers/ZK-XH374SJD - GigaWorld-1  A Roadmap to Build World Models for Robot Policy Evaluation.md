---
type: "literature-note"
title: "GigaWorld-1: A Roadmap to Build World Models for Robot Policy Evaluation"
aliases: ["GigaWorld-1: A Roadmap to Build World Models for Robot Policy Evaluation"]
zotero_keys: ["XH374SJD"]
year: 2026
authors: ["GigaWorld Team", "Angyuan Ma", "Boyuan Wang", "Bohan Li", "Chaojun Ni", "Guo Li", "Guan Huang", "Guosheng Zhao", "Hao Li", "Hengtao Li", "Jingyu Liu", "Jiwen Lu", "Qiuping Deng", "Tingdong Yu", "Xuancheng Xu", "Xinyu Zhou", "Xiuwei Xu", "Xinze Chen", "Xiaofeng Wang", "Xiaoyu Tian", "Yang Wang", "Yifan Chang", "Yukun Zhou", "Yun Ye", "Zhenyu Wu", "Zhanqian Wu", "Zheng Zhu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2607.02642"
url: "http://arxiv.org/abs/2607.02642"
collections: ["05 Robot Learning/Simulation for Training & Evaluation"]
source_tags: ["Computer Science - Robotics"]
tags: ["zotero", "literature", "concept/世界模型评测与功能有效性", "concept-primary/世界模型评测与功能有效性"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# GigaWorld-1: A Roadmap to Build World Models for Robot Policy Evaluation

[Zotero 条目 XH374SJD](zotero://select/library/items/XH374SJD)

[DOI 原文](https://doi.org/10.48550/arxiv.2607.02642)

[来源网页](http://arxiv.org/abs/2607.02642)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Simulation for Training & Evaluation/索引|05 Robot Learning/Simulation for Training & Evaluation]]

概念地图：[[Zotero Knowledge/Concepts/世界模型评测与功能有效性|世界模型评测与功能有效性]]

补充阅读入口：[[Zotero Knowledge/Topics/07 Evaluation & Data/World Model Benchmarks/索引|07 Evaluation & Data/World Model Benchmarks]]

## 原始摘要

Evaluating embodied robot foundation models remains a critical bottleneck; unlike large language models efficiently assessed via digital benchmarks, robotic policies require slow, costly real-world rollouts limited by hardware and human supervision, which has driven interest in world models as surrogate policy evaluators, yet the key properties that make a world model reliable for policy assessment remain poorly understood. This work presents a systematic study of world models for robotic policy evaluation and introduces WMBench, a benchmark constructed from real-robot teleoperation data and matched policy rollouts covering diverse manipulation tasks to enable controlled comparisons across model families, action encodings, rollout horizons, and evaluation metrics. Using WMBench, we analyze 7 video world models, 4 action representation schemes, and over 324,000 simulated policy rollouts paired with real robot executions, further enriching our analysis with large-scale community submissions from the CVPR 2026 GigaBrain Challenge, curated synthetic trajectories, and a training videos spanning more than 12,000 hours. Our experiments deliver three core insights: evaluator quality is dominated by long-horizon, action-faithful rollout consistency rather than short-term visual realism; pretraining gains stem not only from data scale but from balancing general world knowledge with robot-specific controllability; and architectural choices including action encoding, memory design, and evaluatorfocused post-training strongly determine alignment with real-world robot behavior. Drawing on these results, we derive a practical design roadmap and realize it in GigaWorld-1, a world model specially optimized for policy evaluation, and we fully release our code, models, datasets, and toolkits to advance scalable evaluation research for embodied foundation models.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### 笔记

[在 Zotero 查看](zotero://select/library/items/4NCWDT9S)

**原文**

transferable physical priors matter more than raw scale in pretraining

**译文**

预训练中，可迁移的物理先验比原始规模更重要

**原文**

robot-specific data mainly improves embodiment fidelity, but introduces a sharper trade-off.

**译文**

机器人特定数据主要提升具身保真度，但也带来了更尖锐的权衡。

**原文**

The broader lesson is that evaluator-oriented training is inherently a balancing problem: robot data is useful for embodiment refinement, but broad physical data provides a better overall trade-off for reliable policy evaluation.

**译文**

更广泛的启示是，面向评估器的训练本质上是一个平衡问题：机器人数据有助于具身能力的精细化，而广泛的物理数据则为可靠的策略评估提供了更好的整体权衡。

**原文**

Action control must be injected through a spatially aligned interface.

**译文**

动作控制必须通过空间对齐的接口注入。

“The strongest result comes from channel-concatenated control maps” (Team 等, 2026, p. 13)

**原文**

reliable evaluators require persistent memory for long-horizon rollout.

**译文**

可靠的评估器需要用于长时程 rollout 的持久记忆。

### Comment: Project page: https://open-gigaai.github.io/giga-world-1/

[在 Zotero 查看](zotero://select/library/items/EQW8AWZQ)

Comment: Project page: https://open-gigaai.github.io/giga-world-1/

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/PXT9L64F)

[批注 TD938Y7W · 第 2 页](zotero://open-pdf/library/items/PXT9L64F?annotation=TD938Y7W&page=2)

> what matters in building world models for evaluating robot policies?

[批注 3PYIWDS6 · 第 2 页](zotero://open-pdf/library/items/PXT9L64F?annotation=3PYIWDS6&page=2)

> move the field from proof-of-concept demonstrations toward principled design rules

[批注 QURBS4HT · 第 2 页](zotero://open-pdf/library/items/PXT9L64F?annotation=QURBS4HT&page=2)

> First, how should one systematically evaluate whether a world model is a good policy evaluator, beyond generic video quality metrics? Second, how do pretraining and training data affect evaluator quality? Third, which architectural and algorithmic design choices most strongly influence evaluator reliability?

[批注 IHE9WPFE · 第 3 页](zotero://open-pdf/library/items/PXT9L64F?annotation=IHE9WPFE&page=3)

> systematic empirical study showing how evaluator reliability depends on metric design,  pretraining and data composition, and architectural choices such as action representation, memory, and reinforcement-learning-based post-training.

[批注 Z3VYWCBI · 第 5 页](zotero://open-pdf/library/items/PXT9L64F?annotation=Z3VYWCBI&page=5)

> these full long-horizon interaction episodes were subjected to meticulous human annotation based on a four-level ordinal scale,

[批注 YKANEX4C · 第 5 页](zotero://open-pdf/library/items/PXT9L64F?annotation=YKANEX4C&page=5)

> World Model as Evaluator Score (WMES):

[批注 28AVVVIL · 第 6 页](zotero://open-pdf/library/items/PXT9L64F?annotation=28AVVVIL&page=6)

> r diagnostic analysis, we select a subset of automatic metrics from WorldArena [96], keeping their original definitions and evaluation protocols whenever the metric is shared.

[批注 KYZ8G858 · 第 6 页](zotero://open-pdf/library/items/PXT9L64F?annotation=KYZ8G858&page=6)

> frame and representation fidelity; geometry, semantics, and interaction; and motion and long-horizon rollout.

[批注 WIPWH5LI · 第 7 页](zotero://open-pdf/library/items/PXT9L64F?annotation=WIPWH5LI&page=7)

> Qwen2.5-VL

[批注 M29XT8FB · 第 8 页](zotero://open-pdf/library/items/PXT9L64F?annotation=M29XT8FB&page=8)

> scalable VLM-assisted outcome annotation pipeline,

[批注 I8S5JXCI · 第 8 页](zotero://open-pdf/library/items/PXT9L64F?annotation=I8S5JXCI&page=8)

> visual and geometric fidelity dominate WMES prediction.

[批注 S9X98EF6 · 第 9 页](zotero://open-pdf/library/items/PXT9L64F?annotation=S9X98EF6&page=9)

> a world model’s ability to act as a reliable evaluator depends primarily on preserving recognizable subjects, viewpoint geometry, and semantic task information, rather than merely generating smooth motion

[批注 URAD6ZZ5 · 第 9 页](zotero://open-pdf/library/items/PXT9L64F?annotation=URAD6ZZ5&page=9)

> high-level semantic labels are insufficient if they do not capture whether the rollout preserves the policy-relevant geometric state.

[批注 7MTVL536 · 第 9 页](zotero://open-pdf/library/items/PXT9L64F?annotation=7MTVL536&page=9)

> degenerate metrics mislead evaluator ranking

[批注 T9NVSYKQ · 第 9 页](zotero://open-pdf/library/items/PXT9L64F?annotation=T9NVSYKQ&page=9)

> evaluator quality must be assessed under long-horizon rollout, not single-step video generation.

[批注 7AEWN8MX · 第 9 页](zotero://open-pdf/library/items/PXT9L64F?annotation=7AEWN8MX&page=9)

> assess long-horizon quality chunk-by-chunk over 40 seconds using PSNR for multi-view reconstruction and FID/FVD for perceptual and temporal quality.

[批注 ZYJVEVHU · 第 9 页](zotero://open-pdf/library/items/PXT9L64F?annotation=ZYJVEVHU&page=9)

> outcome-centric supervision is essential for scalable VLM evaluation.

[批注 YWI99HA6 · 第 10 页](zotero://open-pdf/library/items/PXT9L64F?annotation=YWI99HA6&page=10)

> VLM evaluators achieve near-perfect agreement with human ratings

[批注 88LI87P4 · 第 11 页](zotero://open-pdf/library/items/PXT9L64F?annotation=88LI87P4&page=11)

> evaluator quality depends not only on scale, but also on whether the pretrained model contains transferable physical priors and whether post-training preserves them under robot-conditioned rollout.

[批注 GL2WIZHK · 第 11 页](zotero://open-pdf/library/items/PXT9L64F?annotation=GL2WIZHK&page=11)

> transferable physical priors matter more than raw scale in pretraining

[批注 XPBDPT2L · 第 11 页](zotero://open-pdf/library/items/PXT9L64F?annotation=XPBDPT2L&page=11)

> whether evaluator quality comes primarily from parameter count, or from the compatibility between pretrained priors and robot-conditioned rollout.

[批注 VD6TM4ZV · 第 12 页](zotero://open-pdf/library/items/PXT9L64F?annotation=VD6TM4ZV&page=12)

> broad physical videos provide the best overall trade-off for evaluator training

[批注 QYEQRX7E · 第 12 页](zotero://open-pdf/library/items/PXT9L64F?annotation=QYEQRX7E&page=12)

> general physical videos reinforce the underlying world knowledge needed to model such interactions

[批注 CRYSVEAX · 第 12 页](zotero://open-pdf/library/items/PXT9L64F?annotation=CRYSVEAX&page=12)

> robot-specific data mainly improves embodiment fidelity, but introduces a sharper trade-off.

[批注 CGGRL9MG · 第 12 页](zotero://open-pdf/library/items/PXT9L64F?annotation=CGGRL9MG&page=12)

> The broader lesson is that evaluator-oriented training is inherently a balancing problem: robot data is useful for embodiment refinement, but broad physical data provides a better overall trade-off for reliable policy evaluation.

[批注 U8YURR6D · 第 13 页](zotero://open-pdf/library/items/PXT9L64F?annotation=U8YURR6D&page=13)

> two design axes that directly determine whether a world model can support faithful policy assessment: the action-control interface and long-horizon memory.

[批注 9YZC5I9E · 第 13 页](zotero://open-pdf/library/items/PXT9L64F?annotation=9YZC5I9E&page=13)

> the action-control interface and long-horizon memory.

[批注 F977783H · 第 13 页](zotero://open-pdf/library/items/PXT9L64F?annotation=F977783H&page=13)

> Action control must be injected through a spatially aligned interface.

[批注 STT4EIN5 · 第 13 页](zotero://open-pdf/library/items/PXT9L64F?annotation=STT4EIN5&page=13)

> The strongest result comes from channel-concatenated control maps

[批注 5CVEADBL · 第 13 页](zotero://open-pdf/library/items/PXT9L64F?annotation=5CVEADBL&page=13)

> reliable evaluators require persistent memory for long-horizon rollout.

[批注 TF6TWJ7G · 第 14 页](zotero://open-pdf/library/items/PXT9L64F?annotation=TF6TWJ7G&page=14)

> GigaWorld-1 is built from Wan [109] backbones of two scales, [1.3B] and [5B]

[批注 KRDSDVSJ · 第 15 页](zotero://open-pdf/library/items/PXT9L64F?annotation=KRDSDVSJ&page=15)

> physical videos

[批注 SQA84HRN · 第 15 页](zotero://open-pdf/library/items/PXT9L64F?annotation=SQA84HRN&page=15)

> ource robot + egocentric + Giga-collected data broad physical priors with embodiment diversity Data curation quality + motion + distribution filtering removes noisy, static, and misaligned samples Structured supervision semantic masks + depth + fast-slow captions

[批注 LPN4ITU4 · 第 15 页](zotero://open-pdf/library/items/PXT9L64F?annotation=LPN4ITU4&page=15)

> quality + motion + distribution filtering

[批注 DCM4ZU9X · 第 15 页](zotero://open-pdf/library/items/PXT9L64F?annotation=DCM4ZU9X&page=15)

> semantic masks + depth + fast-slow captions

[批注 MTTZDRXA · 第 15 页](zotero://open-pdf/library/items/PXT9L64F?annotation=MTTZDRXA&page=15)

> explicit pixel-aligned representation

[批注 YUJRB5UJ · 第 15 页](zotero://open-pdf/library/items/PXT9L64F?annotation=YUJRB5UJ&page=15)

> memory-augmented rollout

[批注 999XX7BQ · 第 17 页](zotero://open-pdf/library/items/PXT9L64F?annotation=999XX7BQ&page=17)

> Depth Anything 3 (DA3)

[批注 UYKSNYRC · 第 18 页](zotero://open-pdf/library/items/PXT9L64F?annotation=UYKSNYRC&page=18)

> reformulate world generation as an autoregressive video-continuation problem

[批注 GMHRVPGM · 第 26 页](zotero://open-pdf/library/items/PXT9L64F?annotation=GMHRVPGM&page=26)

> PSNR (↑) and FID (↓)

[批注 J6IUZ7XP · 第 27 页](zotero://open-pdf/library/items/PXT9L64F?annotation=J6IUZ7XP&page=27)

> gaWorld-1 successfully handles changes in container color, object contents (e.g., different food types), and table textures without geometry collapse

[批注 R542J99S · 第 27 页](zotero://open-pdf/library/items/PXT9L64F?annotation=R542J99S&page=27)

> the model accurately simulates both successful placements and failures

[批注 FJDB6RP2 · 第 30 页](zotero://open-pdf/library/items/PXT9L64F?annotation=FJDB6RP2&page=30)

> Recent community efforts on omni world models, such as Cosmos-3 [1], suggest that absorbing richer multimodal training data may improve both controllability and physical grounding

[批注 9X2ZK7BL · 第 30 页](zotero://open-pdf/library/items/PXT9L64F?annotation=9X2ZK7BL&page=30)

> scaling model parameters remains an important direction

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
