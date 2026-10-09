---
type: "literature"
title: "Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere"
aliases: ["Alignment & Uniformity"]
zotero_keys: ["88IZNLUX"]
year: 2020
authors: ["Wang, Tongzhou", "Isola, Phillip"]
venue: "ICML 2020"
doi: ""
url: "https://arxiv.org/abs/2005.10242"
collections: ["02 Representation & Perception/Visual Representation Learning", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [99, 112]
imported_at: "2026-10-03"
---

# Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere

[在 Zotero 打开](zotero://select/library/items/88IZNLUX) · [论文来源](https://arxiv.org/abs/2005.10242) · [论文 PDF](https://arxiv.org/pdf/2005.10242)

## 文献导读

从单位超球面上的正样本对齐与整体均匀分布解释对比学习。两项指标提供表征诊断视角，不能脱离任务把单一指标的降低直接解释为性能提高。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-YMBWZADV - A Simple Framework for Contrastive Learning of Visual Representations|SimCLR]]
- [[Zotero Knowledge/Papers/ZK-BYZ75H5L - Connect, Collapse, Corrupt  Learning Cross-Modal Tasks with Uni-Modal Data|C3]]

## 原始摘要

Contrastive representation learning has been outstandingly successful in practice. In this work, we identify two key properties related to the contrastive loss: (1) alignment (closeness) of features from positive pairs, and (2) uniformity of the induced distribution of the (normalized) features on the hypersphere. We prove that, asymptotically, the contrastive loss optimizes these properties, and analyze their positive effects on downstream tasks. Empirically, we introduce an optimizable metric to quantify each property. Extensive experiments on standard vision and language datasets confirm the strong agreement between both metrics and downstream task performance. Remarkably, directly optimizing for these two metrics leads to representations with comparable or better performance at downstream tasks than contrastive learning. Project Page: this https URL Code: this https URL , this https URL

来源：[论文官方页面](https://arxiv.org/abs/2005.10242)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 99–112 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 99 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-099.png]]

> [!quote]- 本页可搜索文字
> Understanding Contrastive RepresentationLearning through Alignment and Uniformityon the Hypersphere
>
> [ICML 2020 ] Tongzhou Wang  ·  Phillip Isola
>
> 核心问题：对比学习为什么能够学出好的表征？
>
> 本文答案：Alignment（局部对齐） + Uniformity（全局均匀）
>
> 汇报人丨2612141 余兆舒
>
> 时间丨2026.9.23
>
> 组别丨第一组
>

### 原 PPT 第 100 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-100.png]]

> [!quote]- 本页可搜索文字
> 1 研究动机：对比学习为何有效？从 InfoMax 到超球面几何
>
> 02 / 10
>
> 传统解释：InfoMax / Mutual Information
>
> 100
>
> 01
>
> 正样本对：同一样本的两个随机增强视图  x, y  →  z=f(x),  z⁺=f(y)
>
> InfoMax：让两种视图的表示共享尽可能多的信息
>
> 互信息衡量“知道 Z⁺ 后，Z 的不确定性减少了多少”
>
> 02
>
> InfoNCE：互信息（MI）下界
>
> 关键缺口：更紧的 MI 下界  ≠  更好的 downstream representation。
>
> 03
>
> 实践事实：特征被 L2 归一化
>
> 大量对比学习方法强制  ||f(x)||₂ = 1
>
> 
> 因此表示不是任意欧氏向量，而是落在单位超球面上
>
> 04
>
> 因此作者改问一个更直接的问题
>
> 不再只问：“表示保留了多少互信息？”
>
> 而是直接问：“contrastive loss 在球面上到底应该把表示塑造成什么几何结构？”
>
> 信息论解释
>
> →
>
> 几何性质解释
>
> 研究动机：解释对比学习为何、如何有效
>
> 实际训练通常不直接计算互信息，而是用 1 个正样本 + M 个负样本构造 InfoNCE：
>
> 最小化 InfoNCE  ⇒  提高互信息下界；这就是经典 InfoMax 解释。
>

### 原 PPT 第 101 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-101.png]]

> [!quote]- 本页可搜索文字
> 2 现存痛点：已有理论与评估体系缺乏“几何诊断”
>
> 与研究动机区分：这里不再重复 MI/InfoNCE 的动机，而聚焦“已有工作具体解释不了什么”。
>
> 03 / 10
>
> 01
>
> Negative 数量：已有理论与经验规律冲突
>
> 02
>
> “把点推远”并不等于“均匀分布”
>
> 03
>
> 理论侧：latent-class 分析可得到“大 M 可能使表示质量受损”的结论。 [1][5]
>
> 经验侧：Instance Discrimination / MoCo / SimCLR 反而普遍受益于更大的负样本集合或 batch。 [2-4]
>
> 缺口：若理论解释不了 M↑ 为何常有效，就还没有抓住 contrastive loss 的主导机制。
>
> 均匀分布
>
> 两点反极
>
> 关键恒等式：单位球面上，平均平方距离只由均值 E[u] 决定。 [5]
>
> 反例：“均匀铺满球面”和“只落在 ±u 两点”都可满足 E[u]=0，因此简单平均距离无法区分两者。
>
> 缺口：需要一个真正刻画全局分布、且以球面均匀分布为唯一最优解的 metric。
>
> 参考文献
>
> [1] Saunshi, N., Plevrakis, O., Arora, S., Khodak, M., & Khandeparkar, H. (2019). A Theoretical Analysis of Contrastive Unsupervised Representation Learning. Proceedings of the 36th International Conference on Machine Learning, PMLR 97, 5628–5637.
>
> [2] Wu, Z., Xiong, Y., Yu, S. X., & Lin, D. (2018). Unsupervised Feature Learning via Non-Parametric Instance Discrimination. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 3733–3742.
>
> [3] He, K., Fan, H., Wu, Y., Xie, S., & Girshick, R. (2020). Momentum Contrast for Unsupervised Visual Representation Learning. Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 9729–9738.
>
> [4] Chen, T., Kornblith, S., Norouzi, M., & Hinton, G. (2020). A Simple Framework for Contrastive Learning of Visual Representations. Proceedings of the 37th International Conference on Machine Learning, PMLR 119, 1597–1607.
>
> [5] Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. Proceedings of the 37th International Conference on Machine Learning, PMLR 119, 9929–9939.
>
> Alignment / Uniformity 缺少可量化、可验证的指标
>
> Alignment
>
> Uniformity
>
> 过去更多是“设计直觉”
>
> 如何直接量化？
>
> 原文现状：Alignment / Uniformity 常被当作 representation learning 的动机，但文献中缺少深入理解。[5]
>
> 两个未知：它们是否真的由 contrastive learning 产生？是否真的与 downstream representation quality 一致？[5]
>
> 缺口：需要可计算、可分别诊断、还能直接优化的两个内在几何指标 → 后文 与 。
>

### 原 PPT 第 102 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-102.png]]

> [!quote]- 本页可搜索文字
> 3  本文解决方案：把“好表征”形式化为两个可优化目标
>
> 04 / 10
>
> 01
>
> Alignment：把正样本的不变性写成距离目标
>
> 几何含义：单位球面上最小化距离 = 最大化正样本余弦/点积相似度；它约束的是“同一语义视图应落到同一局部”。
>
> 02
>
> Uniformity：把全局分布写成势能目标
>
> 分布含义：优化对象不再是某一对样本，而是编码后分布 μ_f；目标是让 μ_f 接近球面均匀测度 σ。
>
> 03
>
> 把两个度量直接组成训练目标
>
> 参数作用：α 决定 Alignment 对大距离的惩罚；t 决定 Gaussian kernel 对“近邻拥挤”的敏感尺度；λ 控制局部不变性与全局铺开的权衡。
>
> 结构性 trade-off：有限数据 + augmentation 下，Perfect Alignment 会把同一原样本的视图压成一点；Perfect Uniformity 则要求分布连续铺满球面，两者存在结构性张力。
>
> 这一步的贡献：把“直觉性质”变成可计算、可微、可直接优化的损失。
>
> Fig. 6｜两项损失不到 10 行即可实现
>
> 代码对应：positive pair → lalign；batch 内 pairwise distance → lunif；两视图 uniformity 取平均。
>
> Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. ICML, PMLR 119, 9929–9939.
>

### 原 PPT 第 103 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-103.png]]

> [!quote]- 本页可搜索文字
> 3  本文解决方案：Uniformity 的严格理论基础
>
> 05 / 10
>
> 01
>
> Gaussian potential → 分布能量
>
> 用  表示 feature 在单位球面上的概率分布近点：≈1，拥挤会显著抬高能量；远点：→0。于是“均匀”被转化为最小化整个分布的 pairwise potential。
>
> 02
>
> Proposition 1：唯一极小分布
>
> 关键不是“存在一个均匀解”，而是 uniform measure 是唯一 minimizer。理论基础来自 Gaussian kernel 的 strict positive definiteness。
>
> 03
>
> Proposition 2：有限点也趋向均匀
>
> 对  个点最小化平均势能，得到最优点集 ；当 ，其经验测度weak-* convergence到
>
> Fig. 4｜Gaussian potential 数值越小，分布越接近真正的 uniform
>
> 从 Random Init 0.8474 → 混合分布 0.3439 → Supervised 0.2380 → Contrastive 0.2088 → Uniform samples 0.2070；该排序与“肉眼看到的均匀程度”一致。
>
> Appendix：Uniformity loss 的可解释范围
>
> 上界 0 对应完全 collapse；维度升高时最优下界逼近 −2t。
>
> Wang, T., & Isola, P. (2020). ICML, PMLR 119, 9929–9939.  |  Cohn, H., & Kumar, A. (2007). Universally optimal distribution of points on spheres. Journal of the AMS, 20(1), 99–148.  |  Borodachov, S. V., Hardin, D. P., & Saff, E. B. (2019). Discrete Energy on Rectifiable Sets. Springer.
>

### 原 PPT 第 104 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-104.png]]

> [!quote]- 本页可搜索文字
> 3  本文解决方案：InfoNCE 的渐近分解
>
> 06 / 10
>
> Theorem｜Asymptotics of 
>
> 固定 τ>0，当负样本数 M→∞：
>
> ① positive term → Alignment
>
> ② negative aggregate → Uniformity
>
> 01
>
> 第一项为何等价于 Alignment？
>
> 单位球面把“点积最大化”和“平方距离最小化”变成同一个目标。因此第一项的 minimizer 就是 Perfect Alignment。
>
> 结论：正样本吸引是渐近 loss 的第一项
>
> 02
>
> 第二项如何连接 Gaussian Uniformity？
>
> 把 dot-product exponential 改写成 Gaussian kernel 后，可得到 t=1/(2τ)。论文证明：第二项与 L_uniform 具有相同的 uniform minimizer；L_uniform 只是把 log 的位置调整为更简洁、可直接优化的形式。
>
> 结论：大量 negatives 形成“全局分布压力”
>
> 有限 M 也会快速接近渐近结论；Appendix Theorem 2 进一步证明：若 Perfect A+U 可实现，M=1 时它们也是 exact minimizers（但该结论更弱）。
>
> → 直接训练 A + U
>
> Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. Proceedings of ICML, PMLR 119, 9929–9939.
>

### 原 PPT 第 105 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-105.png]]

> [!quote]- 本页可搜索文字
> 4  核心创新点
>
> 01
>
> 结构化诊断：把表征质量变成二维坐标
>
> MEASURE
>
> 02
>
> 诊断 → 干预：同一组量既能测，也能训练
>
> INTERVENE
>
> 03
>
> 框架迁移：跨算法、跨模态仍保持一致
>
> TRANSFER
>
> 核心变化：作者把 encoder 的质量放进 (, ) 二维坐标，而不是只留下一个 accuracy。
>
> • Fig. 5：304 个 STL-10 + 64 个 NYU-Depth-v2 encoder，训练目标不同，但高性能模型都聚集在低 A / 低 U 区域。
>
> • 这使 A/U 成为一种 representation-level diagnostic axes：不仅比较模型，还能区分“局部不变性不足”与“全局分布失衡”。
>
> INSIGHT  A/U 不只是某个 loss 的附属统计量，更是“表征坐标系”
>
> 核心变化：论文把“解释指标”直接变成“控制变量”——同一组量同时承担 measure / predict / optimize 三种角色。
>
> • Fig. 6：两项 loss 在 minibatch 内用简单 pairwise 运算即可实现，代码不到 10 行；不需要额外 critic 或 MI estimator。
>
> • 更重要的是：后续 finetuning 实验把 A/U 当作干预旋钮——只改善一项会牺牲另一项，同时改善二者才持续提升 accuracy。
>
> INSIGHT  真正的新能力是“发现失衡后，知道该往哪个几何方向修正”
>
> 核心变化：作者没有把 A/U 绑定在原始 InfoNCE 上，而是检验它是否跨 algorithm / modality 仍然成立。
>
> • Fig. 9：MoCo / ImageNet-100 与 Quick-Thought / BookCorpus 的训练机制、数据模态都不同，但低 A / 低 U 仍对应更好的 downstream performance。
>
> • 因此：论文贡献不能简单理解为“一个替代 InfoNCE 的新 loss”，而是提出了更一般的 representation principle。
>
> INSIGHT  当训练配方改变而“坐标系”仍有效，它才具备框架级解释力
>
> 核心 insight：这项工作把对比学习研究从“优化哪个 loss”推进到“如何诊断、干预并验证表征几何”。
>
> Ref.
>
> [1] Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. ICML, PMLR 119, 9929–9939.
>
> [2] He, K., Fan, H., Wu, Y., Xie, S., & Girshick, R. (2020). Momentum Contrast for Unsupervised Visual Representation Learning. CVPR, 9729–9738.
>
> [3] Logeswaran, L., & Lee, H. (2018). An Efficient Framework for Learning Sentence Representations. ICLR.
>

### 原 PPT 第 106 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-106.png]]

> [!quote]- 本页可搜索文字
> 5  论文如何论证有效性：先证明“几何现象”确实出现
>
> 08 / 14
>
> 观察
>
> 预测
>
> 必要性
>
> 干预
>
> 迁移
>
> 结果
>
> 读图方式：左列是 positive-pair 距离；中列是全局角度密度；右侧按类别看局部占据区域。
>
> 原文观察：contrastive representation 同时呈现更紧的正样本关系与更均匀的球面覆盖。
>
> 重要细节：这个 2-D sanity check 中 supervised linear accuracy 为 57.19%，contrastive 为 28.60%。所以 Fig.3 不是“谁 accuracy 更高”的比较，而是在验证作者提出的几何量确实能被观测。
>
> 证据边界：“看见 A/U”只能说明现象存在，还不能说明它们能预测 representation quality。下一步必须跨大量 encoder 检查。
>
> 从representation本身出发：先确认A/U不是理论想象，而是训练后可直接观察的统计结构
>
> Ref.
>
> Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. Proceedings of ICML, PMLR 119, 9929–9939.
>

### 原 PPT 第 107 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-107.png]]

> [!quote]- 本页可搜索文字
> 5  论文如何论证有效性：大规模 sweep 检验“预测性”
>
> 09 / 14
>
> 观察
>
> 预测
>
> 必要性
>
> 干预
>
> 迁移
>
> 结果
>
> Fig. 5｜每个点 = 一个独立训练的 encoder；颜色 = downstream performance
>
> 实验同时扫描 loss 权重、temperature、α、t、batch size、embedding dim、训练轮数 / LR 与初始化——有意打破“只在一个 setting 里相关”的可能性。
>
> 为什么这个 sweep 有说服力？
>
> 覆盖面：304 个 STL-10 encoder + 64 个 NYU-Depth-v2 encoder；不是一次训练的偶然相关。
>
> 不同 readout：STL-10 同时看 output linear 与 fc7 5-NN；NYU 看 conv5 depth MSE，评价头和任务形式都不同。
>
> 稳定结构：高性能点持续落在低 L_align / 低 L_uniform 区域；分类看 accuracy，深度任务看 MSE，方向仍一致。
>
> 真正意义：A/U 开始具representation-level predictor 的资格：训练配方改变后，它们仍能对 encoder 质量排序。
>
> 但这仍是跨模型相关性：还不能回答“主动改变A/U，会不会真的改变性能？”
>
> Ref.
>
> Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. Proceedings of ICML, PMLR 119, 9929–9939.
>

### 原 PPT 第 108 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-108.png]]

> [!quote]- 本页可搜索文字
> 5  论文如何论证有效性：必要性 + 鲁棒区间，而非“单指标越低越好”
>
> 10 / 14
>
> 观察
>
> 预测
>
> 必要性
>
> 干预
>
> 迁移
>
> 结果
>
> Fig. 7｜STL-10：从 align-only 连续扫到 uniform-only
>
> 实验变量：只改变二者相对权重
>
> 倒 U 型性能： 从一端扫到另一端时，validation accuracy 在中间区域最高；两个端点都不是好表示。
>
> 退化机制可见：Alignment 权重远高于 Uniformity 时，所有输入会映射到同一个 feature；原文指出此时 ，即发生 collapse。
>
> 不是“精密调参”：只要两项权重比不过度失衡（论文举例 < 4），representation quality 对精确权重相对不敏感。
>
> 更深的含义：A/U 应被理解为联合约束，而不是两个可独立追求极值的分数；好模型处在一个“可行盆地”中。
>
> 这一步验证 “必要性 + 稳健性”：
>
> A/U 两者缺一不可，但也不需要把  调到单一精确点
>
> Ref.
>
> Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. Proceedings of ICML, PMLR 119, 9929–9939.
>

### 原 PPT 第 109 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-109.png]]

> [!quote]- 本页可搜索文字
> 5  论文如何论证有效性：从相关性升级为“同一模型上的干预”
>
> 11 / 14
>
> 观察
>
> 预测
>
> 必要性
>
> 干预
>
> 迁移
>
> 结果
>
> Fig. 8｜同一  的次优 STL-10 encoder，三种 finetuning 轨迹
>
> 每个 checkpoint 都重新测 A/U，并“从头训练”线性分类器，因此 accuracy 变化不是继承旧 classifier 造成的。
>
> 三种 intervention 的判别力
>
> 只优化 Alignment：L_align 改善，但 Uniformity 与 accuracy 同时恶化。
>
> 只优化 Uniformity：L_uniform 改善，但 Alignment 与 accuracy 同时恶化。
>
> 联合优化：两项几何状态朝兼容方向移动时，validation accuracy 持续上升。
>
> 为什么更强：这里控制了初始化、模型与数据，只改变优化方向；证据从“跨 encoder 相关”提升为“同一 encoder 内的定向干预”。
>
> A/U不只是performance的伴随统计量；沿这两个轴移动representation，会系统地改变下游质量。
>
> Ref.
>
> Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. Proceedings of ICML, PMLR 119, 9929–9939.
>

### 原 PPT 第 110 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-110.png]]

> [!quote]- 本页可搜索文字
> 5  论文如何论证有效性：换算法、换模态后，几何坐标仍然有效
>
> 12 / 14
>
> 观察
>
> 预测
>
> 必要性
>
> 干预
>
> 迁移
>
> 结果
>
> Fig. 9｜MoCo / ImageNet-100 与 Quick-Thought / BookCorpus
>
> 45 个 ImageNet-100 encoder + 108 个 BookCorpus encoder：
>
> 不同方法下，低 A / 低 U 区域仍聚集更好的模型。
>
> 真正的“外部效度”
>
> MoCo：引入memory queue与momentum encoder，训练机制已不再等同于最基本的 Eq.(1)。
>
> Quick-Thought：文本任务使用两个encoder、相邻句作为positive，并且只在evaluation时归一化输出。
>
> 仍然成立：尽管algorithm / modality / downstream task 都改变，A/U—performance 的二维结构依然保留。
>
> 应如何解读：这支持 A/U 是更一般的 representation property，而不是某个具体 loss 的“内部统计量”。
>
> 边界也要看到：跨模态“关系保留”并不意味着最优权重、最优数值范围完全一致。
>
> Ref.
>
> [1] Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. ICML, PMLR 119, 9929–9939.   [2] He, K., Fan, H., Wu, Y., Xie, S., & Girshick, R. (2020). Momentum Contrast for Unsupervised Visual Representation Learning. CVPR, 9729–9738.   [3] Logeswaran, L., & Lee, H. (2018). An Efficient Framework for Learning Sentence Representations. ICLR.
>

### 原 PPT 第 111 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-111.png]]

> [!quote]- 本页可搜索文字
> 5  论文如何论证有效性：直接训练 A+U——有竞争力，但非普遍占优
>
> 13 / 14
>
> 观察
>
> 预测
>
> 必要性
>
> 干预
>
> 迁移
>
> 结果
>
> Tab. 1–2｜STL-10 + NYU-Depth-v2
>
> Tab. 3–5｜ImageNet-100 + BookCorpus + full ImageNet
>
> STL-10
>
> 80.46 → 81.15
>
> A+U 略优
>
> ImageNet-100
>
> 72.80 → 74.60
>
> A+U +1.80 top-1
>
> NYU conv5 MSE
>
> 0.7024 → 0.7014
>
> 小幅改善
>
> BookCorpus
>
> 77.51/83.86 → 73.76/80.95
>
> A+U 反而更低
>
> ImageNet / MoCo v2
>
> 67.5±0.1 → 67.69
>
> 基本可比
>
> A/U 已经抓住了足够多的机制，使其在多项视觉任务上可直接训练出竞争力表征
>
> BookCorpus 的反例同时说明这两个几何量重要，但并未穷尽所有表示因素
>
> Ref.
>
> [1] Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. ICML, PMLR 119, 9929–9939.   [2] Chen, X., Fan, H., Girshick, R., & He, K. (2020). Improved Baselines with Momentum Contrastive Learning. arXiv:2003.04297.   [3] Logeswaran, L., & Lee, H. (2018). An Efficient Framework for Learning Sentence Representations. ICLR.
>

### 原 PPT 第 112 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-112.png]]

> [!quote]- 本页可搜索文字
> 6  论文结论与启发：从“解释对比学习”到“理解表征几何”
>
> 14 / 14
>
> 01
>
> 论文结论｜作者真正建立了什么
>
> 机制层
>
> 高质量表示要求两个尺度同时成立
>
> positive pair 在局部抵抗增广扰动；整体 feature distribution 在全局避免集中并充分展开。两者共同决定可用 representation。
>
> 理论层
>
> Uniformity 有严格最优分布
>
> 大量 negatives 下，contrastive objective 分离出 positive-pair attraction 与 distribution-level pressure；有限 M 还具有 O(M⁻¹ᐟ²) 的逼近速度。
>
> 实证层
>
> A/U 不只是描述变量
>
> 它们能预测 downstream quality、在同一 encoder 上被主动干预，并在 MoCo / Quick-Thought 等不同训练机制下继续保持解释力。
>
> 预测
>
> 干预
>
> 迁移
>
> 直接训练
>
> 02
>
> 研究启发｜这套视角还能带走什么
>
> 评价范式
>
> 从“只看结果”转向“结果 + 内部几何”
>
> linear probe 告诉我们“好不好”；A/U 这类内在指标进一步告诉我们“为什么好 / 坏”。未来评价体系应同时报告外部性能与 representation 的结构状态。
>
> 目标设计
>
> negative 是手段，不是目的
>
> 设计自监督目标时应显式回答两个问题：如何建立对任务有用的不变性？如何避免 feature concentration / collapse 并保持足够的信息承载能力？
>
> 开放问题
>
> 论文的限制本身就是下一步方向
>
> 为什么 unit hypersphere 特别适合表示学习？A/U 能否充分描述非对比方法？有限数据与有限 batch 下，如何自适应平衡局部一致性和全局分布质量？
>
> 好的 representation 不是“共享信息越多越好”，而是让不该变的保持稳定，让整体表征保持充分展开
>
> Ref.
>
> [1] Wang, T., & Isola, P. (2020). Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. ICML, PMLR 119, 9929–9939.  
>
> [2] He, K., Fan, H., Wu, Y., Xie, S., & Girshick, R. (2020). Momentum Contrast for Unsupervised Visual Representation Learning. CVPR, 9729–9738.   [3] Logeswaran, L., & Lee, H. (2018). An Efficient Framework for Learning Sentence Representations. ICLR.
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-2IQ6RLSK - Sigmoid Loss for Language Image Pre-Training|Sigmoid Loss for Language Image Pre-Training]] — 强关联；共同研究内容：对比学习与跨模态编码。
- [[Zotero Knowledge/Papers/ZK-GDGTULM9 - Unlearning the Noisy Correspondence Makes CLIP More Robust|Unlearning the Noisy Correspondence Makes CLIP More Robust]] — 中关联；共同研究内容：对比学习与跨模态编码。
- [[Zotero Knowledge/Papers/ZK-YMBWZADV - A Simple Framework for Contrastive Learning of Visual Representations|A Simple Framework for Contrastive Learning of Visual Representations]] — 中关联；共同研究内容：对比学习与跨模态编码。

<!-- content-relations:end -->
