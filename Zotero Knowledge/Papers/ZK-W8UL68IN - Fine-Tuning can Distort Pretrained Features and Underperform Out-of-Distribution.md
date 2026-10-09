---
type: "literature"
title: "Fine-Tuning can Distort Pretrained Features and Underperform Out-of-Distribution"
aliases: ["LP-FT"]
zotero_keys: ["W8UL68IN"]
year: 2022
authors: ["Kumar, Ananya", "Raghunathan, Aditi", "Jones, Robbie", "Ma, Tengyu", "Liang, Percy"]
venue: "ICLR 2022"
doi: ""
url: "https://arxiv.org/abs/2202.10054"
collections: ["06 Alignment & Reliability/Adaptation & Generalization", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [69, 78]
imported_at: "2026-10-03"
---

# Fine-Tuning can Distort Pretrained Features and Underperform Out-of-Distribution

[在 Zotero 打开](zotero://select/library/items/W8UL68IN) · [论文来源](https://arxiv.org/abs/2202.10054) · [论文 PDF](https://arxiv.org/pdf/2202.10054)

## 文献导读

研究全量微调为何可能扭曲预训练特征并降低分布外表现，提出先线性探测、再全量微调的 LP-FT。应分别比较 ID 与 OOD 指标，并保留理论的模型假设。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Adaptation & Generalization/索引|06 Alignment & Reliability/Adaptation & Generalization]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-SE2PQKZ8 - LoRA  Low-Rank Adaptation of Large Language Models|LoRA]]
- [[Zotero Knowledge/Papers/ZK-RAH7V3N7 - Low-Rank Rescaled Vision Transformer Fine-Tuning  A Residual Design Approach|RLRR]]
- [[Zotero Knowledge/Papers/ZK-BV7746FU - Mahalanobis++  Improving OOD Detection via Feature Normalization|Mahalanobis++]]

## 原始摘要

When transferring a pretrained model to a downstream task, two popular methods are full fine-tuning (updating all the model parameters) and linear probing (updating only the last linear layer -- the "head"). It is well known that fine-tuning leads to better accuracy in-distribution (ID). However, in this paper, we find that fine-tuning can achieve worse accuracy than linear probing out-of-distribution (OOD) when the pretrained features are good and the distribution shift is large. On 10 distribution shift datasets (Breeds-Living17, Breeds-Entity30, DomainNet, CIFAR $\to$ STL, CIFAR10.1, FMoW, ImageNetV2, ImageNet-R, ImageNet-A, ImageNet-Sketch), fine-tuning obtains on average 2% higher accuracy ID but 7% lower accuracy OOD than linear probing. We show theoretically that this tradeoff between ID and OOD accuracy arises even in a simple setting: fine-tuning overparameterized two-layer linear networks. We prove that the OOD error of fine-tuning is high when we initialize with a fixed or random head -- this is because while fine-tuning learns the head, the lower layers of the neural network change simultaneously and distort the pretrained features. Our analysis suggests that the easy two-step strategy of linear probing then full fine-tuning (LP-FT), sometimes used as a fine-tuning heuristic, combines the benefits of both fine-tuning and linear probing. Empirically, LP-FT outperforms both fine-tuning and linear probing on the above datasets (1% better ID, 10% better OOD than full fine-tuning).

来源：[论文官方页面](https://arxiv.org/abs/2202.10054)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 69–78 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 69 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-069.png]]

> [!quote]- 本页可搜索文字
> Fine-Tuning can Distort Pretrained Features and Underperform Out- of- Distribution
>
> 论文汇报
>
> 同济大学计算机科学与技术学院
>
> 程喆豪
>
> 2612133@tongji.edu.cn
>

### 原 PPT 第 70 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-070.png]]

> [!quote]- 本页可搜索文字
> 目录CONTENT
>
> 01
>
> 研究动机
>
> 02
>
> 现存痛点
>
> 03
>
> 核心创新点
>
> 04
>
> 解决方案
>
> 05
>
> 实验逻辑
>
> 06
>
> 结论与启发
>

### 原 PPT 第 71 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-071.png]]

> [!quote]- 本页可搜索文字
> 71
>
> 研究动机
>
> 全量微调一定更鲁棒吗？
>
> 预训练迁移两大主流：
>
>       全量微调 FT：更新所有参数，包括特征提取器和分类头。
>
>       线性探测 LP：冻结预训练特征提取器，只训练最后的线性分类头。
>
>       ID 精度高是否意味着 OOD 精度也高？FT 是否一定比 LP 更鲁棒？
>
> ：参数为  的特征提取器；：线性头。
>
> 常识：FT 的 ID 精度更高，因此常被默认用于 OOD。
>
> 反直觉：当预训练特征好 + 分布偏移大时，FT 的 OOD 反而低于 LP。
>
> 核心问题：FT 为什么会在 OOD 上失败？如何缓解？
>

### 原 PPT 第 72 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-072.png]]

> [!quote]- 本页可搜索文字
> 72
>
> 现存痛点
>
> 现有方法缺陷
>
> FT常被默认用于 OOD ，但 ID 高 ≠ OOD 高。
>
> LP 保留预训练特征，OOD 较稳，但不能适配下游任务，ID 偏弱。
>
> FT 理论分析困难：非凸、过参数化、依赖初始化轨迹。
>
> 早停无效：整条 FT 轨迹都难以超过 LP 的 OOD。
>
> 常见微调启发式未专门针对 OOD 鲁棒性设计。
>
>         训练损失， 训练输入， 标签， 特征提取器， 线性头。该梯度说明对  的更新与  的 rowspace 有关。
>
>       若 ，则 ，于是：
>
>         训练数据子空间， 其正交补。FT 不改变 OOD 正交方向特征，只改变 ID 方向特征，造成“特征扭曲”。
>

### 原 PPT 第 73 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-073.png]]

> [!quote]- 本页可搜索文字
> 73
>
> 核心创新点
>
> 创新
>
> 理论创新：首次用两层线性网络 + 梯度流分析 FT，证明 FT 会扭曲预训练特征，并通过计算给出 OOD 误差下界。
>
> 方法创新：提出 LP-FT，先线性探测得到好头，再全量微调，缓解 ID-OOD 的tradeoff。
>
> 核心结论：预训练特征越好、分布偏移越大，FT 的 OOD 劣势越明显。
>
> 场景选择：在 10 个分布偏移数据集上系统比较 FT、LP、LP-FT。
>
> 性能提升：LP-FT 平均 ID 85.7%，OOD 68.9%；比 FT 的 OOD 高约 10%。
>

### 原 PPT 第 74 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-074.png]]

> [!quote]- 本页可搜索文字
> 74
>
> 解决方案
>
> 首先设定一个可分析的简化模型
>
> 作者考虑两层线性网络：
>
> ：特征提取器；
>
> ：线性头；
>
> 预训练得到 ，接近最优 ；
>
> 训练数据  位于低维子空间 ；
>
> OOD 数据包含  方向，即训练数据未覆盖的方向。
>
> 损失为平方损失：
>
>       FT 同时更新 ；LP 冻结 ，只更新 。作者用梯度流（学习率趋于0的连续时间极限）来分析训练动态。
>
> 若 ，则 ，于是：
>
>        在 OOD 正交方向  上， 在 FT 过程中完全不变；但在 ID 方向  上， 会被更新
>
> 在两层线性网络的梯度流中，下面这个量保持不变：
>
> 因此，头  和特征  的更新是耦合的：
>
> 如果头  变化很大，特征  也会变化很大；
>
> 如果头  几乎不变，特征  也几乎不变。
>

### 原 PPT 第 75 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-075.png]]

> [!quote]- 本页可搜索文字
> 75
>
> 解决方案
>
> 特征扭曲 → LP-FT结合
>
> FT的问题：
>
>  随机初始化线性头𝑣
>
>  训练误差大，头𝑣必须大幅更新
>
>  头𝑣 与特征提取器耦合更新
>
>  特征被扭曲，头适配扭曲后 的 ID 特征导致 OOD 变差
>
> LP的特点
>
>  冻结特征提取器 𝐵
>
>  只训练线性头 𝑣
>
>  保留预训练特征，OOD 较稳
>
>  不能适配下游任务，ID 偏弱
>
> 优势结合：LP-FT 的方案
>
>  第一步：LP，得到好的分类头 
>
> 第二步：用  初始化头再全量微调 𝑣,𝐵
>
>  好头不必大改 → 特征扭曲小，最终 ID 和 OOD 都更好
>
>          是线性探测得到的头。用它初始化，可以让 FT 阶段头不需要大幅更新，从而减少特征扭曲。
>
>        即：先线性探测得到好的分类头，再全量微调，兼顾 ID 与 OOD。
>

### 原 PPT 第 76 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-076.png]]

> [!quote]- 本页可搜索文字
> 76
>
> 实验逻辑
>
> 论文如何论证有效性
>
> 实验设置
>
> 主结果
>
> 机制验证与消融
>
> 10 个分布偏移数据集
>
> 预训练：MoCo-v2、CLIP、MoCo-TP
>
> 架构：ResNet-50、ViT-B/16
>
> 对比：FT vs LP vs LP-FT
>
> FT 的 ID 更高，LP 的 OOD 更好，LP-FT 两者最佳
>
> 结论：预训练好 + 偏移大时，保留特征更鲁棒
>
> 特征距离：ID 变化 > OOD 变化
>
> LP-FT 特征变化小 10–100 倍
>
> 早停：LP OOD 67.1% > FT 61.3%
>
> 在数据集 ID≈OOD 时，FT 可的泛化性可能反超LP
>
> CLIP ResNet/ViT 结果一致；LP-FT 优于其他启发式
>
> 微调前后特征距离
>

### 原 PPT 第 77 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-077.png]]

> [!quote]- 本页可搜索文字
> 77
>
> 结论
>
> 论文结论与启发
>
> 本文结论
>
> 启发
>
> FT 会扭曲预训练特征，导致其OOD表现可能差于 LP
>
> LP 相对 FT 更鲁棒，但 ID 偏弱
>
> LP-FT 兼顾 ID 与 OOD，结果更好
>
> 早停不能解决特征扭曲
>
> 预训练越好，越要重视OOD数据的表现
>
> 微调不只优化损失，还改变特征几何；初始化决定隐式正则，进而决定 OOD 表现。
>
> LP-FT 本质是“先对齐头，再解冻特征”；可推广为零样本初始化、逐层解冻、参数高效微调。
>
> 简单两阶段即可同时提升ID与OOD，说明鲁棒性与精度并非必然权衡，关键是控制特征扭曲。
>
>        FT 的 OOD 误差有正下界；随机头  越大、预训练特征与 OOD 方向夹角越大，下界越高。早停无法消除。
>

### 原 PPT 第 78 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-078.png]]

> [!quote]- 本页可搜索文字
> 谢谢，请您批评指正!
>
> 同济大学计算机科学与技术学院
>
> 程喆豪 | 2612133@tongji.edu.cn
>
> 计算机科学与技术学院
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-BV7746FU - Mahalanobis++  Improving OOD Detection via Feature Normalization|Mahalanobis++: Improving OOD Detection via Feature Normalization]] — 中关联；共同研究内容：鲁棒性与域外泛化。
- [[Zotero Knowledge/Papers/ZK-W84DWQI5 - LiT  Zero-Shot Transfer with Locked-image text Tuning|LiT: Zero-Shot Transfer with Locked-image text Tuning]] — 中关联；共同研究内容：鲁棒性与域外泛化。

<!-- content-relations:end -->
