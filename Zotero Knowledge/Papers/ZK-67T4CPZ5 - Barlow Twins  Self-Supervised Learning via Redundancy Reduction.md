---
type: "literature"
title: "Barlow Twins: Self-Supervised Learning via Redundancy Reduction"
aliases: ["Barlow Twins"]
zotero_keys: ["67T4CPZ5"]
year: 2021
authors: ["Zbontar, Jure", "Jing, Li", "Misra, Ishan", "LeCun, Yann", "Deny, Stéphane"]
venue: "ICML 2021"
doi: ""
url: "https://arxiv.org/abs/2103.03230"
collections: ["02 Representation & Perception/Visual Representation Learning", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1", "concept/视觉自监督的目标与表征结构", "concept-primary/视觉自监督的目标与表征结构"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [113, 123]
imported_at: "2026-10-03"
---

# Barlow Twins: Self-Supervised Learning via Redundancy Reduction

[在 Zotero 打开](zotero://select/library/items/67T4CPZ5) · [论文来源](https://arxiv.org/abs/2103.03230) · [论文 PDF](https://arxiv.org/pdf/2103.03230)

## 文献导读

让双视图特征的交叉相关矩阵接近单位阵，以同维一致性和异维去冗余构建自监督目标。适合比较负样本机制与特征统计约束。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-YMBWZADV - A Simple Framework for Contrastive Learning of Visual Representations|SimCLR]]
- [[Zotero Knowledge/Papers/ZK-QQB2NRRQ - Masked Autoencoders Are Scalable Vision Learners|MAE]]

## 原始摘要

Self-supervised learning (SSL) is rapidly closing the gap with supervised methods on large computer vision benchmarks. A successful approach to SSL is to learn embeddings which are invariant to distortions of the input sample. However, a recurring issue with this approach is the existence of trivial constant solutions. Most current methods avoid such solutions by careful implementation details. We propose an objective function that naturally avoids collapse by measuring the cross-correlation matrix between the outputs of two identical networks fed with distorted versions of a sample, and making it as close to the identity matrix as possible. This causes the embedding vectors of distorted versions of a sample to be similar, while minimizing the redundancy between the components of these vectors. The method is called Barlow Twins, owing to neuroscientist H. Barlow's redundancy-reduction principle applied to a pair of identical networks. Barlow Twins does not require large batches nor asymmetry between the network twins such as a predictor network, gradient stopping, or a moving average on the weight updates. Intriguingly it benefits from very high-dimensional output vectors. Barlow Twins outperforms previous methods on ImageNet for semi-supervised classification in the low-data regime, and is on par with current state of the art for ImageNet classification with a linear classifier head, and for transfer tasks of classification and object detection.

来源：[论文官方页面](https://arxiv.org/abs/2103.03230)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 113–123 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 113 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-113.png]]

> [!quote]- 本页可搜索文字
> Barlow Twins
>
> Self-Supervised Learning via Redundancy Reduction
>
> 基于“去冗余”的自监督视觉表征学习
> 
>
> Jure Zbontar · Li Jing · Ishan Misra · Yann LeCun · Stéphane Deny
> ICML 2021 · 课堂文献汇报
>
> 汇报人：刘恺诚
>

### 原 PPT 第 114 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-114.png]]

> [!quote]- 本页可搜索文字
> 一、研究动机：没有标签，如何学到“有用的视觉表示”？
>
> 2
>
> 监督学习的限制
>
>        大规模视觉任务依赖人工标签；自监督学习希望直接利用未标注图像，先学到可迁移的representation。
>
> SSL的主流思路
>
>        对同一图像构造不同增强视图，并约束其表示保持一致，从而学习对数据增强具有不变性的视觉表征。
>
> 真正的难点
>
>        如何在保证同一图像不同增强视图表示一致的同时，避免表示坍塌，并使模型学到信息丰富、非冗余的特征。
>
> 同一图像经过不同的augmentation：  x → yᴬ , yᴮ
>
> 训练目标：  f(yᴬ) ≈ f(yᴮ)    但不能让所有 x 都得到同一个表示
>

### 原 PPT 第 115 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-115.png]]

> [!quote]- 本页可搜索文字
> 二、现有痛点：避免 collapse 往往需要额外机制
>
> 3
>
> InfoNCE/SimCLR等
>
>        通过正样本拉近、负样本推远避免 collapse。
> 
>       问题：需要大量 negative samples；通常依赖较大的 batch；输出维度增大后收益容易饱和。
>
> BYOL/SimSiam等
>
>        虽不使用负样本，但为了避免所有图像得到相同表示，需要引入额外的训练设计，如预测器、停止梯度、目标网络的指数移动平均等。
>
> Barlow Twins的问题意识
>
>        能否设计一个目标函数，使“避免 collapse”直接写进其内部，而不是依赖大量负样本或特殊非对称结构？
>

### 原 PPT 第 116 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-116.png]]

> [!quote]- 本页可搜索文字
> 三、本文模型设计方案：Twin Network + Cross-Correlation
>
> 4
>
>       一个中有张图像，每张图像随机增强两次得到。
>
>       两个分支使用完全相同、参数共享的。
>
> 输出输出 。
>
>       将两个分支的组成 ，并在维度标准化。
>
>       最后计算这两个矩阵之间的。
>

### 原 PPT 第 117 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-117.png]]

> [!quote]- 本页可搜索文字
> 三、核心方法：交叉相关矩阵 
>
> 5
>
> 1  沿对每个特征列标准化
>
> 由该列的个样本计算均值和标准差。非恒定列减均值、除标准差，消除偏移与尺度。
>
> 2  取两列，逐样本相乘后求平均
>
> 固定 ：取的第列、的第列。
>
> 同一张图像对应的两项相乘，再对张取平均。
>
>  到底表示什么？
>
> 固定后：
>
> 取的第个特征列与的第j个特征列
>
> 两列都包含同一 中个样本的取值，因此是两个特征列之间的一个相关性标量。
>

### 原 PPT 第 118 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-118.png]]

> [!quote]- 本页可搜索文字
> 三、核心目标：同维一致，异维去相关
>
> 6
>
> 对角项：不变性
>
> 接近
>
> 同一维特征在两个增强视图下
>
> 保持一致的响应。
>
> 非对角项：冗余抑制
>
>  接近
>
> 不同维度减少重复的线性信息。
>
> 控制两项的相对权重。
>
> 整体目标：让尽量接近单位矩阵
>

### 原 PPT 第 119 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-119.png]]

> [!quote]- 本页可搜索文字
> 四、核心创新：用特征统计构造学习目标
>
> 7
>
> 方法创新
>
> 把跨视图不变性与特征去冗余写入同一个损失。
>
> 直接约束的特征交叉相关矩阵。
>
> 训练机制
>
> 共享参数的对称双分支，两个分支都反向传播。
>
> 无需负样本、预测器、停止梯度或目标网络。
>
> 理论联系
>
> 的核心思想来源于提出的“冗余降低原则”：有效的表征应尽量减少不同特征之间的冗余信息。论文通过约束不同特征维度之间的相关性接近，将这一思想用于自监督学习
>

### 原 PPT 第 120 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-120.png]]

> [!quote]- 本页可搜索文字
> 五、表征质量：线性评估与少标签微调
>
> 8
>
> 先在无标签预训练，再用标签检验学到的表征。
>
> 结果分析：
>
> • 仅使用标签微调时，的，在表中最高，说明其预训练表征在极少标签条件下仍具有较好的可利用性。
>
> • 使用标签时，的为 ，虽并非所有指标最优，但与处于相近水平。
>
> • 相比直接使用少量标签进行监督训练，自监督预训练后再微调取得了比较高的准确率，体现了无标签预训练对少标签学习的价值。
>

### 原 PPT 第 121 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-121.png]]

> [!quote]- 本页可搜索文字
> 五、迁移验证：分类之外也有用
>
> 9
>
> 相同预训练编码器，在不同数据集和任务上评估。
>
> 结果分析：
>
> • 在目标检测中，的，与 处于相近水平。
>
> • 在目标检测中， 的，高于监督预训练的，并与其他主流自监督方法相当。
>
> • 在实例分割中， 的，高于监督预训练的，说明学到的表征不仅适用于分类，也能迁移到目标定位和实例分割任务
>

### 原 PPT 第 122 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-122.png]]

> [!quote]- 本页可搜索文字
> 五、消融实验/超参数分析
>
> 10
>
> 损失消融：在上实验，只改变目标函数
>
> 去掉冗余项：表征质量出现了明显下降
>
> 去掉不变性项：结果接近随机猜测
>
> 输出维度：测试范围内持续受益
>
> 随输出维度增大持续提升，在 维时仍未明显饱和；
>
> 而较早趋于稳定，说明对高维的利用更充分
>

### 原 PPT 第 123 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-123.png]]

> [!quote]- 本页可搜索文字
> 六、结论与启发
>
> 核心结论
>
> 通过，同时实现“跨视图一致”与“特征去冗余”，在对称双分支中学习具有竞争力且可迁移的表征。
>
> 方法上的启发
>
> • 防止不一定依赖负样本或非对称训练机制。
>
> • 可以直接简单的从特征的统计结构出发设计自监督目标。
>
> 实验上的发现
>
> • 在少标签学习和下游迁移任务上具有竞争力。
>
> • 高维对尤其有效，增大维度时性能仍持续提升。
>
> 边界与局限
>
> • 约束的是二阶相关性，去相关并不等于统计独立。
>
> • 高维交叉相关矩阵带来级计算/存储开销，并仍依赖合适的数据增强。
>
> 11
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-9YHA2VQZ - R2-DREAMER  REDUNDANCY-REDUCED WORLD MODELS WITHOUT DECODERS OR AUGMENTATION|R2-DREAMER: REDUNDANCY-REDUCED WORLD MODELS WITHOUT DECODERS OR AUGMENTATION]] — 强关联；对方摘要提到模型 Barlow Twins（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-MWND3NJ9 - Self-Supervised Visual Representation Learning  Pretrain-Finetuning or Joint Training|Self-Supervised Visual Representation Learning: Pretrain-Finetuning or Joint Training?]] — 中关联；共同研究内容：基准与数据合成、视觉自监督。

<!-- content-relations:end -->

<!-- research-integration:start -->
## 研究主题入口

- [[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]]

## 概念比较入口

- [[Zotero Knowledge/Concepts/视觉自监督的目标与表征结构|视觉自监督的目标与表征结构]]
<!-- research-integration:end -->
