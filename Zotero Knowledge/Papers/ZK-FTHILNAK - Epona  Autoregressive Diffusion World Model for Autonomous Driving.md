---
type: "literature-note"
title: "Epona: Autoregressive Diffusion World Model for Autonomous Driving"
aliases: ["Epona: Autoregressive Diffusion World Model for Autonomous Driving"]
zotero_keys: ["FTHILNAK"]
year: 2025
authors: ["Kaiwen Zhang", "Zhenyu Tang", "Xiaotao Hu", "Xingang Pan", "Xiaoyang Guo", "Yuan Liu", "Jingwei Huang", "Li Yuan", "Qian Zhang", "Xiao-Xiao Long", "Xun Cao", "Wei Yin"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2506.24113"
url: "http://arxiv.org/abs/2506.24113"
collections: ["04 World Models/Video-Based Interactive Simulation"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Epona: Autoregressive Diffusion World Model for Autonomous Driving

[Zotero 条目 FTHILNAK](zotero://select/library/items/FTHILNAK)

[DOI 原文](https://doi.org/10.48550/arxiv.2506.24113)

[来源网页](http://arxiv.org/abs/2506.24113)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

补充阅读入口：[[Zotero Knowledge/Topics/05 Robot Learning/Planning & Inverse Control/索引|05 Robot Learning/Planning & Inverse Control]]

## 原始摘要

Diffusion models have demonstrated exceptional visual quality in video generation, making them promising for autonomous driving world modeling. However, existing video diffusion-based world models struggle with flexible-length, long-horizon predictions and integrating trajectory planning. This is because conventional video diffusion models rely on global joint distribution modeling of fixed-length frame sequences rather than sequentially constructing localized distributions at each timestep. In this work, we propose Epona, an autoregressive diffusion world model that enables localized spatiotemporal distribution modeling through two key innovations: 1) Decoupled spatiotemporal factorization that separates temporal dynamics modeling from fine-grained future world generation, and 2) Modular trajectory and video prediction that seamlessly integrate motion planning with visual modeling in an end-to-end framework. Our architecture enables high-resolution, long-duration generation while introducing a novel chain-of-forward training strategy to address error accumulation in autoregressive loops. Experimental results demonstrate state-of-the-art performance with 7.4\% FVD improvement and minutes longer prediction duration compared to prior works. The learned world model further serves as a real-time motion planner, outperforming strong end-to-end planners on NAVSIM benchmarks. Code will be publicly available at \href{https://github.com/Kevin-thu/Epona/}{https://github.com/Kevin-thu/Epona/}.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: ICCV2025, Project Page: https://kevin-thu.github.io/Epona/

[在 Zotero 查看](zotero://select/library/items/PWSZCRDW)

Comment: ICCV2025, Project Page: https://kevin-thu.github.io/Epona/

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/SKBYN3KR)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/CH9VK4KG)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-CMM8GA8N - Astra  General Interactive World Model with Autoregressive Denoising|Astra: General Interactive World Model with Autoregressive Denoising]] — 中关联；共同研究内容：低延迟自回归视频、扩散生成架构、自动驾驶。
- [[Zotero Knowledge/Papers/ZK-UNNWY4C6 - From Slow Bidirectional to Fast Autoregressive Video Diffusion Models|From Slow Bidirectional to Fast Autoregressive Video Diffusion Models]] — 中关联；共同研究内容：低延迟自回归视频、基准与数据合成、扩散生成架构。
- [[Zotero Knowledge/Papers/ZK-4RGNDFVB - DynVLA  Learning World Dynamics for Action Reasoning in Autonomous Driving|DynVLA: Learning World Dynamics for Action Reasoning in Autonomous Driving]] — 中关联；共同研究内容：自动驾驶。

<!-- content-relations:end -->
