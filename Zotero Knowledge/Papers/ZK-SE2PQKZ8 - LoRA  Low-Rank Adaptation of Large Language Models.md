---
type: "literature"
title: "LoRA: Low-Rank Adaptation of Large Language Models"
aliases: ["LoRA"]
zotero_keys: ["SE2PQKZ8"]
year: 2022
authors: ["Hu, Edward J.", "Shen, Yelong", "Wallis, Phillip", "Allen-Zhu, Zeyuan", "Li, Yuanzhi", "Wang, Shean", "Wang, Lu", "Chen, Weizhu"]
venue: "ICLR 2022"
doi: ""
url: "https://arxiv.org/abs/2106.09685"
collections: ["06 Alignment & Reliability/Adaptation & Generalization", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [55, 68]
imported_at: "2026-10-03"
---

# LoRA: Low-Rank Adaptation of Large Language Models

[在 Zotero 打开](zotero://select/library/items/SE2PQKZ8) · [论文来源](https://arxiv.org/abs/2106.09685) · [论文 PDF](https://arxiv.org/pdf/2106.09685)

## 文献导读

冻结预训练权重，用低秩矩阵参数化权重增量。关注更新位置、秩、参数预算，以及训练后的增量合并方式。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Adaptation & Generalization/索引|06 Alignment & Reliability/Adaptation & Generalization]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-WE2HF7Y8 - Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning|Intrinsic Dimensionality]]
- [[Zotero Knowledge/Papers/ZK-RAH7V3N7 - Low-Rank Rescaled Vision Transformer Fine-Tuning  A Residual Design Approach|RLRR]]
- [[Zotero Knowledge/Papers/ZK-Y364L7RZ - MultiLoReFT  Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning|MultiLoReFT]]

## 原始摘要

An important paradigm of natural language processing consists of large-scale pre-training on general domain data and adaptation to particular tasks or domains. As we pre-train larger models, full fine-tuning, which retrains all model parameters, becomes less feasible. Using GPT-3 175B as an example -- deploying independent instances of fine-tuned models, each with 175B parameters, is prohibitively expensive. We propose Low-Rank Adaptation, or LoRA, which freezes the pre-trained model weights and injects trainable rank decomposition matrices into each layer of the Transformer architecture, greatly reducing the number of trainable parameters for downstream tasks. Compared to GPT-3 175B fine-tuned with Adam, LoRA can reduce the number of trainable parameters by 10,000 times and the GPU memory requirement by 3 times. LoRA performs on-par or better than fine-tuning in model quality on RoBERTa, DeBERTa, GPT-2, and GPT-3, despite having fewer trainable parameters, a higher training throughput, and, unlike adapters, no additional inference latency. We also provide an empirical investigation into rank-deficiency in language model adaptation, which sheds light on the efficacy of LoRA. We release a package that facilitates the integration of LoRA with PyTorch models and provide our implementations and model checkpoints for RoBERTa, DeBERTa, and GPT-2 at this https URL .

来源：[论文官方页面](https://arxiv.org/abs/2106.09685)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 55–68 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 55 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-055.png]]

> [!quote]- 本页可搜索文字
> TONGJI UNIVERSITY
>
> 汇报人：丰佳奕 
>
> 日期：2026年9月23日
>
> LoRA：大语言模型的低秩适配
>
> Low-Rank Adaptation of Large Language Models
>
> Edward Hu 等  ·  ICLR  ·  2022
>

### 原 PPT 第 56 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-056.png]]

> [!quote]- 本页可搜索文字
> 01
>
> PART ONE
>
> 背景与问题
>
> TONGJI UNIVERSITY
>

### 原 PPT 第 57 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-057.png]]

> [!quote]- 本页可搜索文字
> 研究动机：全量微调的适配成本
>
> 阶段 1：传统任务专用训练
>
> 任务 A
>
> （图像分类）
>
> 标注数据
>
> （任务 A）
>
> 模型 A
>
> 任务 B
>
> （情感分析）
>
> 标注数据
>
> （任务 B）
>
> 模型 B
>
> 任务 C
>
> （机器翻译）
>
> 标注数据
>
> （任务 C）
>
> 模型 C
>
> 每个任务单独收集标注数据
>
> 为每个任务从头训练一个模型
>
> 成本高、泛化差、难迁移
>
> 一个任务，一个模型，从头开始
>
> 阶段 2：预训练 + 微调
>
> 海量通用数据
>
> …
>
> 文本
>
> 图像
>
> 网页
>
> 预训练
>
> 通用知识
>
> 分类
>
> 问答
>
> 摘要
>
> …
>
> 先用海量通用数据学习通用知识
>
> 再针对具体任务进行微调
>
> 大幅降低从头训练门槛
>
> 先学通用能力，再适配具体任务
>
> 微调适配不同任务
>
> 阶段 3：大模型时代的新痛点
>
> 大模型 / LLM
>
> （数百亿 / 千亿参数）
>
> 任务 A
>
> （全量微调）
>
> 完整模型
>
> 副本 A
>
> 任务 B
>
> （全量微调）
>
> 完整模型
>
> 副本 B
>
> 任务 C
>
> （全量微调）
>
> 完整模型
>
> 副本 C
>
> 为什么又变贵了？
>
> 训练/存储/部署
>
> 模型越大，适配越贵
>
> 例：GPT-3 175B，
>
> FP16 权重约 350 GB / 任务；
>
> 100 个任务 ≈ 35 TB。
>
> 关键问题：能否共享预训练模型，只学习少量任务参数？这就是参数高效微调与 LoRA 要解决的问题
>
> 57
>

### 原 PPT 第 58 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-058.png]]

> [!quote]- 本页可搜索文字
> 现有PEFT方法的三类痛点
>
> Adapter
>
> Prefix-Tuning
>
> Diff Pruning
>
> W = W₀ + ΔW
>
> 仅存储稀疏差值
>
> 冻结主模型，仅训练小型瓶颈层
>
> 参数少，但新增串行计算路径
>
> 在线推理/小batch 时延迟更明显
>
> 参数省了，但推理变慢
>
> 冻结模型，只学习少量前缀表示
>
> 训练可能不稳定，常需额外技巧
>
> 前缀占用可用序列长度
>
> 占用上下文长度且优化不稳定
>
> 最终每个任务只保存极少差值参数
>
> 存储更省，但训练时仍要学习差值与稀疏掩码
>
> 训练过程显存/计算开销依然不低
>
> 共同问题:虽然任务参数变少了，但至少仍有一项成本没有解决
>
> 训练耗时约为全量微调的1.5-2倍
>
> 存储少但训练成本没降低
>
> 58
>

### 原 PPT 第 59 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-059.png]]

> [!quote]- 本页可搜索文字
> 思路启发：从低维适配到低秩更新
>
> 前置工作
>
> Aghajanyan et al.
>
> Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning
>
> ACL-IJCNLP 2021 (Outstanding Paper)
>
> 现象:模型参数很多，但任务适配只需要较少有效自由度。
>
> LoRA的思想迁移
>
> 1
>
> 启发，而未进行严格
>
> 数学推导
>
> LoRA 的进一步假设：
>
> 权重更新 ΔW 具有低内在秩
>
> 对 ΔW 做低秩参数化
>
> 受到前人工作启发，考虑低内在维度问题
>
> 2
>
> 任务适配只需要少数有效方向
>
> 3
>
> 4
>
> 59
>

### 原 PPT 第 60 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-060.png]]

> [!quote]- 本页可搜索文字
> 02
>
> PART TWO
>
> 算法与实验
>
> TONGJI UNIVERSITY
>

### 原 PPT 第 61 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-061.png]]

> [!quote]- 本页可搜索文字
> LoRA的切入点:对权重增量进行低秩参数化
>
> LoRA 方法总览
>
> 冻结大模型已有知识，只学习下游任务所需的低秩权重修正
>
> 蓝色：冻结主权重
>
> 橙色：
>
> 任务增量
>
> 核心直觉：不重新训练整个矩阵，只学习少量有效更新方向。
>
> 如何理解 LoRA？
>
> h = W₀x +
>
> α
>
> r
>
> BAx
>
> 1
>
> 保留基础能力
>
> W₀
>
> Frozen
>
> 预训练知识保留，
>
> 不更新。
>
> 2
>
> 学习任务增量
>
> ΔW = BA
>
> 3
>
> 部署直接合并
>
> W′ = W₀ +
>
> α
>
> r
>
> BA
>
> 只训练两个小矩阵 A、B，
>
> 且 r ≪ min(d, k)
>
> 推理时将低秩更新合并回原权重，不增加网络深度。
>
> 61
>

### 原 PPT 第 62 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-062.png]]

> [!quote]- 本页可搜索文字
> 算法样例分析
>
> 训练：用两个小矩阵学习增量
>
> 单个权重矩阵示例：d = k = 4096，r = 8
>
> 全矩阵更新
>
> LoRA 更新
>
> 4096 × 4096
>
> …
>
> 参数量：16,777,216
>
> d × k
>
> B ∈ ℝ
>
> d×r
>
> 4096
>
> × 8
>
> A ∈ ℝ
>
> r×k
>
> 8 × 4096
>
> 参数量：65,536
>
> 仅为原来的 1/256
>
> 部署：将增量合并回原权重
>
> W = W₀ +
>
> α
>
> r
>
> BA
>
> 1
>
> 任务仅需保存 A、B
>
> 2
>
> 合并后不增加推理计算层
>
> 训练阶段（两支路）
>
> 部署阶段（单一矩阵）
>
> x
>
> x ∈ ℝ
>
> k
>
> W₀
>
> (d × k)
>
> BA
>
> (d × k)
>
> +
>
> h
>
> h ∈ ℝ
>
> d
>
> x
>
> x ∈ ℝ
>
> k
>
> W′ = W₀ +
>
> α
>
> r
>
> BA
>
> (d × k)
>
> h
>
> h ∈ ℝ
>
> d
>
> 62
>

### 原 PPT 第 63 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-063.png]]

> [!quote]- 本页可搜索文字
> 有限预算下的结构设计
>
> LoRA 不只是“低秩”，还强调：在固定参数预算下，如何把低秩更新放在更有效的位置
>
> 在 GPT-3 中针对不同类型注意力权重应用 LoRA 后，在 WikiSQL 和 MultiNLI 数据集上的验证准确率（给定相同数量的可训练参数）。
>
> 原论文 Table 5
>
> 研究问题
>
> Wq,  Wk,  Wv,  Wo
>
> 核心发现
>
> Wq + Wv 整体表现尤其稳定
>
> 方法层面的意义
>
> 1
>
> 结构设计比单纯增大 rank 更重要；
>
> 2
>
> 任务相关信息主要集中在注意力投影中；
>
> 3
>
> LoRA 的有效性依赖“放在哪里”，而不只是参数量多少。
>
> 在相同可训练参数预算下，LoRA 应优先加到哪些注意力权重？
>
> 论文固定可训练参数约 18M，比对不同插入位置。
>
> 结果表明：与其把更大的 rank 集中在单个矩阵，不如在更多注意力投影上使用较小 rank。
>
> 结构创新：固定预算下，优先扩大覆盖范围，而不是提高单点 rank
>
> 63
>

### 原 PPT 第 64 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-064.png]]

> [!quote]- 本页可搜索文字
> 工程与性能创新
>
> 不同于Adapter等方法，LoRA 可以在训练、存储与部署三个环节同时获益
>
> 原论文 Table 4
>
> 不同适配方法在GPT-3 175B上的性能表现。LoRA的表现优于包括全量微调在内的先前方法。
>
> 参数与显存
>
> 1
>
> 可训练参数最高减少约 10000×
>
> 2
>
> GPU 显存需求约降低 3×
>
> 3
>
> 性能表现
>
> 轻量化并没有明显降低性能，甚至更好
>
> 部署优势
>
> W′ = W₀ +
>
> α
>
> r
>
> BA
>
> 任务 checkpoint 可从约 350 GB 降到约 35 MB
>
> 在 WikiSQL、MNLI、SAMSum 等任务上，LoRA 在GPT-3 175B 上达到或超过 Full Fine-Tuning 的效果。
>
> 推理前可将低秩增量直接合并回原权重，因此不像 Adapter 那样增加新的串行计算层，额外推理延迟几乎为0。
>
> 64
>

### 原 PPT 第 65 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-065.png]]

> [!quote]- 本页可搜索文字
> 低秩假设的经验验证
>
> 为了验证低秩假设，LoRA还通过实验说明：任务更新确实高度集中在少数有效方向
>
> 原论文 Table 6
>
> 原论文 Figure 3
>
> 实验结论
>
> r = 1 也能接近较大 rank 的效果。
>
> 对 Wq 与 Wv 进行 LoRA 时，r = 1 / 2 / 4 / 8 / 64 的性能差距并不大，说明很多任务只需要极少数更新方向。
>
> 实验结论
>
> 有效任务信息集中在少数主方向，
>
> 额外 rank 可能更多对应冗余或噪声。
>
> 比较 r = 8 与 r = 64 学到的子空间后发现：最主要的方向高度重合，而后续方向重合度较低。
>
> 65
>

### 原 PPT 第 66 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-066.png]]

> [!quote]- 本页可搜索文字
> 03
>
> PART THREE
>
> 总结与启发
>
> TONGJI UNIVERSITY
>

### 原 PPT 第 67 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-067.png]]

> [!quote]- 本页可搜索文字
> 论文结论
>
> 1
>
> 低秩适配有效且性能不逊于全量微调
>
> 极低的 rank 已经足够
>
> 在注意力层使用效果更好
>
> 显著的训练与存储效率提升
>
> 具有良好的通用性
>
> 在 RoBERTa、DeBERTa、GPT-2、GPT-3 等多种模型和多种任务上，LoRA 达到与全量微调相当甚至更好的性能。
>
> 在多个任务上，r = 1 或 4 即可取得接近最佳的效果，任务相关的权重更新集中在少数方向
>
> 2
>
> 3
>
> 在相同参数预算下，将 LoRA 应用于 Wq 和 Wv 比仅在单个矩阵上使用更有效
>
> 4
>
> 以 GPT-3 175B 为例，可训练参数量减少约10,000×，显存需求降低约 3×
>
> 受到LoRA启发的后续工作
>
> 5
>
> 在不同规模、不同架构和不同任务上均验证了 LoRA 的有效性。
>
> AdaLoRA
>
> (ICLR 2023)
>
> 突破：动态分配 rank，重要的层/矩阵分配更多容量
>
> 基于奇异值分解和重要性度量，自动裁剪不重要的组件
>
> 在固定参数预算下取得比固定 rank 更好的性能
>
> 无需手动为每一层设置 rank
>
> QLoRA
>
> (NeurIPS 2023)
>
> 突破：4-bit 量化基础模型 + LoRA，实现极低显存微调
>
> 提出 4-bit NF4、Double Quantization、Paged Optimizer
>
> 65B 模型可在单张 48GB GPU 上高效微调
>
> 接近 16-bit 全量微调的性能
>
> DoRA
>
> (ICML 2024)
>
> 突破：分解权重的幅值与方向，提升低秩适配能力
>
> 将权重分解为 Magnitude + Direction
>
> 对方向使用 LoRA 进行低秩更新，对幅值单独学习
>
> 在语言和多模态模型上均优于 LoRA
>
> 不增加额外的推理开销
>
> PiSSA
>
> (NeurIPS 2024)
>
> 突破：基于主奇异方向的初始化，加速收敛并提升性能
>
> 使用 SVD 提取原权重的主奇异方向进行初始化
>
> 比随机初始化的 LoRA 收敛更快、效果更好
>
> 有限的低秩容量应该分配给更重要的位置
>
> 参数高效不等于显存高效
>
> 进一步研究LoRA到底在改变权重的什么性质，使其更接近全量微调
>
> 低秩子空间的选择很重要
>
> 论文总结与研究演进
>
> 67
>

### 原 PPT 第 68 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-068.png]]

> [!quote]- 本页可搜索文字
> 感谢倾听！
>
> TONGJI UNIVERSITY
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-EA33AYCQ - EgoX  Egocentric Video Generation from a Single Exocentric Video|EgoX: Egocentric Video Generation from a Single Exocentric Video]] — 强关联；对方摘要提到模型 LoRA（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-WE2HF7Y8 - Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning|Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning]] — 强关联；共同研究内容：低秩与参数高效微调、语言模型与语言表征。
- [[Zotero Knowledge/Papers/ZK-RAH7V3N7 - Low-Rank Rescaled Vision Transformer Fine-Tuning  A Residual Design Approach|Low-Rank Rescaled Vision Transformer Fine-Tuning: A Residual Design Approach]] — 中关联；共同研究内容：低秩与参数高效微调。
- [[Zotero Knowledge/Papers/ZK-Y364L7RZ - MultiLoReFT  Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning|MultiLoReFT: Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning via Low-Rank Representation Fine-Tuning]] — 中关联；共同研究内容：低秩与参数高效微调。

<!-- content-relations:end -->
