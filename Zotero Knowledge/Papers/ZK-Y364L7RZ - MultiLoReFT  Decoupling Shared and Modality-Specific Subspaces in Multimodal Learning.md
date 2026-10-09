---
type: "literature"
title: "MultiLoReFT: Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning via Low-Rank Representation Fine-Tuning"
aliases: ["MultiLoReFT"]
zotero_keys: ["Y364L7RZ"]
year: 2026
authors: ["Tonekaboni, Sana", "Schuster, Viktoria", "Uhler, Caroline"]
venue: "ICML 2026"
doi: ""
url: "https://arxiv.org/abs/2607.16789"
collections: ["02 Representation & Perception/Vision-Language Representation", "90 Projects/Pattern Recognition Course/Project 1/Group 2", "06 Alignment & Reliability/Adaptation & Generalization", "06 Alignment & Reliability/Representation Alignment"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2", "concept/跨模态对齐与模态间隙", "concept/微调策略与泛化鲁棒性", "concept-primary/跨模态对齐与模态间隙"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [21, 38]
imported_at: "2026-10-03"
---

# MultiLoReFT: Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning via Low-Rank Representation Fine-Tuning

[在 Zotero 打开](zotero://select/library/items/Y364L7RZ) · [论文来源](https://arxiv.org/abs/2607.16789) · [论文 PDF](https://arxiv.org/pdf/2607.16789)

## 文献导读

使用低秩表示微调分离共享和模态特异子空间，并以自适应剪枝决定子空间维度。结合可解释性、下游预测与缺失模态实验检查解耦是否有效。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Vision-Language Representation/索引|02 Representation & Perception/Vision-Language Representation]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-SE2PQKZ8 - LoRA  Low-Rank Adaptation of Large Language Models|LoRA]]
- [[Zotero Knowledge/Papers/ZK-3D4I5WS2 - Understanding Geometric Representations in Self-Supervised Vision Transformers via Su|Geometric Subspace Intervention]]
- [[Zotero Knowledge/Papers/ZK-BYZ75H5L - Connect, Collapse, Corrupt  Learning Cross-Modal Tasks with Uni-Modal Data|C3]]

## 原始摘要

Real-world perception and decision making are inherently multimodal, integrating complementary signals across modalities. However, training multimodal models faces two main obstacles. First, collecting large-scale, well-aligned paired multimodal datasets is often impractical, making end-to-end multimodal training difficult. Second, existing multimodal representations frequently entangle information shared across modalities with modality-specific information, hindering interpretability and control. We introduce MultiLoReFT, an efficient and scalable low-rank representation fine-tuning framework for multimodal learning with pretrained unimodal models. MultiLoReFT extends low-rank adaptation to the multimodal setting and learns interpretable projection subspaces that decouple shared and modality-specific information. Across simulated and real-world benchmarks, it produces representations that support multimodal prediction while explicitly revealing how shared and modality-specific information is distributed across modalities.

来源：[论文官方页面](https://arxiv.org/abs/2607.16789)。

会议信息已对照 [ICML 2026 官方论文列表](https://icml.cc/Downloads/2026)核对。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 21–38 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 21 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-021.png]]

> [!quote]- 本页可搜索文字
> MultiLoReFT: Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning via Low-Rank Representation Fine-Tuning
>
> 通过低秩表示微调实现多模态学习中共享子空间与模态特异性子空间的解耦
>
> ICML 2026 
>
> 汇报人：2612196 肖颖
>

### 原 PPT 第 22 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-022.png]]

> [!quote]- 本页可搜索文字
> 研究动机：多模态融合与信息来源解析
>
> 1 研究动机
>
> 02 / 19
>
> 多模态数据提供互补线索，但配对数据难收集，且模型内部的信息分工常不可见。
>
> 1.数据现实
>
> 医疗等观察性场景中，大规模、严格配对的数据往往稀缺或昂贵。
>
> 2.模型机会
>
> 单模态预训练模型已积累丰富表征，可复用到小样本多模态任务。
>
> 研究目标
>
> 在保留单模态知识的同时学习跨模态共性，并显式识别各模态独有信号。
>
> 核心问题
>
> 能否以较少可训练参数，将“共同信息”和“模态特异信息”分开表示？
>

### 原 PPT 第 23 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-023.png]]

> [!quote]- 本页可搜索文字
> 现存痛点：现有融合方法难以区分共享与模态特异信息
>
> 2 现存痛点
>
> 03 / 19
>
> 三类瓶颈彼此关联，限制小样本场景中的可解释性与可靠性。
>
> 1.配对数据少
>
> 端到端多模态训练依赖大规模对齐样本，现实数据常达不到。
>
> 2.微调整体昂贵
>
> 全量微调成本高；简单拼接、注意力或对比学习通常不提供清晰的信息分解。
>
> 3.信息泄露
>
> 共享与模态私有因素可能混在同一表示里，难以判断模型依赖了什么。
>
> 缺失模态时，若单模态表征没有保留跨模态可预测信息，性能也可能下降。
>

### 原 PPT 第 24 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-024.png]]

> [!quote]- 本页可搜索文字
> 模型结构：共享子空间与私有子空间并行更新
>
> 3 本文解决方案
>
> 05 / 19
>
> 左：低秩投影内学习表征编辑　　右：把输出解释为共享 zₛ 与模态独有 zₘ₁、zₘ₂
>

### 原 PPT 第 25 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-025.png]]

> [!quote]- 本页可搜索文字
> 06 / 19
>
> Rs: shared projection matrix
>
> Rm1: modality 1 unique subspace
>
> Rm1: modality 1 unique subspace
>
> Rsh1: 原本投影到 shared space 里的特征
>
> δ1: fs1(h1)表示模型学出来的更合适的 shared 表示
>
> 模型结构：共享子空间与私有子空间并行更新
>

### 原 PPT 第 26 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-026.png]]

> [!quote]- 本页可搜索文字
> 模型结构：共享子空间与私有子空间并行更新
>
> 07 / 19
>
> 如果两个模态都存在，最终 shared representation zs可以由两者的 shared projection 做平均；如果只剩一个模态，就使用那个模态的 shared projection
>

### 原 PPT 第 27 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-027.png]]

> [!quote]- 本页可搜索文字
> 训练目标：分离子空间，同时保留原始信息
>
> 08 / 19
>
> 总损失由三个互补约束组成
>
> 独立损失
>
> HSIC 降低共享与私有表征之间的非线性依赖，也抑制两个私有子空间间的信息泄漏。
>
> 正交损失
>
> 约束共享投影与各私有投影的基向量不重叠，减少表示空间中的方向干扰。
>
> 互信息保留
>
> InfoNCE 让更新后的投影仍包含原单模态嵌入的信息，并对齐跨模态共享内容。
>
> L=λ1Lindep+λ2Lorth+λ3LMI
>
> HSIC是两个随机变量之间统计相依性的非参数度量。给定具有特征核K和L ( e.g. ,高斯RBF或拉普拉斯)的随机变量X和Y，HSIC( X , Y) = 0当且仅当X和Y是统计独立的.
>

### 原 PPT 第 28 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-028.png]]

> [!quote]- 本页可搜索文字
> 自适应剪枝：让子空间维度由信息量决定
>
> 09 / 19
>
> 核心目的：自动决定 shared / modality-specific subspace 需要多少维，避免手工设置 rank
>
> 关键步骤
>
> 对 Rs,Rm1,Rm2 做SVD
>
> 找出σi<ℇ的低信息维度
>
> 每次最多剪掉当前 rank 的 10%
>
> 同步压缩对应的 transformation f
>
> 设计意义：保留主要信息方向，删除冗余维度，在不明显损失表示质量的前提下降低参数量，并减少信息泄漏
>

### 原 PPT 第 29 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-029.png]]

> [!quote]- 本页可搜索文字
> MultiLoReFT Training：完整训练流程
>
> 10 / 19
>
> 核心流程
>
> Frozen encoder 提取h1,h2
>
> 通过 shared / modality-specific low-rank edits 得到 φ1，φ2
>
> 得到 zs,zm1,zm2
>
> 优化三类目标：
>
> Independence：减少信息重复
>
> Orthogonality：减少子空间重叠
>
> Mutual Information：避免有用信息丢失
>
> 50 epoch warm-up 后，满足条件时调用 Algorithm 1
>
> 持续训练直到收敛
>

### 原 PPT 第 30 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-030.png]]

> [!quote]- 本页可搜索文字
> 实验验证思路：解耦效果、预测能力与缺失模态表现
>
> 5 论文如何论证有效性
>
> 11 / 19
>
> 解耦效果
>
> 共享信息与模态特异信息是否进入对应子空间？
>
> 预测能力
>
> 解耦后的表示能否用于下游多模态预测？
>
> 缺失模态表现
>
> 只保留一个模态时，表示是否仍然有效？
>
> 对照公平
>
> 基线共用同一组预训练单模态嵌入，差异聚焦在解耦/融合模块。
>

### 原 PPT 第 31 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-031.png]]

> [!quote]- 本页可搜索文字
> 模拟数据：MultiLoReFT 更能把共享因素留在共享空间
>
> 12 / 19
>
> 实验目的：验证 MultiLoReFT 是否真的把 shared information 和 modality-specific information 分开。
>
> Shared label：只应在 shared subspace zs中形成明显聚类
>
> Modality 1 label：只应在zm1中形成明显聚类
>
> Modality 2 label：只应在zm2中形成明显聚类
>
> 其他不相关子空间应尽量无明显结构。
>
> 结论：不同类型的信息被集中到对应子空间中，说明 MultiLoReFT 能减少 information leakage，实现显式 disentanglement。
>
> Visualization of Learned Shared and Modality-Specific Subspaces
>

### 原 PPT 第 32 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-032.png]]

> [!quote]- 本页可搜索文字
> 真实数据：可解释的信息分工能对应到具体模态线索
>
> 13 / 19
>
> Flickr30K-Multi
>
> 文本特异分量预测语言标签：99.7%
>
> 共享分量：77.2%
>
> CREMA-D
>
> 视频 / 音频私有分量分别捕获年龄、语句身份等线索。
>
> 在 Crema-D 和 Flickr30K 上观察不同属性在各子空间中的分布
>
> 与模态相关的信息主要集中在对应 modality-specific subspace
>
> shared subspace 对不相关的 modality-specific 属性更弱
>
> PCA Visualization
>

### 原 PPT 第 33 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-033.png]]

> [!quote]- 本页可搜索文字
> 真实数据：可解释的信息分工能对应到具体模态线索
>
> 14 / 19
>
> shared space 更倾向找到“人在切割/处理材料”这类语义相近样本；image-specific space 更容易找到“木头、树木、视觉纹理”等相似内容
>
> Nearest-Neighbor Retrieval
>
> Shared space：检索到高层语义相似的样本
>
> Image-specific space：检索到视觉细节相似的样本
>
> 说明 shared space 学到“跨模态共同语义”
>
> specific space 学到“单模态特有细节”
>

### 原 PPT 第 34 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-034.png]]

> [!quote]- 本页可搜索文字
> 下游预测：简单拼接微调表示，在四组任务中均领先或持平
>
> 5 论文如何论证有效性
>
> 15 / 19
>
> 串联微调后的表示Φ 1和Φ 2并训练一个轻量级逻辑回归器一致优于一系列基线。
>
> 提升幅度因任务而异；真实数据上的优势较小，UR-FUNNY raw-video 结果与 Cross-attention 接近。
>
> Multiplicative Interactions
>

### 原 PPT 第 35 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-035.png]]

> [!quote]- 本页可搜索文字
> 消融实验：缺失模态时剩余模态的微调表示仍携带跨模态信息
>
> 5 论文如何论证有效性
>
> 16 / 19
>
> 实验对照
>
> 每次移除一个模态，只用剩余模态预测。
>
> h：原始预训练表示
>
> Φ：MultiLoReFT 微调表示
>
> 三个数据集、两种缺失方向上，Φ 的准确率均高于 h。
>
> Downstream classification accuracy under missingmodality inference
>

### 原 PPT 第 36 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-036.png]]

> [!quote]- 本页可搜索文字
> 核心创新：面向多模态解耦的低秩表示微调框架
>
> 4 核心创新点
>
> 17 / 19
>
> 方法创新
>
> 将 LoReFT 扩展到多模态表示学习，显式构建共享子空间与模态特异子空间，并通过低秩表示干预实现轻量微调。
>
> 解耦机制
>
> 联合使用三类loss实现 shared / specific 信息分离：
>
> HSIC：降低 shared 与 specific 表示之间的统计依赖
>
> Orthogonality：减少不同子空间的几何重叠
>
> Mutual Information：保证解耦过程中不过度丢失原始信息
>
> 自适应结构
>
> 提出 Adaptive Rank Pruning，根据奇异值动态压缩 Rs,Rm1,Rm2 的有效维度。
>
> 避免人工固定 rank，同时去除冗余表示，提高参数效率和解耦质量。
>
> 有效性证据
>
> Synthetic data：有 ground truth，可直接验证 shared / specific 信息是否进入正确子空间
>
> Real-world data：通过 PCA 和 nearest-neighbor 验证语义可解释性
>
> Downstream tasks：解耦后仍保持或提升预测性能
>
> Missing modality：单一模态缺失时，微调后的表示更稳健
>

### 原 PPT 第 37 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-037.png]]

> [!quote]- 本页可搜索文字
> 结论与启发：把“融合”推进到可检查的信息分工
>
> 6 结论与启发
>
> 18 / 19
>
> 论文结论
>
> 冻结预训练单模态编码器，并通过低秩表示微调显式分离共享与模态特异信息，可在较低参数开销下兼顾多模态预测、表示可解释性与缺失模态鲁棒性。
>
> 启发
>
> 评估多模态模型时，不应只看最终预测性能，还应检查共享因素是否真正集中在 shared subspace，以及模态缺失时剩余表示是否仍保留有效的跨模态信息。
>
> 论文边界
>
> • 主实验以双模态为主；更多模态的部分共享因素尚难解释与验证。
>
> • 方法上限受预训练单模态编码器的表示质量与任务相关信息覆盖范围限制。
>
> • 真实数据上的下游性能提升幅度因任务而异；解耦效果的验证仍依赖可用的属性或语义标签。
>

### 原 PPT 第 38 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-038.png]]

> [!quote]- 本页可搜索文字
> 谢谢您的观看
>
> 汇报人：2612196 肖颖
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-RAH7V3N7 - Low-Rank Rescaled Vision Transformer Fine-Tuning  A Residual Design Approach|Low-Rank Rescaled Vision Transformer Fine-Tuning: A Residual Design Approach]] — 中关联；共同研究内容：低秩与参数高效微调。
- [[Zotero Knowledge/Papers/ZK-3D4I5WS2 - Understanding Geometric Representations in Self-Supervised Vision Transformers via Su|Understanding Geometric Representations in Self-Supervised Vision Transformers via Subspace Intervention]] — 中关联；共同研究内容：低秩与参数高效微调。
- [[Zotero Knowledge/Papers/ZK-SE2PQKZ8 - LoRA  Low-Rank Adaptation of Large Language Models|LoRA: Low-Rank Adaptation of Large Language Models]] — 中关联；共同研究内容：低秩与参数高效微调。

<!-- content-relations:end -->

<!-- research-integration:start -->
## 研究主题入口

- [[Zotero Knowledge/Topics/02 Representation & Perception/Vision-Language Representation/索引|02 Representation & Perception/Vision-Language Representation]]
- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Adaptation & Generalization/索引|06 Alignment & Reliability/Adaptation & Generalization]]
- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]]

## 概念比较入口

- [[Zotero Knowledge/Concepts/跨模态对齐与模态间隙|跨模态对齐与模态间隙]]
- [[Zotero Knowledge/Concepts/微调策略与泛化鲁棒性|微调策略与泛化鲁棒性]]
<!-- research-integration:end -->
