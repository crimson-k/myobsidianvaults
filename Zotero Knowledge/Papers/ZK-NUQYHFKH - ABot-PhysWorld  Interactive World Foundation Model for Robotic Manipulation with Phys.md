---
type: "literature-note"
title: "ABot-PhysWorld: Interactive World Foundation Model for Robotic Manipulation with Physics Alignment"
aliases: ["ABot-PhysWorld: Interactive World Foundation Model for Robotic Manipulation with Physics Alignment"]
zotero_keys: ["NUQYHFKH"]
year: 2026
authors: ["Yuzhi Chen", "Ronghan Chen", "Dongjie Huo", "Yandan Yang", "Dekang Qi", "Haoyun Liu", "Tong Lin", "Shuang Zeng", "Junjin Xiao", "Xinyuan Chang", "Feng Xiong", "Xing Wei", "Zhiheng Ma", "Mu Xu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2603.23376"
url: "https://arxiv.org/abs/2603.23376"
collections: ["04 World Models/Video-Based Interactive Simulation"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences", "Robotics (cs.RO)", "notion"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# ABot-PhysWorld: Interactive World Foundation Model for Robotic Manipulation with Physics Alignment

[Zotero 条目 NUQYHFKH](zotero://select/library/items/NUQYHFKH)

[DOI 原文](https://doi.org/10.48550/arxiv.2603.23376)

[来源网页](https://arxiv.org/abs/2603.23376)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

补充阅读入口：[[Zotero Knowledge/Topics/06 Alignment & Reliability/Physics Grounding & Rollout Verification/索引|06 Alignment & Reliability/Physics Grounding & Rollout Verification]]

## 原始摘要

Video-based world models offer a powerful paradigm for embodied simulation and planning, yet state-of-the-art models often generate physically implausible manipulations—such as object penetration and anti-gravity motion—due to training on generic visual data and likelihood-based objectives that ignore physical laws. We present ABot-PhysWorld, a 14B Diffusion Transformer model that generates visually realistic, physically plausible, and action-controllable videos. Built on a curated dataset of three million manipulation clips with physics-aware annotation, it uses a novel DPO-based post-training framework with decoupled discriminators to suppress unphysical behaviors while preserving visual quality. A parallel context block enables precise spatial action injection for cross-embodiment control. To better evaluate generalization, we introduce EZSbench, the first training-independent embodied zero-shot benchmark combining real and synthetic unseen robot-task-scene combinations. It employs a decoupled protocol to separately assess physical realism and action alignment. ABot-PhysWorld achieves new state-of-the-art performance on PBench and EZSbench, surpassing Veo 3.1 and Sora v2 Pro in physical plausibility and trajectory consistency. We will release EZSbench to promote standardized evaluation in embodied video generation.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/QXPHWXUK)

## Other

 Code: https://github.com/amap-cvlab/ABot-PhysWorld.git

## 附件与批注

### Notion

[在 Zotero 查看附件](zotero://select/library/items/IUHIM2DN)

附件笔记：

## Do not modify or delete!

This link attachment serves as a reference for
[Notero](https://github.com/dvanoni/notero)
so that it can properly update the Notion page for this item.

Last synced: 2026/5/27 20:13:40

{}

### PDF

[打开 PDF](zotero://open-pdf/library/items/NC6X4K2I)

[批注 QE8DC5Q4 · 第 8 页](zotero://open-pdf/library/items/NC6X4K2I?annotation=QE8DC5Q4&page=8)

> 3.3 Action-Conditioned Video Generation

[批注 YSJFWE4I · 第 8 页](zotero://open-pdf/library/items/NC6X4K2I?annotation=YSJFWE4I&page=8)

> convert discrete action commands into spatially structured action maps and inject them through parallel context blocks that preserve the backbone’s pre-trained physical knowledge.

[批注 7BSU6WJN · 第 8 页](zotero://open-pdf/library/items/NC6X4K2I?annotation=7BSU6WJN&page=8)

> we clone selective blocks from the main DiT [39] to form a parallel set of context blocks that process the action maps [22]. The output of each context block is projected via zero-initialized convolution layers and added residually to the corresponding main DiT block:

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-6AVL3P5T - MIND-V  Hierarchical World Model for Long-Horizon Robotic Manipulation with RL-based |MIND-V: Hierarchical World Model for Long-Horizon Robotic Manipulation with RL-based Physical Alignment]] — 中关联；共同研究内容：基准与数据合成、机器人操作、物理可信度。
- [[Zotero Knowledge/Papers/ZK-667F4VGC - PhysisForcing  Physics Reinforced World Simulator for Robotic Manipulation|PhysisForcing: Physics Reinforced World Simulator for Robotic Manipulation]] — 中关联；共同研究内容：扩散生成架构、机器人操作、物理可信度。

<!-- content-relations:end -->
