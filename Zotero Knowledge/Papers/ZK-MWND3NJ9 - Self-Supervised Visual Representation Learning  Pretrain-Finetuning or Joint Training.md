---
type: "literature"
title: "Self-Supervised Visual Representation Learning: Pretrain-Finetuning or Joint Training?"
aliases: ["PFT vs JT"]
zotero_keys: ["MWND3NJ9"]
year: 2026
authors: ["Munia, Nusrat", "Ward, Tyler", "Nayla, Nishat", "Massey, Matthew A.", "Imran, Abdullah-Al-Zubaer"]
venue: "arXiv 2026"
doi: ""
url: "https://arxiv.org/abs/2607.13192"
collections: ["02 Representation & Perception/Visual Representation Learning", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [155, 178]
imported_at: "2026-10-03"
---

# Self-Supervised Visual Representation Learning: Pretrain-Finetuning or Joint Training?

[在 Zotero 打开](zotero://select/library/items/MWND3NJ9) · [论文来源](https://arxiv.org/abs/2607.13192) · [论文 PDF](https://arxiv.org/pdf/2607.13192)

## 文献导读

比较先自监督预训练再有监督微调与联合优化两种训练范式。方法选择依赖任务、标签量与领域复杂度，应结合数据效率、鲁棒性和跨域泛化判断。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-UFXHC76Q - Revisiting Self-Supervised Visual Representation Learning|Revisiting SSL]]
- [[Zotero Knowledge/Papers/ZK-QQB2NRRQ - Masked Autoencoders Are Scalable Vision Learners|MAE]]
- [[Zotero Knowledge/Papers/ZK-YMBWZADV - A Simple Framework for Contrastive Learning of Visual Representations|SimCLR]]

## 原始摘要

Self-supervision is a powerful technique for learning visual representations from unlabeled data. Existing techniques primarily adopt a two-stage approach for self-supervised learning (SSL): a pretraining stage on unlabeled data followed by a finetuning stage on labeled data. While this pipeline has demonstrated extreme effectiveness, the interaction between self-supervised and supervised learning objectives remains insufficiently understood. In this work, we systematically investigate whether jointly optimizing the self-supervised and supervised objectives during training provides a better alternative. We compare two training paradigms: (1) the aforementioned pretraining followed by finetuning (PFT) and (2) joint training (JT), where self-supervised and supervised losses are optimized simultaneously in the same network. Across eight representative SSL methods and diverse computer vision tasks on natural, medical, crisis response, and remote sensing data, we evaluate performance under varying percentages of labeled data. Our results reveal that the relative effectiveness of PFT and JT depends strongly on the task at hand, the availability of labeled data, and the complexity of the domain. We find that JT consistently improves data and training efficiency while being robust in low-label settings, while PFT is more reliable in more specialized domains. We further analyze representation quality, robustness, and cross-domain generalization, providing new insights into how self-supervised and supervised objectives interact during optimization. We establish a comprehensive empirical benchmark for hybrid SSL-based semi-supervised learning and offer practical guidance for selecting appropriate training strategies across diverse vision applications.

来源：[论文官方页面](https://arxiv.org/abs/2607.13192)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 155–178 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 155 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-155.png]]

> [!quote]- 本页可搜索文字
> Self-Supervised Visual Representation Learning:
>
> Pretrain–Finetuning or Joint Training?
>
> 模式识别-文献汇报
>
> 汇报人：沈徐敏
>
> 第一组序号11
>

### 原 PPT 第 156 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-156.png]]

> [!quote]- 本页可搜索文字
> CONTENTS
>
> 研究动机
>
> 01
>
> 现存痛点
>
> 02
>
> 本文解决方案
>
> 03
>
> 主要贡献
>
> 04
>
> 实验逻辑
>
> 论文结论与启发
>
> 05
>
> 06
>

### 原 PPT 第 157 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-157.png]]

> [!quote]- 本页可搜索文字
> 01
>
> 研究动机
>

### 原 PPT 第 158 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-158.png]]

> [!quote]- 本页可搜索文字
> 研究动机——背景
>
> “
>
> “
>
> SSL
>
> Self-Supervised Learning（SSL）利用无标签数据构造监督信号，学习可迁移的视觉表征。
>
> 数据增强 / 视图
>
> 无标注图像 X
>
> 编码器
>
> fθ
>
> 投影头
>
> gφ
>
> 表示向量
>
> z = gφ(h)
>
> 01
>
> 02
>
> 03
>
> 04
>
> 问题形式化
>
> 令 Dₗ = {(xᵢ, yᵢ)}ᵢ₌₁ᴺˡ 表示一个包含 Nₗ 个样本的标注数据集，其中 xᵢ ∈ X 代表输入图像，yᵢ ∈ Y 是其对应的真实值标签。令 Dᵤ = {xⱼ}ⱼ₌₁ᴺᵘ 表示一个未标注数据集，可能属于相同或不同的领域。
>
> 编码表示
>
> 模型 fθ，由参数 θ 参数化，将输入 x 编码为潜在表示h = fθ(x)，其中 h 可选。
>
> 投影头
>
> 投影头 gφ 生成用于自监督目标的嵌入 z = gφ(h)。
>
> 优化目标
>
> 自监督损失 LSSL 促使同一图像在不同变换下的表示保持一致，
>
> 具体形式取决于自监督学习框架。对于标注样本 (xᵢ, yᵢ) ∈ Dₗ，
>
> 模型通过最小化面向下游任务的监督损失 Lsup 进行优化，
>
> 如 Lsup = (1/Nₗ)Σᵢ₌₁ᴺˡ ℓtask(fθ(xᵢ), yᵢ)。
>
> 1
>
> 2
>
> 3
>
> 4
>

### 原 PPT 第 159 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-159.png]]

> [!quote]- 本页可搜索文字
> 研究动机——SSL的主要方法
>
> 通过对比正负样本，学习使同一图像的不同视图在特征空间中更接近。
>
> 通过重建被遮挡的图像内容，学习图像的上下文信息和语义结构。
>
> 通过减少不同视图之间的冗余信息，学习更紧凑、更有区分性的表征。
>

### 原 PPT 第 160 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-160.png]]

> [!quote]- 本页可搜索文字
> 研究动机——两大训练范式
>
> “
>
> “
>
> 在顺序情景下
>
> 模型首先在未标记数据上使用自监督目标进行预训练。
>
> 随后在标注子集上进行微调以用于下游评
>
> 该方法遵循传统 SSL 中常用的迁移学习范式，即把自监督表示重新用于特定任务的最优化。 
>
> Pretrain-Finetuning
>
> Pretrain-Finetuning (PFT)先进行自监督预训练，再将得到的骨干网络迁移到具体下游任务，通过有标签数据进行微调。
>

### 原 PPT 第 161 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-161.png]]

> [!quote]- 本页可搜索文字
> 研究动机—— 
>
> 两大训练范式
>
> Joint Training
>
> “
>
> “
>
> 在联合训练情景下，自监督目标与监督目标被纳入统一框架中进行协同优化。模型在单一训练阶段同时利用标注数据与未标记数据进行学习，其中，自监督损失 定义于未标记样本，监督损失 定义于标注样本。整体训练目标可表示为
>
> 该目标函数使模型能够在学习未标记样本不变性表征的同时，充分利用标注数据所提供的判别性信息。联合优化过程中，两类损失共享同一编码器 ，因此参数更新同时受到自监督目标和监督目标的影响。在第 个优化步骤中，编码器参数的更新可表示为
>
> 其中， 表示学习率。当 与 的方向一致或具有较高相似性时，两类学习目标会产生协同作用，从而形成建设性的梯度更新，并促进共享表征的优化。
>
> Joint Training (JT)
>
> 在训练过程中同时利用无标签数据产生的自监督信号，以及有标签数据产生的下游监督信号。
>

### 原 PPT 第 162 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-162.png]]

> [!quote]- 本页可搜索文字
> 02
>
> 现存痛点
>

### 原 PPT 第 163 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-163.png]]

> [!quote]- 本页可搜索文字
> 现存痛点：在模型训练过程中，自监督与监督目标应该如何相互作用？ 
>
> 01
>
> 02
>
> 03
>
> 04
>
> 计算与迭代成本高
>
> 现有联合学习研究覆盖不足
>
> SSL与监督任务的梯度可能冲突
>
> PFT：训练信号在时间上被割裂
>
> PFT 的预训练阶段只关心代理任务，例如让
>
> 同一图像的两个增强视图相近；真正的类别
>
> 标签在这一阶段完全缺席。到了下游阶段，
>
> 本文又冻结预训练编码器，只训练下游头。
>
> PFT 需要先完成一段完整的自监督训练，
>
> 再做下游训练。若每次改变数据比例、
>
> 下游任务或数据集，都要重复这一流程，
>
> 成本很高。JT 只需一个训练阶段，理论上
>
> 可以避免重复的顺序训练。
>
> 已有工作多集中在旋转预测、对比学习等
>
> 少数 SSL 信号作为下游任务的辅助目标；
>
> 但这些工作通常只考虑一类 SSL 方法或
>
> 一个任务。目前仍不知道联合训练的收益是普遍规律，还是个别任务的偶然现象？
>
> SSL 与监督任务的梯度可能一致，也可能
>
> 冲突。例如，对比学习希望对数据增强保
>
> 持不变，而密集分割可能需要保留精细空
>
> 间位置；旋转预测在自然图像中可能有帮
>
> 助，但在需要保持辨识细节方向的医学任
>
> 务中则可能造成干扰。
>
> → 导致自监督与监督信号缺乏有效交互。
>
> → 顺序式训练带来显著的计算与时间开销。
>
> → 缺乏系统、全面的比较与结论。
>
> → 不同任务间存在目标不一致的风险。
>

### 原 PPT 第 164 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-164.png]]

> [!quote]- 本页可搜索文字
> 03
>
> 本文解决方案
>
> 在十一个数据集和八个代表性自监督学习框架上 严格评估两种训练方案。 
>

### 原 PPT 第 165 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-165.png]]

> [!quote]- 本页可搜索文字
> 本文解决方案：构建 PFT 与 JT 的统一比较框架
>
> 在 11 个数据集和 8 个代表性自监督学习框架上进行了大量实验。覆盖颜色化、旋转、SimCLR、BYOL、MoCo、DINO、MAE、Barlow Twins 等方法。
>
> 从数据规模、领域和任务三个维度严格评估两种训练方案。
>
> 评估任务覆盖图像分类、检测、语义分割和图像质量评估（IQA），全面分析学成表示的迁移能力与鲁棒性。
>
> 代表性自监督方法
>
> 颜色化        旋转        SimCLR     BYOL 
>
>      MoCo          DINO        MAE     Barlow Twins
>
> 跨领域评测场景
>
> 通用视觉
>
> CIFAR-10、COCO、PASCAL VOC2012、KADID-10k、KonIQ-10k
>
> 灾害情境        CrisisMMD、DMD
>
> 遥感领域        Earth-Scape
>
> 医疗领域        ISIC、JSRT、LDCTIQA
>
> 任务类型        图像分类、检测、语义分割、图像质量评估（IQA）
>

### 原 PPT 第 166 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-166.png]]

> [!quote]- 本页可搜索文字
> 本文解决方案：从单一性能评估到多维度评价
>
> 评价思路
>
> 使用标准指标来评估模型性能，既关注整体
>
> 准确率，也强调类别层面的平衡性。
>
> 对于通用领域数据集（如 CIFAR-10），报告
>
> Top-1 与 Top-5 准确率；对于特定领域数据集
>
> （如 CrisisMMD、Earth-Scape），补充使用 F1 得分，以实现更公平的类别比较。
>
> 针对目标检测、语义分割与图像质量评估（IQA）
>
> 任务，进一步引入与任务特性相匹配的多指标体系，从而实现从单一性能评估到多维度评价的转变。
>
> 由单一准确率 → 多维指标矩阵
>
> 图像分类与识别
>
> • 通用领域：Top-1、Top-5
>
> • 特定领域：F1 Score
>
> • 衡量整体识别能力与类别平衡
>
> 目标检测与语义分割
>
> • 检测指标：Precision（P）、Recall（R）
>
> • mAP@0.5
>
> • mAP@[0.5:0.95]
>
> • 分割指标：Dice、mIoU
>
> 图像质量评估（IQA）
>
> • 目标：预测 1–5 质量尺度上的 DMOS
>
> • 相关系数：SROCC
>
> • 相关系数：PLCC
>
> • 衡量预测结果与主观感知的一致性
>
> 01
>
> 02
>
> 03
>

### 原 PPT 第 167 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-167.png]]

> [!quote]- 本页可搜索文字
> 04
>
> 主要贡献
>

### 原 PPT 第 168 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-168.png]]

> [!quote]- 本页可搜索文字
> 创新点 1：构建跨方法、跨任务的统一评测
>

### 原 PPT 第 169 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-169.png]]

> [!quote]- 本页可搜索文字
> 创新点 2：分析不同数据规模和数据分布下的适用性
>
> “
>

### 原 PPT 第 170 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-170.png]]

> [!quote]- 本页可搜索文字
> 创新点 3：计算成本与训练效率分析
>

### 原 PPT 第 171 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-171.png]]

> [!quote]- 本页可搜索文字
> 05
>
> 实验逻辑
>

### 原 PPT 第 172 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-172.png]]

> [!quote]- 本页可搜索文字
> 实验配置
>
> 任务
>
> 数据集示例
>
> 模型/指标
>
> 分类
>
> CIFAR-10、CrisisMMD、DMD
>
> ResNet-18；Accuracy、F1
>
> 检测
>
> COCO、PASCAL VOC2012
>
> YOLOv12；P、R、mAP@50、mAP@50-95
>
> 分割
>
> ISIC、JSRT、EarthScape
>
> U-Net + ResNet-18；Dice、mIoU
>
> IQA
>
> KADID-10k、KonIQ-10k、LDCTIQA
>
> 回归头；SROCC、PLCC
>
> MAE 使用 ViT 编码器，其他大多数方法使用 ResNet-18。所有实验在 Intel Xeon、128 GB 内存、2 张 RTX A4000（每张 16 GB）上完成。
>

### 原 PPT 第 173 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-173.png]]

> [!quote]- 本页可搜索文字
> 图像分类+图像分割
>
> 图像分类：CIFAR-10 
>
> 100% 标签：Colorization-JT Accuracy 0.9099，显著高于 PFT 0.5090 
>
> 10% 标签：Colorization-JT 0.7715，高于 PFT 0.4388 
>
> 说明：JT 在充分监督和少标签场景下都能提升分类性能 
>
> 图像分割：ISIC / EarthScape 
>
> ISIC：MoCo-JT Dice/mIoU 0.9123/0.8704，高于 PFT 0.8946/0.8540 
>
> EarthScape：Rotation-JT mIoU 0.4281，高于 PFT 0.3187 
>
> 但 DINO 在 EarthScape 中 PFT 更优：0.3612 vs JT 0.3357 
>
> 结论 
>
> JT 对分类和分割有效，尤其在生成式或空间结构匹配的代理任务中更明显 
>
> 不同 SSL 方法对 JT/PFT 的适配性不同
>
> JT 在分类和分割任务中整体表现较强，但效果依赖 SSL 任务类型。
>

### 原 PPT 第 174 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-174.png]]

> [!quote]- 本页可搜索文字
> 目标检测+图像质量评估
>
> 检测任务中 JT 与 PFT 性能接近，但 JT 显著节省训练时间。
>
> 任务场景：COCO 检测，10% 标签 
>
> DINO-PFT 训练时间：21.3 h 
>
> DINO-JT 训练时间：4.3 h 
>
> mAP@50 差异约 0.001 
>
> 结果解读 
>
> 在检测精度几乎相同的情况下，JT 的主要优势是效率 
>
> JT 避免了“先预训练、再微调”的两阶段流程 
>
> 结论 
>
> 对目标检测而言，JT 不一定显著提升精度 
>
> 但在低标签和资源受限场景下，JT 更具训练效率优势 
>

### 原 PPT 第 175 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-175.png]]

> [!quote]- 本页可搜索文字
> 泛化能力+效率分析+对抗鲁棒性+可解释性+特征分析
>
> JT 的收益不是单一维度，而体现在数据效率、鲁棒性和训练效率上；但跨域泛化并不总是优于 PFT。
>
> 泛化能力 
>
> CrisisMMD → DMD，10% 标签 
>
> SimCLR-PFT 跨域 Accuracy 0.8037，高于 JT 0.6771 
>
> 说明：对比式方法在分布偏移下，PFT 迁移能力可能更强 
>
> 对抗鲁棒性 
>
> CIFAR-10，对抗噪声强度 0.1 
>
> Colorization-JT 0.8782，高于 PFT 0.3993 
>
> 说明：部分 JT 方法在轻度扰动下仍能保持优势 
>
> 效率分析 
>
> ISIC：论文报告 JT 训练时间约为 PFT 的 1/4 
>
> COCO：JT 4.3 h vs PFT 21.3 h 
>
> 说明：JT 的重要价值在于减少训练流程和时间成本 
>
> 可解释性 / 特征分析 
>
> JT 可能学习到更贴近下游任务的表征 
>
> 但若 SSL 目标与任务结构不匹配，JT 可能削弱泛化能力 
>
> 结论：JT 是否有效，取决于 SSL 目标、任务类型与数据分布是否一致
>

### 原 PPT 第 176 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-176.png]]

> [!quote]- 本页可搜索文字
> 06
>
> 论文结论与启发
>

### 原 PPT 第 177 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-177.png]]

> [!quote]- 本页可搜索文字
> 结论与启发
>
> 实际条件
>
> 更值得优先尝试
>
> 原因
>
> 标签很少，无标注样本丰富
>
> JT
>
> 让两类数据在同一阶段共同优化，数据效率较高
>
> 预文本任务是重建、颜色化或旋转等辅助任务
>
> JT
>
> 更容易借助标签将结构信息对齐到任务语义
>
> 需要快速迭代、预算有限
>
> JT
>
> 消除顺序预训练阶段，常可显著减少总时间
>
> 强调跨域迁移或分布偏移
>
> PFT 作为稳健基线
>
> 对比式表示在实验中常体现更稳定的迁移性
>
> 数据具有严格空间/物理含义
>
> 先检查代理任务匹配性
>
> 不匹配的变换会造成梯度冲突，例如医学图像中的旋转预测
>
> 训练范式的选择会受到 SSL 目标、标注规模、任务类型和领域偏移共同影响。
>
> 01
>
> 02
>
> 03
>
> JT 的强项是标签效率和训练效率。在低标注以及 MAE、颜色化、旋转等重建/辅助目标中，JT 常具有明显优势。
>
> PFT 的强项是稳定的迁移性。在一些对比式 SSL 方法和跨域设置中，先预训练再训练下游头仍然更加可靠
>

### 原 PPT 第 178 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-178.png]]

> [!quote]- 本页可搜索文字
> 感谢观看
>
> THANK YOU
>
> 汇报人：沈徐敏
>
> 第一组序号11
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-UFXHC76Q - Revisiting Self-Supervised Visual Representation Learning|Revisiting Self-Supervised Visual Representation Learning]] — 中关联；共同研究内容：基准与数据合成、视觉自监督。
- [[Zotero Knowledge/Papers/ZK-67T4CPZ5 - Barlow Twins  Self-Supervised Learning via Redundancy Reduction|Barlow Twins: Self-Supervised Learning via Redundancy Reduction]] — 中关联；共同研究内容：基准与数据合成、视觉自监督。

<!-- content-relations:end -->
