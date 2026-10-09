---
type: "literature-note"
title: "Causal Forcing: Autoregressive Diffusion Distillation Done Right for High-Quality Real-Time Interactive Video Generation"
aliases: ["Causal Forcing: Autoregressive Diffusion Distillation Done Right for High-Quality Real-Time Interactive Video Generation"]
zotero_keys: ["SU7DT9W7"]
year: 2026
authors: ["Hongzhou Zhu", "Min Zhao", "Guande He", "Hang Su", "Chongxuan Li", "Jun Zhu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2602.02214"
url: "http://arxiv.org/abs/2602.02214"
collections: ["03 Visual Generation/General Video Generation"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature", "concept/视频生成的因果化与流式推理", "concept-primary/视频生成的因果化与流式推理"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Causal Forcing: Autoregressive Diffusion Distillation Done Right for High-Quality Real-Time Interactive Video Generation

[Zotero 条目 SU7DT9W7](zotero://select/library/items/SU7DT9W7)

[DOI 原文](https://doi.org/10.48550/arxiv.2602.02214)

[来源网页](http://arxiv.org/abs/2602.02214)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/General Video Generation/索引|03 Visual Generation/General Video Generation]]

概念地图：[[Zotero Knowledge/Concepts/视频生成的因果化与流式推理|视频生成的因果化与流式推理]]

## 原始摘要

To achieve real-time interactive video generation, current methods distill pretrained bidirectional video diffusion models into few-step autoregressive (AR) models, facing an architectural gap when full attention is replaced by causal attention. However, existing approaches do not bridge this gap theoretically. They initialize the AR student via ODE distillation, which requires frame-level injectivity, where each noisy frame must map to a unique clean frame under the PF-ODE of an AR teacher. Distilling an AR student from a bidirectional teacher violates this condition, preventing recovery of the teacher's flow map and instead inducing a conditional-expectation solution, which degrades performance. To address this issue, we propose Causal Forcing, which uses an autoregressive teacher for ODE initialization to bridge the architectural gap, and then applies the same DMD procedure as in Self Forcing. Empirical results show that our method outperforms all baselines across all metrics, surpassing the SOTA Self Forcing by 19.3\% in Dynamic Degree, 8.7\% in VisionReward, and 16.7\% in Instruction Following. Project page: \href{https://thu-ml.github.io/CausalForcing.github.io/}{https://thu-ml.github.io/CausalForcing.github.io/}; the code: \href{https://github.com/thu-ml/Causal-Forcing}{https://github.com/thu-ml/Causal-Forcing}.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project page and the code: \href{https://thu-ml.github.io/CausalForcing.github.io/}{https://thu-ml.github.io/Ca

[在 Zotero 查看](zotero://select/library/items/LVZXNIKR)

Comment: Project page and the code: \href{https://thu-ml.github.io/CausalForcing.github.io/}{https://thu-ml.github.io/CausalForcing.github.io/}; https://github.com/thu-ml/Causal-Forcing. ICML 2026

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/L78WFAE7)

[批注 RHIKJ2WS · 第 1 页](zotero://open-pdf/library/items/L78WFAE7?annotation=RHIKJ2WS&page=1)

> ODE distillation

批注评论：<b>ODE Distillation</b> is a machine learning technique used to massively accelerate the inference time of generative <b>diffusion models</b>

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/7BN778ZC)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-YLGPQLIA - Causal Forcing++  Scalable Few-Step Autoregressive Diffusion Distillation for Real-Ti|Causal Forcing++: Scalable Few-Step Autoregressive Diffusion Distillation for Real-Time Interactive Video Generation]] — 强关联；对方摘要提到模型 Causal Forcing（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-CSY37EWX - One-Forcing  Towards Stable One-Step Autoregressive Video Generation|One-Forcing: Towards Stable One-Step Autoregressive Video Generation]] — 中关联；共同研究内容：低延迟自回归视频、少步与蒸馏。
- [[Zotero Knowledge/Papers/ZK-UNNWY4C6 - From Slow Bidirectional to Fast Autoregressive Video Diffusion Models|From Slow Bidirectional to Fast Autoregressive Video Diffusion Models]] — 中关联；共同研究内容：低延迟自回归视频、少步与蒸馏、扩散生成架构。
- [[Zotero Knowledge/Papers/ZK-YKKPMHHW - Causal-rCM  A Unified Teacher-Forcing and Self-Forcing Open Recipe for Autoregressive|Causal-rCM: A Unified Teacher-Forcing and Self-Forcing Open Recipe for Autoregressive Diffusion Distillation in Streaming Video Generation and Interactive World Models]] — 中关联；共同研究内容：低延迟自回归视频、少步与蒸馏、扩散生成架构。
- [[Zotero Knowledge/Papers/ZK-HX6ZCBCB - Matrix-Game 3.0  Real-Time and Streaming Interactive World Model with Long-Horizon Me|Matrix-Game 3.0: Real-Time and Streaming Interactive World Model with Long-Horizon Memory]] — 中关联；共同研究内容：少步与蒸馏、扩散生成架构。

<!-- content-relations:end -->
