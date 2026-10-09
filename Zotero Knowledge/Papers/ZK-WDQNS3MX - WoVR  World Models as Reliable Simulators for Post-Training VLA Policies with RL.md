---
type: "literature-note"
title: "WoVR: World Models as Reliable Simulators for Post-Training VLA Policies with RL"
aliases: ["WoVR: World Models as Reliable Simulators for Post-Training VLA Policies with RL"]
zotero_keys: ["WDQNS3MX"]
year: 2026
authors: ["Zhennan Jiang", "Shangqing Zhou", "Yutong Jiang", "Zefang Huang", "Mingjie Wei", "Yuhui Chen", "Tianxing Zhou", "Zhen Guo", "Hao Lin", "Quanlu Zhang", "Yu Wang", "Haoran Li", "Chao Yu", "Dongbin Zhao"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2602.13977"
url: "https://arxiv.org/abs/2602.13977"
collections: ["05 Robot Learning/Simulation for Training & Evaluation"]
source_tags: ["Artificial Intelligence (cs.AI)", "FOS: Computer and information sciences", "Robotics (cs.RO)", "notion"]
tags: ["zotero", "literature", "highlight", "concept/想象中的规划与强化学习", "concept-primary/想象中的规划与强化学习"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# WoVR: World Models as Reliable Simulators for Post-Training VLA Policies with RL

[Zotero 条目 WDQNS3MX](zotero://select/library/items/WDQNS3MX)

[DOI 原文](https://doi.org/10.48550/arxiv.2602.13977)

[来源网页](https://arxiv.org/abs/2602.13977)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Simulation for Training & Evaluation/索引|05 Robot Learning/Simulation for Training & Evaluation]]

概念地图：[[Zotero Knowledge/Concepts/想象中的规划与强化学习|想象中的规划与强化学习]]

## 原始摘要

Reinforcement learning (RL) promises to unlock capabilities beyond imitation learning for Vision–Language–Action (VLA) models, but its requirement for massive real-world interaction prevents direct deployment on physical robots. Recent work attempts to use learned world models as simulators for policy optimization, yet closed-loop imagined rollouts inevitably suffer from hallucination and long-horizon error accumulation. Such errors do not merely degrade visual fidelity—they corrupt the optimization signal, encouraging policies to exploit model inaccuracies rather than genuine task progress. We propose WoVR, a reliable world-model-based reinforcement learning framework for post-training VLA policies. Instead of assuming a faithful world model, WoVR explicitly regulates how RL interacts with imperfect imagined dynamics. It improves rollout stability through a controllable action-conditioned video world model, reshapes imagined interaction to reduce effective error depth via Keyframe-Initialized Rollouts, and maintains policy–simulator alignment through World Model-Policy co-evolution. Extensive experiments on LIBERO benchmarks and real-world robotic manipulation demonstrate that WoVR enables stable long-horizon imagined rollouts and effective policy optimization, improving average LIBERO success from 39.95% to 69.2% (+29.3 points) and real-robot success from 61.7% to 91.7% (+30.0 points). These results show that learned world models can serve as practical simulators for reinforcement learning when hallucination is explicitly controlled.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/7V5FLVIA)

## Other
21pages, 8 figures

## 附件与批注

### Notion

[在 Zotero 查看附件](zotero://select/library/items/3Y2T2NDQ)

附件笔记：

## Do not modify or delete!

This link attachment serves as a reference for
[Notero](https://github.com/dvanoni/notero)
so that it can properly update the Notion page for this item.

Last synced: 2026/5/27 20:11:33

### PDF

[打开 PDF](zotero://open-pdf/library/items/LSGW9TSW)

[批注 ZXD67528 · 第 1 页](zotero://open-pdf/library/items/LSGW9TSW?annotation=ZXD67528&page=1)

> use learned world models as simulators for policy optimization, yet closed-loop imagined rollouts inevitably suffer from hallucination and long-horizon error accumulation

[批注 M2SN7U9J · 第 1 页](zotero://open-pdf/library/items/LSGW9TSW?annotation=M2SN7U9J&page=1)

> WoVR explicitly regulates how RL interacts with imperfect imagined dynamics

[批注 A9HI27XF · 第 3 页](zotero://open-pdf/library/items/LSGW9TSW?annotation=A9HI27XF&page=3)

> prior works adapt pretrained video models into action-conditioned world models using projected end-effector position [41, 42], AdaLN-based frame-wise action injection [43, 22, 44, 45], cross-attention [46, 47], and MoE-based conditioning

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-4MHFRDYK - Ctrl-World  A Controllable Generative World Model for Robot Manipulation|Ctrl-World: A Controllable Generative World Model for Robot Manipulation]] — 中关联；共同研究内容：动作条件预测、想象与模型式强化学习、机器人操作。
- [[Zotero Knowledge/Papers/ZK-F8CLH377 - What Can RL Bring to VLA Generalization  An Empirical Study|What Can RL Bring to VLA Generalization? An Empirical Study]] — 中关联；共同研究内容：VLA 策略、基准与数据合成、想象与模型式强化学习。
- [[Zotero Knowledge/Papers/ZK-3TP5FDZ4 - WorldGym  World Model as An Environment for Policy Evaluation|WorldGym: World Model as An Environment for Policy Evaluation]] — 中关联；共同研究内容：VLA 策略、动作条件预测、策略评测与模拟可靠性。

<!-- content-relations:end -->
