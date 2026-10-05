---
type: "literature-note"
title: "VACE: All-in-One Video Creation and Editing"
aliases: ["VACE: All-in-One Video Creation and Editing"]
zotero_keys: ["IDTQ2XG3"]
year: 2025
authors: ["Zeyinzi Jiang", "Zhen Han", "Chaojie Mao", "Jingfeng Zhang", "Yulin Pan", "Yu Liu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2503.07598"
url: "http://arxiv.org/abs/2503.07598"
collections: ["03 Visual Generation/Editing & Identity Control"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# VACE: All-in-One Video Creation and Editing

[Zotero 条目 IDTQ2XG3](zotero://select/library/items/IDTQ2XG3)

[DOI 原文](https://doi.org/10.48550/arxiv.2503.07598)

[来源网页](http://arxiv.org/abs/2503.07598)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Editing & Identity Control/索引|03 Visual Generation/Editing & Identity Control]]

## 原始摘要

Diffusion Transformer has demonstrated powerful capability and scalability in generating high-quality images and videos. Further pursuing the unification of generation and editing tasks has yielded significant progress in the domain of image content creation. However, due to the intrinsic demands for consistency across both temporal and spatial dynamics, achieving a unified approach for video synthesis remains challenging. We introduce VACE, which enables users to perform Video tasks within an All-in-one framework for Creation and Editing. These tasks include reference-to-video generation, video-to-video editing, and masked video-to-video editing. Specifically, we effectively *Equal Contribution. †Project lead.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project page: https://ali-vilab.github.io/VACE-Page/

[在 Zotero 查看](zotero://select/library/items/NMZ4HK4M)

Comment: Project page: https://ali-vilab.github.io/VACE-Page/

以下是对论文 **《VACE: All-in-One Video Creation and Editing》** 的总结，重点放在 **Masked Video-to-Video Editing (MV2V)** 的部分及其涉及的 Mask 相关方法论与技术路径。

## 一、总体创新概述

VACE 的核心创新是提出一个 **统一的视频生成与编辑框架**，适配多种输入模态（文本、图像、视频、mask），并通过统一接口 **Video Condition Unit (VCU)** 和结构适配机制 **Context Adapter** 实现不同任务（T2V, R2V, V2V, MV2V）及其组合的“一模多用”。
VACE 的目标是让所有视频生成与编辑任务都能在同一个模型中执行，从而摆脱以往各任务分别训练的困境。

## 二、MV2V（Masked Video-to-Video Editing）的设计目标与创新点

### 1. 任务定义与特点

MV2V 是在输入视频的 **局部三维空间-时间区域 (3D ROI)** 内进行修改的任务，属于“部分编辑”类操作，例如：

- 
视频对象修复、主体删除（inpainting）

- 
场景扩展（outpainting）

- 
视频时序延展（temporal extension）
其关键挑战是：**在局部修改的同时保持与未修改部分的时空一致性**。

在 VACE 中，MV2V 是四大基础任务之一，其输入包括：

- 
原始视频帧序列 `{u1, u2, ..., un}`

- 
与视频对齐的 mask 序列 `{m1, m2, ..., mn}`，用“1”表示可编辑区域、“0”表示保持不变。
两者在空间 (`h×w`) 和时间 (`n`) 上完全对齐。

## 三、Mask 相关的 Methodology 与 Technical Path

### A. **Video Condition Unit (VCU) 表示统一化**

在 VACE 中，mask 元素是被正式纳入到模型输入结构的关键一环。
VCU 定义为： $$
V = [T; F; M]$$ 其中：

- 
$T$ 为文本提示

- 
$F = \{u_1, u_2, \ldots, u_n\}$ 为上下文帧序列（RGB）

- 
$M = \{m_1, m_2, \ldots, m_n\}$ 为时间序列 mask（二值）

在 MV2V 中： $$
F = \{u_1, u_2, ..., u_n\}, \quad M = \{m_1, m_2, ..., m_n\}$$

这一结构实现了 **mask 与视频的空间-时间对齐表示（spatiotemporal aligned representation）**，为后续模块如 “Concept Decoupling” 和 “Context Embedder” 提供标准化接口。

### B. **Concept Decoupling（概念解耦策略）**

MV2V 任务中 mask 的核心作用是将视频区域划分为：

- 
**Reactive frames ($F_c$)**：待编辑区域（$M=1$）

- 
**Inactive frames ($F_k$)**：保持不变的区域（$M=0$）

实现方式如下： $$
F_c = F \times M, \quad F_k = F \times (1 - M)$$

这个解耦操作的创新点：

- 
**将语义角色分离**：允许模型明确学习“该修改”与“不该修改”的特征。

- 
**提升模型收敛速度与编辑定位精度**：有效防止在训练中图像与视频特征分布的混淆。

- 
**兼容多类型任务**：mask 能表示局部空间、局部时间甚至复杂 3D ROI，使模型具备跨任务的泛化能力。

### C. **Context Latent Encoding（上下文潜编码）**

MV2V 任务需要确保 mask 与视频在 **时空维度上的一致性**。
在这个阶段，经过概念解耦的 $F_c$, $F_k$ 和 $M$：

- 
都被编码到高维潜空间（与视频 VAE 的 latent space 对齐）；

- 
维度为 $n′ × h′ × w′$，保证时序与空间一致；

- 
mask 通过 reshape 和插值操作，对齐至视频 latent 的空间尺度。

这一过程的目的：

将局部编辑区域（由 mask 控定）无缝嵌入视频生成的整体时空特征流，使结果在视觉上平滑过渡。

### D. **Context Embedder（上下文嵌入器）**

此模块将 $F_c$, $F_k$, $M$ 拼接在通道维度后进行 token 化： $$
\text{Context Tokens} = \text{Embed}(F_c, F_k, M)$$ 其中：

- 
mask 的嵌入权重初始化为零（保证学习基于任务相关signal）；

- 
模型利用 Diffusion Transformer 的 block 结构进行上下文注入。

这样做的优点：

- 
mask 信号在 token 层直接参与 attention；

- 
改变区域与保持区域的信息被 Transformer 同时建模；

- 
形成适应各种编辑范围的统一特征流。

### E. **Training Strategy — Context Adapter Tuning**

在具体训练阶段，MV2V 不采用传统的全量微调，而使用“**Context Adapter Tuning**”：

- 
主干 DiT 参数冻结；

- 
仅训练 Context Blocks 与 mask 相关的辅助分支；

- 
mask 控制的区域编辑信号以“加性残差 (Additive Signal)”形式被注入主干模型。

这种方法的技术优势：

- 
收敛速度快；

- 
模型可插拔（mask 编辑能力可单独添加）；

- 
支持多任务融合（如结合参考生成 + 局部编辑）。

### F. **Dataset Construction for Mask Tasks**

在数据构建上，VACE 针对 mask 设计了专门的样本生成策略：

- 
**Inpainting/Outpainting任务**：随机实例挖空构造局部mask，mask反转用于outpainting。

- 
**Extension任务**：提取首尾帧并标注mask进行时序扩展。

- 
**Augmentation**：对mask进行任意形态变换（形状/比例），扩大模型对各种局部编辑粒度的泛化适应性。

通过结合 SAM2 [52] 的时序传播和 RAM + Grounding DINO 的检测结果构成视频级mask分布，为 MV2V 提供真实、稳定的训练样本。

## 四、总结：MV2V创新点核心

 | 

层次

 | 

创新点

 | 

技术实现

 | 

**输入统一化**

 | 

用 VCU 定义 mask 与视频、文本的统一格式

 | 

$V = [T; F; M]$

 | 

**概念解耦**

 | 

分离编辑和非编辑区域

 | 

$F_c = F×M$, $F_k = F×(1-M)$

 | 

**潜空间对齐**

 | 

在高维 latent 中保持 mask 的时空一致性

 | 

Context Latent Encoding

 | 

**上下文嵌入**

 | 

将 mask 融入 Transformer token 流

 | 

Context Embedder

 | 

**高效训练**

 | 

使用 Context Adapter Tuning 实现可插拔式 mask 训练

 | 

冻结主干，仅训练 adapter

 | 

**数据支持**

 | 

提供多任务、多形态的视频局部mask构造

 | 

RAM + DINO + SAM2 segmentation

### 简要结论

在 VACE 中，mask 不再只是辅助标注，而是被提升为视频编辑与生成任务的核心控制信号。通过 **VCU → Concept Decoupling → Context Adapter** 这一完整链路，MV2V 实现了“统一输入、分离学习、时空对齐、可插训练、灵活组合”的创新技术路径，使局部视频编辑任务能够与其他生成任务在同一模型中共融运行。

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/MUDEJ8NS)

[批注 SCT3B4A5 · 第 5 页](zotero://open-pdf/library/items/MUDEJ8NS?annotation=SCT3B4A5&page=5)

> RAM [78] and combine it with Grounding DINO

[批注 H74KRZLP · 第 5 页](zotero://open-pdf/library/items/MUDEJ8NS?annotation=H74KRZLP&page=5)

> secondary filtering on videos with target areas that are either too small or too large

[批注 XRYJLE8U · 第 5 页](zotero://open-pdf/library/items/MUDEJ8NS?annotation=XRYJLE8U&page=5)

> propagate operation

[批注 DDNSKQV9 · 第 5 页](zotero://open-pdf/library/items/MUDEJ8NS?annotation=DDNSKQV9&page=5)

> SAM2

[批注 V2DVKDKY · 第 5 页](zotero://open-pdf/library/items/MUDEJ8NS?annotation=V2DVKDKY&page=5)

> video segmentation

[批注 7B5AD7CV · 第 5 页](zotero://open-pdf/library/items/MUDEJ8NS?annotation=7B5AD7CV&page=5)

> effective frame ratio based on the mask area threshold

[批注 TN6H4R4J · 第 5 页](zotero://open-pdf/library/items/MUDEJ8NS?annotation=TN6H4R4J&page=5)

> repainting tasks, random instances from the videos can be masked for inpainting, while the inverse of the mask enables the construction of outpainting data. Augmentation of the masks [62] allows for unconditional inpainting.

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
