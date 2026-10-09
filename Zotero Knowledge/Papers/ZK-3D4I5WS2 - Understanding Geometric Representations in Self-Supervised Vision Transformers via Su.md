---
type: "literature"
title: "Understanding Geometric Representations in Self-Supervised Vision Transformers via Subspace Intervention"
aliases: ["Geometric Subspace Intervention"]
zotero_keys: ["3D4I5WS2"]
year: 2026
authors: ["Zhou, Weichen", "Zou, Yawen", "Gu, Chunzhi", "Dong, Ran", "Xie, Haoran", "Zhang, Chao"]
venue: "ECCV 2026"
doi: ""
url: "https://arxiv.org/abs/2607.01987"
collections: ["02 Representation & Perception/Visual Representation Learning", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1", "concept/视觉自监督的目标与表征结构", "concept-primary/视觉自监督的目标与表征结构"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [124, 139]
imported_at: "2026-10-03"
---

# Understanding Geometric Representations in Self-Supervised Vision Transformers via Subspace Intervention

[在 Zotero 打开](zotero://select/library/items/3D4I5WS2) · [论文来源](https://arxiv.org/abs/2607.01987) · [论文 PDF](https://arxiv.org/pdf/2607.01987)

## 文献导读

对训练后的几何探针权重做 SVD 并进行子空间干预，研究几何信息的可读性、可压缩性和跨层分布。区分特征中存在信息与某种探针能够读出信息。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-QQB2NRRQ - Masked Autoencoders Are Scalable Vision Learners|MAE]]
- [[Zotero Knowledge/Papers/ZK-Y364L7RZ - MultiLoReFT  Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning|MultiLoReFT]]

## 原始摘要

We introduce a controlled subspace intervention framework to investigate how self-supervised Vision Transformers (ViTs) encode dense geometric information. While linear probing is widely used to assess geometric representations, it treats features as a black box, failing to disentangle the underlying topology. To address this issue, we decompose the weights of converged linear probes to isolate the low-rank subspaces containing explicit geometric signals using Singular Value Decomposition (SVD). Our perspective yields three key insights: (1) Pre-training objectives determine how features are encoded. DINOv2 aligns spatial features for efficient linear extraction, while Masked Autoencoders (MAE) tend to disperse these signals, requiring a broader spatial context. (2) Explicit geometric representations are highly compressible, suggesting dense predictive heads could potentially be constrained to low-rank subspaces with minimal performance loss. (3) The layer-wise task affinity suggests that geometric precision peaks at intermediate layers before yielding to semantic abstraction in the final layers. By connecting internal encoding mechanics with downstream performance, these findings provide a basis for effective feature selection and lightweight decoder design. The source code is available at this https URL .

来源：[论文官方页面](https://arxiv.org/abs/2607.01987)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 124–139 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 124 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-124.png]]

> [!quote]- 本页可搜索文字
> ECCV 2026 Oral
>
> Understanding Geometric Representations
>
> in Self-Supervised Vision Transformers
>
> via Subspace Intervention
>
> Weichen Zhou, Yawen Zou, Chunzhi Gu, Ran Dong, Haoran Xie, Chao Zhang (Corresponding)
>
> 汇报人：马樱萍	           学号：2612144 
>
> 1
>

### 原 PPT 第 125 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-125.png]]

> [!quote]- 本页可搜索文字
> 目录
>
> 01
>
> 研究背景与动机
>
> 02
>
> 方法：子空间干预框架
>
> 03
>
> 实验设计
>
> 04
>
> 核心结果与分析
>
> 05
>
> 结论与展望
>
> 2
>

### 原 PPT 第 126 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-126.png]]

> [!quote]- 本页可搜索文字
> 01 · 研究背景
>
> 自监督 ViT 已具备隐式几何理解，但编码方式未知
>
> 已确立的事实
>
> 自监督 ViT（DINOv2、MAE 等）作为稠密预测骨干，在无显式 3D 监督下即可恢复单视图几何信息（深度、表面法线）。
>
> 这种几何感知是解决语义歧义的功能性必需。
>
> 尚未解决的问题
>
> 几何信息究竟是分散在整个高维特征空间，还是对齐到特定的线性可访问坐标？
>
> 现有黑盒探针无法区分"信息缺失"与"信息无法解码"。
>
> 核心假设
>
> 预训练目标（自蒸馏 / 掩码重建 / 混合）决定了几何基元在隐子空间中的路由与格式化方式。理解不同范式如何塑造内部几何表示，是有效适配下游任务的关键。
>
> 3
>

### 原 PPT 第 127 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-127.png]]

> [!quote]- 本页可搜索文字
> 02 · 方法总览
>
> 受控子空间干预框架：两阶段诊断
>
> Figure 1 · 框架总览：(A) 三层探针建立可读性差距；(B) SVD 分解探针权重，对子空间做投影干预后用冻结线性头评估
>
> 阶段一：Readability Gap
>
> 阶段二：Subspace Intervention
>
> 4
>

### 原 PPT 第 128 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-128.png]]

> [!quote]- 本页可搜索文字
> 02 · 三层探针层级
>
> 三级探针解耦"是否存在"与"如何编码"
>
> Tier 1 · Linear
>
> 1×1 卷积直接映射 patch token 到目标空间
>
> 测量显式、可线性读取的几何信号
>
> Tier 2 · MLP
>
> 逐 token 引入 GELU 非线性
>
> 与 Tier 1 的差距 = 局部非线性纠缠
>
> Tier 3 · DPT
>
> 多尺度聚合 + 全局感受野
>
> 与 Tier 2 的差距 = 空间碎片化
>
> 诊断逻辑
>
> 5
>
> 线性探针表现好：几何已线性对齐（显式编码）
>
> Linear 较差但 MLP 补回：几何存在局部非线性纠缠
>
> MLP 仍差但 DPT 补回：几何信息分散在多个 patch
>

### 原 PPT 第 129 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-129.png]]

> [!quote]- 本页可搜索文字
> 02 · 子空间干预
>
> 对探针权重做 SVD，隔离任务对齐方向
>
> 核心观察
>
> 线性探针通过将特征投影到学习到的权重矩阵 W 上来提取信息。由于目标空间维度 C 远小于特征维度 D，W 的秩被上界为 C。
>
> 收敛后的 W 编码了探针发现的任务对齐几何方向。
>
> 干预操作（无需额外训练）
>
> ① 对 W 做 SVD，提取前 k 个右奇异向量
>
> ② 将特征投影到任务对齐子空间 Sₖ
>
> ③ 用冻结线性头评估，无需重新训练
>
> 严格控制：随机子空间与正交残差
>
> 随机子空间 Rₖ
>
> 维度相同但打乱任务对齐，作为空基线。
>
> 6
>
> 正交残差 Sk⊥
>
> 移除对齐成分，检验低秩核心是否已包含主要信号。
>

### 原 PPT 第 130 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-130.png]]

> [!quote]- 本页可搜索文字
> 03 · 实验设置
>
> 三种自监督范式 × 三类几何任务
>
> 评估的自监督范式（均为 ViT-L）
>
> DINOv2：自蒸馏范式，冻结主干
>
> MAE：掩码图像建模（生成式重建）
>
> iBOT：自蒸馏 + 掩码 tokenizer 混合
>
> 数据集与任务
>
> NYU Depth V2（主实验）：室内单目深度估计
>
> 表面法线估计：角度精度 d1 < 11.25°
>
> 40 类语义分割：mIoU
>
> 分析路线
>
> 1  三级探针：区分线性对齐与空间分散
>
> 2  SVD 干预：测量可压缩性与跨层能量
>
> 3  单层分析：比较几何与语义的层级偏好
>
> 4  多随机种子：验证低秩子空间稳定性
>
> 7
>

### 原 PPT 第 131 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-131.png]]

> [!quote]- 本页可搜索文字
> 04 · 结果 · 特征编码格式
>
> DINOv2 线性对齐，MAE 空间分散
>
> Backbone
>
> Linear
>
> 1×1 MLP
>
> DPT
>
> Local Entang.
>
> DINOv2-L
>
> 0.9157
>
> 0.9325
>
> 0.9483
>
> +0.0168
>
> iBOT-L
>
> 0.8198
>
> 0.8376
>
> 0.8524
>
> +0.0178
>
> MAE-L
>
> 0.6033
>
> 0.6390
>
> 0.7022
>
> +0.0357
>
> 指标：Scale-aware δ1
>
> 越大越好
>
> Table 1 · 三级探针性能
>
> 结论
>
> DINOv2 的线性探针已接近 DPT，几何信息呈线性可读格式。
>
> MAE 依赖全局聚合，说明几何基元分散在多个 patch。
>
> iBOT 处于两种编码方式之间。
>
> 8
>

### 原 PPT 第 132 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-132.png]]

> [!quote]- 本页可搜索文字
> 04 · 结果 · 可压缩性
>
> 显式几何表示高度可压缩：低秩子空间足以恢复
>
> 关键观察
>
> 随机子空间与正交残差上性能骤降至噪声基线 → 预测严格瓶颈在前 k 维。
>
> MAE 在 k=32 时已恢复 >98% 线性潜力（最快饱和）。
>
> DINOv2 需 k ≥ 64 才收敛——因为它线性编码了更丰富的细粒度几何细节。
>
> Figure 3 · 不同秩 k 下的深度预测可视化（RGB 输入 / GT / DINOv2 / MAE / iBOT）
>
> 启示：稠密预测头可被约束在低秩子空间中，几乎不损失性能——为轻量化解码器设计提供了依据。
>
> 9
>

### 原 PPT 第 133 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-133.png]]

> [!quote]- 本页可搜索文字
> 04 · 结果 · 跨层能量路由
>
> DINOv2 将 72% 几何能量压在中间层
>
> Model
>
> l6
>
> l12
>
> l18
>
> l24
>
> DINOv2
>
> 17.2%
>
> 35.8%
>
> 36.7%
>
> 10.3%
>
> iBOT
>
> 26.9%
>
> 28.4%
>
> 22.4%
>
> 22.3%
>
> MAE
>
> 19.5%
>
> 28.4%
>
> 32.7%
>
> 19.4%
>
> 解读
>
> DINOv2 的几何能量集中在中间层，末层明显下降。
>
> MAE 与 iBOT 的能量分布更均匀。
>
> 启示
>
> 多尺度探针之所以有效，是因为它用中间层补偿了 DINOv2 末层几何容量的急剧下降——但这也掩盖了末层发生了什么。
>
> 必须做严格的单层诊断，才能追踪空间理解是如何逐层演化、又是在哪里退化的。
>
> 10
>

### 原 PPT 第 134 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-134.png]]

> [!quote]- 本页可搜索文字
> 04 · 结果 · 逐层任务亲和度
>
> 几何精度在中间层达峰，语义抽象在末层达峰
>
> 任务峰值逐层后移
>
> 表面法线：Layer 18 达峰
>
> 深度估计：Layer 21 达峰
>
> 语义分割：Layer 24 达峰
>
> 归一化轨迹呈顺序迁移：中间层偏好局部几何，末层转向高层语义抽象。
>
> 启示：只依赖末层特征做稠密多任务预测是次优的——需要按深度做特征路由（depth-aware feature routing）。
>
> 11
>
> Figure 6 · DINOv2 在不同层（18 / 21 / 24）解码的表面法线、深度与语义分割预测
>

### 原 PPT 第 135 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-135.png]]

> [!quote]- 本页可搜索文字
> 04 · 结果 · 鲁棒性验证
>
> 低秩核心是结构属性，而非优化偶然
>
> 验证设计
>
> 用三个随机探针初始化训练线性探针，分别提取子空间基 V_k，测量它们之间的子空间相似度（principal angle）。
>
> 结果
>
> 低秩段（k ≤ 16）：跨初始化相似度 > 0.93（DINOv2）→ 几何核心稳定。
>
> 高维尾段（k ≥ 64）：相似度低 → 缺乏稳定几何信号，对初始化敏感。
>
> 意义
>
> 这与可压缩性结论互相印证：前 k 个主成分承载了真正稳定的几何信号，而尾部维度没有一致的几何语义。
>
> 排除了"提取到的低秩基只是某种优化伪影"的质疑——它确实反映了特征流形的内在结构。
>
> 12
>

### 原 PPT 第 136 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-136.png]]

> [!quote]- 本页可搜索文字
> 05 · 主要发现
>
> 三大核心发现
>
> 01
>
> 预训练目标决定几何编码格式
>
> DINOv2 自蒸馏将几何对齐为低秩线性坐标；MAE 掩码重建将信号分散到全局 patch，需要空间聚合。
>
> 02
>
> 显式几何高度可压缩
>
> 所有范式下，显式几何信号均可压缩到 k ≤ 64 的低秩子空间而几乎无损——稠密预测头可轻量化。
>
> 03
>
> 逐层任务亲和度：几何在中间层达峰
>
> 13
>
> 表面法线（l18）、深度（l21）、语义（l24）依次达峰，末层几何衰减来自语义抽象。
>

### 原 PPT 第 137 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-137.png]]

> [!quote]- 本页可搜索文字
> 05 · 贡献与价值
>
> 方法论贡献与下游价值
>
> 方法论贡献
>
> 提出受控子空间干预框架，将探针权重 SVD 分解后做后验分析
>
> 三级探针层级解耦"局部非线性纠缠"与"全局空间碎片化"
>
> 从黑盒输出指标转向对内部流形拓扑的直接检查
>
> 对下游的指导意义
>
> 特征选择：几何任务应路由到中间层，而非默认取末层
>
> 轻量解码器：预测头可约束在低秩子空间，减少参数与计算
>
> 范式选择：DINOv2 类自蒸馏更适合需要线性可读几何的下游任务
>
> 14
>

### 原 PPT 第 138 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-138.png]]

> [!quote]- 本页可搜索文字
> 05 · 局限与未来
>
> 局限性与未来方向
>
> 当前局限
>
> 未来方向
>
> 15
>
> 线性干预只能分离显式几何，难以展开高度非线性纠缠。
>
> 跨域与户外验证受限，缺少同时具备深度、法线和语义标注的数据。
>
> 受资源限制，尚未评估 ViT-G 等更大模型。
>
> 扩展到非线性拓扑干预，解开被折叠的几何信号。
>
> 使用合成多模态数据覆盖户外与跨域场景。
>
> 在更大规模模型上验证编码格式的一致性。
>

### 原 PPT 第 139 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-139.png]]

> [!quote]- 本页可搜索文字
> 感 谢 聆 听 
>
> 敬 请 批 评 指 正
>
> 汇报人：马樱萍
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-QQB2NRRQ - Masked Autoencoders Are Scalable Vision Learners|Masked Autoencoders Are Scalable Vision Learners]] — 强关联；本篇摘要提到模型 MAE（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-RAH7V3N7 - Low-Rank Rescaled Vision Transformer Fine-Tuning  A Residual Design Approach|Low-Rank Rescaled Vision Transformer Fine-Tuning: A Residual Design Approach]] — 中关联；共同研究内容：低秩与参数高效微调。
- [[Zotero Knowledge/Papers/ZK-Y364L7RZ - MultiLoReFT  Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning|MultiLoReFT: Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning via Low-Rank Representation Fine-Tuning]] — 中关联；共同研究内容：低秩与参数高效微调。

<!-- content-relations:end -->

<!-- research-integration:start -->
## 研究主题入口

- [[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]]

## 概念比较入口

- [[Zotero Knowledge/Concepts/视觉自监督的目标与表征结构|视觉自监督的目标与表征结构]]
<!-- research-integration:end -->
