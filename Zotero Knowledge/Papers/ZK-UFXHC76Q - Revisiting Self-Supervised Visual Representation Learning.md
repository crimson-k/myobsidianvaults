---
type: "literature"
title: "Revisiting Self-Supervised Visual Representation Learning"
aliases: ["Revisiting SSL"]
zotero_keys: ["UFXHC76Q"]
year: 2019
authors: ["Kolesnikov, Alexander", "Zhai, Xiaohua", "Beyer, Lucas"]
venue: "CVPR 2019"
doi: ""
url: "https://arxiv.org/abs/1901.09005"
collections: ["02 Representation & Perception/Visual Representation Learning", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [42, 54]
imported_at: "2026-10-03"
---

# Revisiting Self-Supervised Visual Representation Learning

[在 Zotero 打开](zotero://select/library/items/UFXHC76Q) · [论文来源](https://arxiv.org/abs/1901.09005) · [论文 PDF](https://arxiv.org/pdf/1901.09005)

## 文献导读

统一控制前置任务、骨干架构与评估协议，检查方法排名是否受到混杂因素影响。阅读重点是架构与任务的交互，以及线性探针是否充分优化。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-MWND3NJ9 - Self-Supervised Visual Representation Learning  Pretrain-Finetuning or Joint Training|PFT vs JT]]
- [[Zotero Knowledge/Papers/ZK-3D4I5WS2 - Understanding Geometric Representations in Self-Supervised Vision Transformers via Su|Geometric Subspace Intervention]]

## 原始摘要

Unsupervised visual representation learning remains a largely unsolved problem in computer vision research. Among a big body of recently proposed approaches for unsupervised learning of visual representations, a class of self-supervised techniques achieves superior performance on many challenging benchmarks. A large number of the pretext tasks for self-supervised learning have been studied, but other important aspects, such as the choice of convolutional neural networks (CNN), has not received equal attention. Therefore, we revisit numerous previously proposed self-supervised models, conduct a thorough large scale study and, as a result, uncover multiple crucial insights. We challenge a number of common practices in selfsupervised visual representation learning and observe that standard recipes for CNN design do not always translate to self-supervised representation learning. As part of our study, we drastically boost the performance of previously proposed techniques and outperform previously published state-of-the-art results by a large margin.

来源：[论文官方页面](https://arxiv.org/abs/1901.09005)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 42–54 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 42 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-042.png]]

> [!quote]- 本页可搜索文字
> 课程论文汇报 · CVPR 2019
>
> Revisiting Self-Supervised Visual Representation Learning
>
> 重新审视自监督视觉表征学习
>
> Alexander Kolesnikov · Xiaohua Zhai · Lucas Beyer
>
> Google Brain · CVPR 2019
>
> 汇报人：万立志    学号：2612121
>
> 课程：模式识别    日期：2026年9月23日
>
> 核心问题
>
> 网络架构会不会改变我们对自监督方法优劣的判断？
>
> 中心结论
>
> 架构与前置任务强耦合
>

### 原 PPT 第 43 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-043.png]]

> [!quote]- 本页可搜索文字
> PRIOR KNOWLEDGE · SUPERVISION
>
> 先验知识：自监督学习用数据自身构造监督信号
>
> 02
>
> Kolesnikov et al. · CVPR 2019
>
> 无标签图像
>
> 自动构造监督信号
>
> 前置任务训练
>
> 骨干网络 Backbone
>
> 视觉表征 z
>
> 下游任务 Linear Probe
>
> 大量未标注的图像
>
> （自然图像）
>
> 标签来自数据变换
>
> ResNet、RevNet、VGG 等深度卷积网络
>
> 高维、语义丰富
>
> 的视觉表征
>
> 仅训练线性分类器
>
> 评估表征泛化能力
>

### 原 PPT 第 44 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-044.png]]

> [!quote]- 本页可搜索文字
> PRIOR KNOWLEDGE · LINEAR PROBE
>
> 先验知识：线性探针只衡量表征的线性可分性
>
> 03
>
> 输入图像
>
> →
>
> 冻结骨干 Backbone
>
> →
>
> 提取表征 z
>
> →
>
> 训练 Linear Probe
>
> →
>
> 下游准确率
>
> ImageNet / Places205
>
> ❄  参数 θ 固定
>
> 不更新骨干
>
> Pre-logits 高维向量
>
> 只更新 W 和 b
>
> 其他参数保持不变
>
> 猫
>
> 狗
>
> 汽车
>
> 鸟
>
> …
>
> Top-1 Accuracy
>
> Linear Probe 能回答
>
> 类别信息是否已经可以被线性读取
>
> Linear Probe 不能完整回答
>
> 检测、分割、鲁棒性和生成任务是否同样有效
>
> 公平比较需要固定骨干、特征读取位置、维度和探针训练协议
>

### 原 PPT 第 45 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-045.png]]

> [!quote]- 本页可搜索文字
> MOTIVATION · CONFOUNDING FACTORS
>
> 作者动机：既有研究忽略了网络架构带来的混杂
>
> 04
>
> 不同工作往往同时改变任务、骨干、特征位置和评估协议，最终准确率不能直接归因于某一个方法
>

### 原 PPT 第 46 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-046.png]]

> [!quote]- 本页可搜索文字
> PRETEXT TASKS
>
> 研究对象：四类前置任务提供不同的监督信号
>
> 05
>
> Rotation Prediction
>
> Exemplar
>
> Relative Patch Location
>
> Jigsaw Puzzle
>
> 预测旋转角度
>
> 同一实例增强保持接近
>
> 不同实例分开
>
> 预测 8 种相对位置
>
> 从候选排列中恢复拼图顺序
>
> 前置任务只是训练手段，真正目标是学习可迁移表征
>

### 原 PPT 第 47 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-047.png]]

> [!quote]- 本页可搜索文字
> CONTROLLED STUDY · LINEAR PROBE
>
> 实验设计：统一控制任务、架构和评估协议
>
> 06
>
> ImageNet
>
> 无标签图像
>
> →
>
> 4 种前置任务
>
> →
>
> 6 类 CNN 设置
>
> →
>
> 多种宽度
>
> →
>
> 冻结骨干网络
>
> →
>
> 提取 Pre-logits
>
> 表征 z
>
> →
>
> 训练
>
> Linear Probe
>
> →
>
> 下游任务评估
>
> 用于自监督预训练
>
> Rotation
>
> 0°/90°/180°/270°
>
> Exemplar
>
> 拉近 / 推远
>
> Jigsaw
>
> 恢复排列
>
> Rel. Patch
>
> 8 种位置
>
> RevNet50
>
> ResNet50 v1
>
> ResNet50 v2
>
> VGG19-BN
>
> …
>
> 4×
>
> 8×
>
> 12×
>
> 16×
>
> …
>
> ❄  θ 固定
>
> 不更新
>
> z
>
> 高维向量
>
> Linear
>
> Probe
>
> (W,b)
>
> 只更新 W,b
>
> ImageNet
>
> 物体分类
>
> Places205
>
> 场景分类
>
> Linear Probe 的具体说明
>
> 冻结的骨干网络
>
> θ 固定
>
> →
>
> 表征 z
>
> →
>
> 线性分类器
>
> 仅更新 W 和 b
>
> →
>
> 只测试语义信息是否已经可以被线性读取
>
> Backbone 参数固定，只在 Pre-logits 表征上训练一个线性分类器
>

### 原 PPT 第 48 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-048.png]]

> [!quote]- 本页可搜索文字
> MAIN RESULT · FIGURE 1 + TABLE 1
>
> 核心发现：更换骨干架构会改变前置任务的排名
>
> 07
>
> Figure 1：不同任务对应不同最优骨干
>
> Table 1：增宽通常有效，但不会消除交互
>
> Rotation：RevNet50 16× = 53.7%
>
> Relative Patch Location：ResNet50 v1 8× = 50.5%
>
> 任务与架构必须联合比较
>

### 原 PPT 第 49 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-049.png]]

> [!quote]- 本页可搜索文字
> ABLATIONS · FIGURES 4–6
>
> 消融结果：读取层、宽度与表征维度都会影响结论
>
> 08
>
> ① 深度与跳跃连接
>
> VGG 后层退化，ResNet 与 RevNet 通常持续提升。信息保留是解释性假设。
>
> ② 宽度与表征维度是两个变量
>
> 固定最窄 1× 网络，只把表征维度从 512 增至 8192，准确率约 31% 增至 43%。沿行和沿列都提升。
>
> ③ 前置任务准确率不能跨架构预测表征质量
>
> 同一架构内部可能正相关，跨架构比较时相关性失效。
>

### 原 PPT 第 50 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-050.png]]

> [!quote]- 本页可搜索文字
> EVALUATION PROTOCOL · FIGURE 8
>
> 评估问题：线性探针训练不足会低估表征质量
>
> 09
>
> Figure 8 · Linear classifier optimization
>
> 实验条件
>
> Batch size 2048
>
> 初始学习率 0.1
>
> 首次衰减 30 / 120 / 480 epoch
>
> 关键观察
>
> 约 500 epoch 后仍可能提升
>
> 学习率衰减越晚，最终准确率越高
>
> 公平比较需要公开优化器、学习率、
>
> 衰减节点和训练时长
>

### 原 PPT 第 51 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-051.png]]

> [!quote]- 本页可搜索文字
> RESULTS & CONTRIBUTIONS · TABLE 2
>
> 结果与贡献：旧方法通过合理选型即可大幅提升
>
> 10
>
> 此前最佳与本文统一重评结果（ImageNet Top-1，%）
>
> 前置任务
>
> 此前结果
>
> 本文结果
>
> 提升
>
> Rotation
>
> 38.7
>
> 55.4
>
> +16.7
>
> Exemplar
>
> 31.5
>
> 46.0
>
> +14.5
>
> Rel. Patch Loc.
>
> 36.2
>
> 51.4
>
> +15.2
>
> Jigsaw
>
> 34.7
>
> 44.6
>
> +9.9
>
> 55.4%
>
> Rotation 最佳结果
>
> +16.7 pt
>
> 最大绝对提升
>
> 论文的实际创新
>
> 01
>
> 把架构纳入自监督方法的核心评价
>
> 02
>
> 证明架构与前置任务存在强交互
>
> 03
>
> 拆开网络宽度与表征维度的贡献
>
> 04
>
> 揭示读取层和探针日程会改变结论
>
> 论文没有发明 Rotation、Jigsaw，也没有提出新的自监督损失
>

### 原 PPT 第 52 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-052.png]]

> [!quote]- 本页可搜索文字
> LIMITATIONS & COURSE PROJECT
>
> 局限与启示：论文方法论仍适用于当前课程项目
>
> 11
>
> 论文的适用边界
>
> 研究时代
>
> 集中在早期 pretext-task 方法
>
> 模型范围
>
> 以 CNN 为主，未覆盖 ViT
>
> 评价范围
>
> 主要观察分类线性可分性
>
> 因果边界
>
> 跳跃连接的信息保留仍是解释
>
> 效率成本
>
> 增宽会增加计算与显存开销
>
> 对项目一的具体启示
>
> 研究问题
>
> SimCLR 与 MAE 学到的表征有何差异
>
> 统一骨干
>
> ViT-B/16，固定 CLS token 768D
>
> 下游比较
>
> Linear Probe 与 LoRA r=8/16
>
> 分析视角
>
> SVD、alignment/uniformity、t-SNE/UMAP
>
> 控制变量
>
> 相同数据划分、训练预算和特征口径
>
> 共同方法论：先固定混杂因素，再比较方法，并从表征本身解释差异
>

### 原 PPT 第 53 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-053.png]]

> [!quote]- 本页可搜索文字
> CONCLUSION
>
> 结论：自监督方法必须与骨干和评估协议共同评价
>
> 12
>
> 01
>
> 架构与前置任务存在交互
>
> 同一任务换骨干后，方法排名可能反转
>
> 02
>
> 容量与表示方式会改变分数
>
> 宽度、表征维度和读取层都需要单独控制
>
> 03
>
> 评估器本身也是实验变量
>
> 线性探针训练不足会低估已经学到的表征
>
> Representation Quality ≠ f(Pretext Task only)
>

### 原 PPT 第 54 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-054.png]]

> [!quote]- 本页可搜索文字
> 谢谢聆听
>
> 核心结论
>
> 评价自监督方法时，前置任务、骨干架构和评估协议必须同时报告
>
> Revisiting Self-Supervised Visual Representation Learning
>
> CVPR 2019
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-MWND3NJ9 - Self-Supervised Visual Representation Learning  Pretrain-Finetuning or Joint Training|Self-Supervised Visual Representation Learning: Pretrain-Finetuning or Joint Training?]] — 中关联；共同研究内容：基准与数据合成、视觉自监督。

<!-- content-relations:end -->
