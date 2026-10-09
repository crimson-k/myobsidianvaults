---
type: "literature-note"
title: "Causal Forcing++: Scalable Few-Step Autoregressive Diffusion Distillation for Real-Time Interactive Video Generation"
aliases: ["Causal Forcing++: Scalable Few-Step Autoregressive Diffusion Distillation for Real-Time Interactive Video Generation"]
zotero_keys: ["YLGPQLIA", "MEILYEYD"]
year: 2026
authors: ["Min Zhao", "Hongzhou Zhu", "Kaiwen Zheng", "Zihan Zhou", "Bokai Yan", "Xinyuan Li", "Xiao Yang", "Chongxuan Li", "Jun Zhu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2605.15141"
url: "http://arxiv.org/abs/2605.15141"
collections: ["03 Visual Generation/General Video Generation"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature", "concept/视频生成的因果化与流式推理", "concept-primary/视频生成的因果化与流式推理"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Causal Forcing++: Scalable Few-Step Autoregressive Diffusion Distillation for Real-Time Interactive Video Generation

[Zotero 条目 YLGPQLIA](zotero://select/library/items/YLGPQLIA)

[DOI 原文](https://doi.org/10.48550/arxiv.2605.15141)

[来源网页](http://arxiv.org/abs/2605.15141)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/General Video Generation/索引|03 Visual Generation/General Video Generation]]

概念地图：[[Zotero Knowledge/Concepts/视频生成的因果化与流式推理|视频生成的因果化与流式推理]]

## 原始摘要

Real-time interactive video generation requires low-latency, streaming, and controllable rollout. Existing autoregressive (AR) diffusion distillation methods have achieved strong results in the chunk-wise 4-step regime by distilling bidirectional base models into few-step AR students, but they remain limited by coarse response granularity and non-negligible sampling latency. In this paper, we study a more aggressive setting: frame-wise autoregression with only 1--2 sampling steps. In this regime, we identify the initialization of a few-step AR student as the key bottleneck: existing strategies are either target-misaligned, incapable of few-step generation, or too costly to scale. We propose \textbf{Causal Forcing++}, a principled and scalable pipeline that uses \emph{causal consistency distillation} (causal CD) for few-step AR initialization. The core idea is that causal CD learns the same AR-conditional flow map as causal ODE distillation, but obtains supervision from a single online teacher ODE step between adjacent timesteps, avoiding the need to precompute and store full PF-ODE trajectories. This makes the initialization both more efficient and easier to optimize. The resulting pipeline, \ours, surpasses the SOTA 4-step chunk-wise Causal Forcing under the \textit{\textbf{frame-wise 2-step setting}} by 0.1 in VBench Total, 0.3 in VBench Quality, and 0.335 in VisionReward, while reducing first-frame latency by 50\% and Stage 2 training cost by $\sim$$4\times$. We further extend the pipeline to action-conditioned world model generation in the spirit of Genie3. Project Page: https://github.com/thu-ml/Causal-Forcing and https://github.com/shengshu-ai/minWM .

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/HCWPARMV)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/JAFJCHPQ)

## 合并条目与附件来源

- [Zotero 条目 MEILYEYD](zotero://select/library/items/MEILYEYD)
- [来源网页](https://huggingface.co/papers/2605.15141)
- [在 Zotero 查看附件](zotero://select/library/items/EE8EKM3U)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-SU7DT9W7 - Causal Forcing  Autoregressive Diffusion Distillation Done Right for High-Quality Rea|Causal Forcing: Autoregressive Diffusion Distillation Done Right for High-Quality Real-Time Interactive Video Generation]] — 强关联；本篇摘要提到模型 Causal Forcing（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-CSY37EWX - One-Forcing  Towards Stable One-Step Autoregressive Video Generation|One-Forcing: Towards Stable One-Step Autoregressive Video Generation]] — 中关联；共同研究内容：低延迟自回归视频、少步与蒸馏。
- [[Zotero Knowledge/Papers/ZK-YKKPMHHW - Causal-rCM  A Unified Teacher-Forcing and Self-Forcing Open Recipe for Autoregressive|Causal-rCM: A Unified Teacher-Forcing and Self-Forcing Open Recipe for Autoregressive Diffusion Distillation in Streaming Video Generation and Interactive World Models]] — 中关联；共同研究内容：低延迟自回归视频、动作条件预测、少步与蒸馏。

<!-- content-relations:end -->
