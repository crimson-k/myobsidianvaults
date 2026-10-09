---
type: "literature"
title: "Low-Rank Rescaled Vision Transformer Fine-Tuning: A Residual Design Approach"
aliases: ["RLRR"]
zotero_keys: ["RAH7V3N7"]
year: 2024
authors: ["Dong, Wei", "Zhang, Xing", "Chen, Bihui", "Yan, Dawei", "Lin, Zhijun", "Yan, Qingsen", "Wang, Peng", "Yang, Yang"]
venue: "CVPR 2024"
doi: ""
url: "https://arxiv.org/abs/2403.19067"
collections: ["06 Alignment & Reliability/Adaptation & Generalization", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1", "concept/微调策略与泛化鲁棒性", "concept-primary/微调策略与泛化鲁棒性"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [79, 98]
imported_at: "2026-10-03"
---

# Low-Rank Rescaled Vision Transformer Fine-Tuning: A Residual Design Approach

[在 Zotero 打开](zotero://select/library/items/RAH7V3N7) · [论文来源](https://arxiv.org/abs/2403.19067) · [论文 PDF](https://arxiv.org/pdf/2403.19067)

## 文献导读

以残差式低秩重缩放适配视觉 Transformer 权重，平衡预训练知识保留与下游适配。可与 LoRA 比较参数化方式、插入位置和相同预算下的实验。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Adaptation & Generalization/索引|06 Alignment & Reliability/Adaptation & Generalization]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-SE2PQKZ8 - LoRA  Low-Rank Adaptation of Large Language Models|LoRA]]
- [[Zotero Knowledge/Papers/ZK-W8UL68IN - Fine-Tuning can Distort Pretrained Features and Underperform Out-of-Distribution|LP-FT]]

## 原始摘要

Parameter-efficient fine-tuning for pre-trained Vision Transformers aims to adeptly tailor a model to downstream tasks by learning a minimal set of new adaptation parameters while preserving the frozen majority of pre-trained parameters. Striking a balance between retaining the generalizable representation capacity of the pre-trained model and acquiring task-specific features poses a key challenge. Currently, there is a lack of focus on guiding this delicate trade-off. In this study, we approach the problem from the perspective of Singular Value Decomposition (SVD) of pre-trained parameter matrices, providing insights into the tuning dynamics of existing methods. Building upon this understanding, we propose a Residual-based Low-Rank Rescaling (RLRR) fine-tuning strategy. This strategy not only enhances flexibility in parameter tuning but also ensures that new parameters do not deviate excessively from the pre-trained model through a residual design. Extensive experiments demonstrate that our method achieves competitive performance across various downstream image classification tasks, all while maintaining comparable new parameters. We believe this work takes a step forward in offering a unified perspective for interpreting existing methods and serves as motivation for the development of new approaches that move closer to effectively considering the crucial trade-off mentioned above. Our code is available at \href{ this https URL }{ this https URL }.

来源：[论文官方页面](https://arxiv.org/abs/2403.19067)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 79–98 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 79 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-079.png]]

> [!quote]- 本页可搜索文字
> Low-Rank Rescaled Vision Transformer Fine-Tuning：
>
> A Residual Design Approach
>
> 低秩重缩放视觉Transformer微调：一种残差设计方法
>
> IEEE/CVF  CVPR  2024
>
> Wei Dong, Xing Zhang, Bihui Chen, Dawei Yan, Zhijun Lin, 
>
> Qingsen Yan, Peng Wang(通讯), Yang Yang
>
> 电子科技大学   西安建筑科技大学    西北工业大学
>
> github.com/zstarN70/RLRR  ·  arXiv: 2403.19067
>
>                 汇报人：马睿辰
>
>               汇报时间：2026年9月23日
>

### 原 PPT 第 80 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-080.png]]

> [!quote]- 本页可搜索文字
> CONTENTS
>
> 目 录
>
> 01
>
> 研究动机
>
> 为什么做这篇工作：PEFT的权衡困境
>
> 02
>
> 现存痛点
>
> 现有方法只调单一维度，缺乏统一重缩放
>
> 03
>
> 本文解决方案
>
> 残差+低秩重缩放+平移
>
> 04
>
> 核心创新点
>
> 理论 / 方法 / 场景 /性能四类创新
>
> 05
>
> 论证有效性
>
> VTAB-1k 主结果 消融 扩展实验
>
> 06
>
> 结论与启发
>
> 贡献、局限与启示
>
> RLRR · 低秩重缩放 ViT 微调
>
> 02 / 19
>

### 原 PPT 第 81 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-081.png]]

> [!quote]- 本页可搜索文字
> 一、研究动机
>
> 背景：从单独训练到共享预训练+微调
>
> 范式转变：从任务专属训练，转向共享预训练骨干上的下游微调。
>
> 预训练规模扩大：ViT/Swin 配合 ImageNet-1K/21K、JFT-300M 等大规模数据。
>
> 全量微调代价高：存储与计算开销大，小样本下游还容易过拟合。
>
> PEFT 的目标：冻结大部分骨干，只学习少量参数，兼顾效率与适配。
>
> 大模型微调三要素
>
> 1.预训练骨干  提供通用表征
>
> 2.少量可训练参数
>
> 3.下游任务目标
>
> 核心矛盾
>
> 适应性 vs 保真度
>
> 演进主线
>
> 海量数据预训练
>
> 共享骨干微调
>
> PEFT 轻量适配
>
> RLRR · 低秩重缩放 ViT 微调
>
> 03 / 19
>

### 原 PPT 第 82 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-082.png]]

> [!quote]- 本页可搜索文字
> 一、研究动机
>
> 动机：被忽视的权衡
>
> 核心观察
>
> PEFT的关键不是“能不能适配”，而是如何在保留预训练泛化能力与获取任务特征之间取得平衡。
>
> 本文切入点
>
> 用SVD拆解预训练参数矩阵，分析不同PEFT方法究竟改变了哪些奇异分量。
>
> 冗余性：LoRA等低秩方法有时能超过全量微调，说明参数更新存在冗余。
>
> 现有不足：方法多关注高效适配，较少显式控制对预训练表征的扰动。
>
> 本文目标：用统一视角设计一种更平衡、更可控的参数高效微调方法。
>
> 偏重适应性
>
> 过拟合、遗忘通用知识
>
> RLRR 残差设计
>
> 在两端之间取平衡
>
> 偏重保真度
>
> 迁移不足、适配乏力
>
> RLRR · 低秩重缩放 ViT 微调
>
> 04 / 19
>

### 原 PPT 第 83 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-083.png]]

> [!quote]- 本页可搜索文字
> 二、现存痛点
>
> 现存痛点：现有 PEFT 难以同时兼顾保真与适配
>
> Adapter (2019)
>
> 瓶颈Wdown作用于右奇异向量 ud
> 可能会破坏右奇异矩阵正交性（Eq.8）
>
> LoRA (2021)
>
> W+BA低秩旁路
> 大D时弱适配、欠扰动谱（Eq.10）
>
> VPT (2022)
>
> prompt与左奇异向量dd交互
> 可能过度偏离预训练（Eq.12）
>
> SSF (2022)
>
> 输出特征 (XW+b)⊙s
> 扰动右奇异向量ud与谱（Eq.14）
>
> AdaptFormer (2022)
>
> 并行adapter同Adapter的右奇异正交缺陷
>
> FacT (2023)
>
> 张量分解重组参数
> 低秩因子扰动谱结构
>
> ARC (2023)
>
> 跨层共享 adapter
> 独立缩放因子扰动谱
>
> 本文 RLRR (2024)
>
> SVD视角+残差
> 行/列双向重缩放+平移（Eq.16-20）
>
> 核心矛盾：LoRA对全谱扰动较弱，容易欠适配；Adapter / VPT / SSF直接改变奇异方向或谱，容易过度偏离预训练。
>
> RLRR的切入点：用残差保护原始通路，再对权重做行、列双向低秩重缩放。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 05 / 19
>

### 原 PPT 第 84 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-084.png]]

> [!quote]- 本页可搜索文字
> 二、现存痛点
>
> 关键洞察：把权重矩阵拆成奇异分量
>
> 标准记号 σ / u / v ｜ 论文记号 λ / ⃗d（左奇异向量）/ ⃗u（右奇异向量），Table 1 沿用后者
>
> 秩一分量：           = 左奇异向量×奇异值×右奇异向量。
>
> λd表示分量能量；奇异值谱反映矩阵的低秩结构与冗余。
>
> 因此，微调可以被拆成三类变化：缩放能量、改变输出方向、改变输入方向。
>
> 微调：改动哪些维度
>
> 1. λ幅度 —— 缩放分量能量
>
> 2. 左奇异方向 —— 重组输出
>
> 3. 右奇异方向 —— 重组输入
>
> 统一视角：用同一组正交坐标定位Adapter / LoRA / VPT / SSF的扰动位置。
>
> 核心追问：能否同时、受控地调整左右奇异方向与奇异值幅度，同时不远离预训练模型？
>
> RLRR · 低秩重缩放 ViT 微调
>
> 06 / 19
>

### 原 PPT 第 85 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-085.png]]

> [!quote]- 本页可搜索文字
> 二、现存痛点
>
> 用 SVD 框架统一解读现有方法
>
> 方法
>
> SVD 视角：微调改动了什么
>
> 影响的奇异分量
>
> LoRA
>
> WdownWup 对每个奇异分量适配微弱，D大时仅轻微扰动谱（Eq.10）
>
> 全谱弱扰动欠适配
>
> SSF（scale & shift）
>
> udᵀ⊙s逐元素缩放右奇异向量，λd⊙s同时扰动谱（Eq.14）
>
> ud方向σ幅度
>
> Adapter
>
> Wdown 直接作用右奇异向量ud，破坏右奇异矩阵正交性（Eq.8）
>
> ud 方向+σ幅度
>
> VPT
>
> promptΘ与左奇异向量dd 直接交互，过度影响调参（Eq.12）
>
> dd方向+σ幅度
>
> LoRA
>
> SSF（scale & shift）
>
> 现存痛点：LoRA全谱弱扰动，欠适配；Adapter / VPT / SSF直接扰动奇异方向与谱 → 易过适配。缺乏受控的行、列双向统一重缩放来平滑权衡保真与适配——这正为 RLRR 留出空间。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 07 / 19
>
> Adapter  Wdown Wup（Eq.8）
>
> VPT  prompt Θ（Eq.12）
>

### 原 PPT 第 86 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-086.png]]

> [!quote]- 本页可搜索文字
> 二、现存痛点
>
> PEFT 方法的 SVD 统一解释框架
>
> 来源：论文 Table 1 —— Adaptation / LoRA / Prompt / scale&shift 各方法的奇异谱分析
>
> RLRR · 低秩重缩放 ViT 微调
>
> 08 / 19
>

### 原 PPT 第 87 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-087.png]]

> [!quote]- 本页可搜索文字
> 三、本文解决方案
>
> RLRR：残差设计+低秩重缩放+平移
>
> 残差定义
>
> 等价相乘
>
> 逐元素(Eq.19)
>
> 秩一关键
>
> 残差性质
>
> 三个可学习量
>
> sleft（dout×1）行缩放
>
> sright（din×1）列缩放
>
> f（dout×1）平移
>
> 参数开销
>
> 残差设计是关键：
>
> W′ = (1+sleft srightᵀ)⊙W       b′=b+f
>
> 逐元素：W′ij = (1+sleft [i]·sright[j]) Wij
>
> 常数项 1 保留预训练通路；缩放与平移归零时，W′≡W。新增参数仅0.33M，约为Full微调参数量的0.38%，推理时可吸收进权重。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 09 / 19
>

### 原 PPT 第 88 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-088.png]]

> [!quote]- 本页可搜索文字
> 三、本文解决方案
>
> RLRR 作用位置：MHA / FFN 权重矩阵
>
> Figure 1：对任意权重 W 做「冻结 + 低秩重缩放 + 残差」
>
> 权重侧：对每层的Q/K/V/输出投影与FFN两个全连接层施加RLRR。
>
> 特征侧：LayerNorm与patch embedding 输出沿用 scale&shift。
>
> 覆盖范围：每层 ViT encoder的6个权重矩阵，共12层。
>
> 直观理解：每个模块仍保持 x+f(x) 的残差通路，只对 f() 内的权重做可控重缩放。
>
> 覆盖范围：右侧已列出每层6个权重矩阵，共12层。
>
> 相对 SSF：RLRR 额外在权重上进行行、列双向重缩放，同时调整左右奇异方向与谱幅度。
>
> 残差语义：每个模块仍保持 x + f(x) 的前向通路，只对 f() 内的投影权重做可控重缩放。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 10 / 19
>

### 原 PPT 第 89 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-089.png]]

> [!quote]- 本页可搜索文字
> 四、核心创新点
>
> 核心创新点：理论 / 方法 / 场景 / 性能
>
> 理论创新
>
> 用SVD统一框架系统分析PEFT方法，定位各方法扰动了哪个奇异方向（左 dd/右 ud）与谱 λd，揭示过/欠适配根源
>
> 方法创新
>
> 残差设计+秩一重缩放（行、列同时）+平移，缩放归零时W′≡W，初始化即不偏离预训练模型
>
> 场景创新
>
> 验证于 ViT-L/H、Swin 层级骨干、MAE/MoCo v3自监督权重、CNN卷积核等多场景，泛化性强
>
> 性能创新
>
> VTAB-1k 74.5%/75.1%、FGVC 90.4%/91.0% 取得有竞争力的结果；FGVC5 个数据集×2 种骨干共 10 项评测中，7项取得最优；新增参数仅 0.33M（约 Full 的 0.38%）
>
> 理论 → 方法 → 场景 → 性能
>
> 四类创新形成完整链条：SVD统一视角解释问题，残差秩一重缩放解决问题，多骨干与多预训练来源验证泛化，VTAB-1k/FGVC结果验证有效性。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 11 / 19
>

### 原 PPT 第 90 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-090.png]]

> [!quote]- 本页可搜索文字
> 五、论证有效性
>
> 实验设置与VTAB-1k主结果
>
> 骨干网络
>
> ViT-B/16
> ImageNet-21k 预训练
>
> 评测基准
>
> VTAB-1k  19 任务
> Natural/Spec./Struct.
>
> 对比方法
>
> Full/Linear  Adapter
> LoRA/VPT/SSF/FacT/ARC
>
> 训练细节
>
> AdamW  cosine  100 ep
> 每任务 1000 张样本
>
> 74.5%
>
> RLRR（plain ViT-B/16）
>
> 75.1%
>
> RLRR（AugReg 增强骨干）
>
> 结果：plain ViT-B/16 为 74.5%，AugReg骨干为 75.1%。
>
> 优势：相对同一骨干下的最优PEFT基线，plain 提升1.1个百分点，AugReg 提升0.8个百分点。
>
> 效率：新增参数仅 0.33M，约为 Full 微调的 0.38%，与LoRA同量级。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 12 / 19
>

### 原 PPT 第 91 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-091.png]]

> [!quote]- 本页可搜索文字
> 五、论证有效性
>
> 论文原表：VTAB-1k上与各基线/SOTA的完整对比
>
> 来源：论文 Table 2 ——  在 VTAB-1k 上对比 RLRR 与 SOTA 参数高效微调方法。全部方法使用 ImageNet-21k 预训练 ViT-B/16；带 * 的方法采用 AugReg 增强骨干。粗体为 SOTA，下划线为次优。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 13 / 19
>

### 原 PPT 第 92 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-092.png]]

> [!quote]- 本页可搜索文字
> 五、论证有效性
>
> 消融：各组件的独立贡献
>
> 左侧缩放sleft
>
> 仅left缩放（无残差）89.2%；过度单侧重缩放仍损害泛化
>
> 右侧缩放sright
>
> 仅right缩放（无残差）89.3%；单侧优于双侧无残差
>
> 双侧缩放(无残差)
>
> left+right都开但无残差→88.9%，过度重缩放损害泛化
>
> 残差项
>
> 加残差后趋势反转，双侧+残差最优 90.4%（Table 6 FGVC）
>
> 插入模块/层数
>
> 随层数增加精度上升；MHA+FFN+LayerNorm 全模块最优（Fig 2 CIFAR-100）
>
> 关键结论：无残差时，双侧缩放反而低于单侧；加入残差后，趋势反转，双侧缩放+残差达到最高 90.4%。
>
> 残差项同时保留预训练表征与重缩放的适配自由度，是性能提升的关键。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 14 / 19
>

### 原 PPT 第 93 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-093.png]]

> [!quote]- 本页可搜索文字
> 五、论证有效性
>
> 论文图表：插入位置与组件组合的消融
>
> Figure 2 —— CIFAR-100 上不同模块 / 层数组合
>
> Table 6 —— FGVC 上左/右缩放 × 残差组合
>
> 关键发现：无残差时单侧缩放优于双侧；加入残差后，双侧缩放最优。
>
> 残差项保护原始表征，使重缩放可以更灵活地适配下游任务。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 15 / 19
>

### 原 PPT 第 94 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-094.png]]

> [!quote]- 本页可搜索文字
> 五、论证有效性
>
> 扩展实验：更大骨干、Swin、自监督 、CNN
>
> 更大骨干 (RQ2)
>
> ViT-L/ViT-H随规模扩大
>
> 仍保持竞争力（ViT-L +2.7%、ViT-H +2.6%）
>
> 可扩展性强
>
> 层级结构 (RQ3)
>
> Swin Transformer骨干
>
> 适配移位窗口层级结构
>
> 验证非标准ViT通用性
>
> 自监督预训练 (RQ6)
>
> MAE/MoCo v3自监督权重
>
> 同样可被低秩重缩放
>
> 拓宽预训练来源
>
> Figure 3 —— 卷积核拼接为权重矩阵，RLRR 可迁移到 CNN
>
> RLRR在更大骨干、层级结构、自监督权重和CNN卷积核上均保持有效，说明它不是只针对ViT-B/16的特例。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 16 / 19
>

### 原 PPT 第 95 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-095.png]]

> [!quote]- 本页可搜索文字
> 六、结论与启发
>
> 总结：四条核心贡献
>
> 1
>
> 统一分析框架
>
> 基于SVD透视预训练参数矩阵，系统理解主流PEFT的调参动力学。
>
> 2
>
> 权衡探索
>
> 填补空白，显式探索保留泛化能力vs高效适配的权衡。
>
> 3
>
> RLRR 方法
>
> 残差设计+低秩重缩放+平移，兼顾灵活性与保真度。
>
> 4
>
> 全面实验
>
> VTAB-1k等多任务上与SOTA相当，且新增参数极少。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 17 / 19
>

### 原 PPT 第 96 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-096.png]]

> [!quote]- 本页可搜索文字
> 六、结论与启发
>
> 思考：优点、局限与启发
>
> 优点
>
> SVD视角统一，解释力强
>
> 残差设计：初始化即不偏离
>
> 权重侧行+列细粒度重缩放
>
> 参数高效（约 Full 的 0.38%）
>
> VTAB-1k等多骨干验证扎实
>
> 局限
>
> 聚焦图像分类，未及检测/分割
>
> 秩数/缩放结构需人工设定
>
> SVD分析偏定性、缺严格理论
>
> 对表征扰动的量化有限
>
> 与更大模型的效率对比不足
>
> 启发
>
> 可视为权重侧SSF+低秩残差
>
> 提供可控扰动微调手段
>
> 与LoRA秩对照天然契合
>
> 可量化微调对表征的重写程度
>
> 值得复现并检验秩一假设
>
> 论文展望：可迁移至 NLP Transformer
>
> RLRR通过“残差+秩一重缩放”控制权重扰动，在参数效率、预训练保真与下游适配之间取得平衡。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 18 / 19
>

### 原 PPT 第 97 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-097.png]]

> [!quote]- 本页可搜索文字
> 参考文献与资源
>
> 参考文献与资源
>
> 论文：W. Dong, X. Zhang, B. Chen, D. Yan, Z. Lin, Q. Yan, P. Wang, Y. Yang. “Low-Rank Rescaled Vision Transformer Fine-Tuning: A Residual Design Approach.” IEEE/CVF CVPR 2024.
>
> 代码：https://github.com/zstarN70/RLRR
>
> arXiv：https://arxiv.org/abs/2403.19067
>
> 要点回顾
>
> 从预训练参数矩阵的SVD出发，RLRR用残差式低秩重缩放提升调参灵活性，同时避免新参数过度偏离预训练模型。论文在图像分类任务上以接近LoRA的参数量取得有竞争力的结果。
>
> RLRR · 低秩重缩放 ViT 微调
>
> 19 / 19
>

### 原 PPT 第 98 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-098.png]]

> [!quote]- 本页可搜索文字
> 感谢老师与各位同学
>
> 欢迎提问与交流探讨
>
> 汇报人：2612134马睿辰
>
> 《模式识别》课程项目一第一小组 · 文献汇报
>
> THANK YOU FOR YOUR ATTENTION
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-Y364L7RZ - MultiLoReFT  Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning|MultiLoReFT: Decoupling Shared and Modality-Specific Subspaces in Multimodal Learning via Low-Rank Representation Fine-Tuning]] — 中关联；共同研究内容：低秩与参数高效微调。
- [[Zotero Knowledge/Papers/ZK-SE2PQKZ8 - LoRA  Low-Rank Adaptation of Large Language Models|LoRA: Low-Rank Adaptation of Large Language Models]] — 中关联；共同研究内容：低秩与参数高效微调。
- [[Zotero Knowledge/Papers/ZK-3D4I5WS2 - Understanding Geometric Representations in Self-Supervised Vision Transformers via Su|Understanding Geometric Representations in Self-Supervised Vision Transformers via Subspace Intervention]] — 中关联；共同研究内容：低秩与参数高效微调。
- [[Zotero Knowledge/Papers/ZK-WE2HF7Y8 - Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning|Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning]] — 中关联；共同研究内容：低秩与参数高效微调。

<!-- content-relations:end -->

<!-- research-integration:start -->
## 研究主题入口

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Adaptation & Generalization/索引|06 Alignment & Reliability/Adaptation & Generalization]]

## 概念比较入口

- [[Zotero Knowledge/Concepts/微调策略与泛化鲁棒性|微调策略与泛化鲁棒性]]
<!-- research-integration:end -->
