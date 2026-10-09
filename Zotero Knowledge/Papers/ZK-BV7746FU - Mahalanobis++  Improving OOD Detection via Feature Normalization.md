---
type: "literature"
title: "Mahalanobis++: Improving OOD Detection via Feature Normalization"
aliases: ["Mahalanobis++"]
zotero_keys: ["BV7746FU"]
year: 2025
authors: ["Müller, Maximilian", "Hein, Matthias"]
venue: "ICML 2025"
doi: ""
url: "https://arxiv.org/abs/2505.18032"
collections: ["06 Alignment & Reliability/Robustness & OOD", "90 Projects/Pattern Recognition Course/Project 1/Group 1"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-1", "concept/微调策略与泛化鲁棒性", "concept-primary/微调策略与泛化鲁棒性"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [140, 154]
imported_at: "2026-10-03"
---

# Mahalanobis++: Improving OOD Detection via Feature Normalization

[在 Zotero 打开](zotero://select/library/items/BV7746FU) · [论文来源](https://arxiv.org/abs/2505.18032) · [论文 PDF](https://arxiv.org/pdf/2505.18032)

## 文献导读

在拟合类别均值和共享协方差前先归一化特征，缓解特征模长变化对 Mahalanobis OOD 分数的影响。比较检测指标时需要统一模型、数据与阈值协议。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Robustness & OOD/索引|06 Alignment & Reliability/Robustness & OOD]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-W8UL68IN - Fine-Tuning can Distort Pretrained Features and Underperform Out-of-Distribution|LP-FT]]
- [[Zotero Knowledge/Papers/ZK-FWQPPDF7 - Is the Modality Gap a Bug or a Feature  A Robustness Perspective|Modality Gap Robustness]]

## 原始摘要

Detecting out-of-distribution (OOD) examples is an important task for deploying reliable machine learning models in safety-critial applications. While post-hoc methods based on the Mahalanobis distance applied to pre-logit features are among the most effective for ImageNet-scale OOD detection, their performance varies significantly across models. We connect this inconsistency to strong variations in feature norms, indicating severe violations of the Gaussian assumption underlying the Mahalanobis distance estimation. We show that simple $\ell_2$-normalization of the features mitigates this problem effectively, aligning better with the premise of normally distributed data with shared covariance matrix. Extensive experiments on 44 models across diverse architectures and pretraining schemes show that $\ell_2$-normalization improves the conventional Mahalanobis distance-based approaches significantly and consistently, and outperforms other recently proposed OOD detection methods.

来源：[论文官方页面](https://arxiv.org/abs/2505.18032)。

正式作者拼写与会议年份依据 [ICML 2025 Proceedings](https://proceedings.mlr.press/v267/muller25a.html)。

## PPT 文献分享原页

来源：[第 1 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC1%E5%B0%8F%E7%BB%84%281%29.pptx)，原文件第 140–154 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 140 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-140.png]]

> [!quote]- 本页可搜索文字
>     文献汇报
>
> Mahalanobis++: Improving OOD Detection via Feature Normalization
>
> 王婉越
>
> 9/23
>

### 原 PPT 第 141 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-141.png]]

> [!quote]- 本页可搜索文字
> CONTENTS 
>
> 目录
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
> 本文解决方案
>
> 04
>
>    核心创新点
>
> 05
>
> 论文有效性  
>
> 06
>
> 结论与启发  
>

### 原 PPT 第 142 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-142.png]]

> [!quote]- 本页可搜索文字
>      研究动机  
>
> 01
>

### 原 PPT 第 143 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-143.png]]

> [!quote]- 本页可搜索文字
> 研究动机  
>
> OOD检测  
>
>     神经网络在训练分布内的数据上可能表现很好，但遇到训练阶段没有见过的 Out-of-Distribution（OOD）样本 时，仍然可能输出非常高置信度的错误预测。例如一个 ImageNet 分类器输入：噪声图片；医学图片；完全不同领域的图片；模型有可能仍然非常自信地把它分类成 ImageNet 的某个类别。因此 OOD detection 的任务就是：
>
> Mahalanobis的不稳定性 
>
>     已有 OOD 方法可以分成：Training-time(修改训练过程,修改 loss,需要重新训练);Post-hoc(不改变 pretrained model,训练完成后直接使用,部署成本低)。对于大规模 pretrained models，Post-hoc更加高效。即模型训练完以后，直接利用已有模型的 logits 或 feature 做 OOD detection。而在 ImageNet-scale 的 post-hoc OOD detection 中，Mahalanobis distance 是一个非常简单而且很强的 baseline。
>
>      Mahalanobis利用 pre-logit feature,计算每个类别中心的Mahalanobis距离，离所有 ID 类别中心越远，就越倾向于认为它是 OOD。Mahalanobis 虽然很强，但在不同模型上的 OOD 检测性能差异非常大。因此，本文的核心研究问题是：为什么相同的MahalanobisDetector在不同模型上表现差异如此巨大？
>

### 原 PPT 第 144 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-144.png]]

> [!quote]- 本页可搜索文字
>      现存痛点    
>
> 02
>

### 原 PPT 第 145 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-145.png]]

> [!quote]- 本页可搜索文字
> 现存痛点  
>
> Mahalanobis 的统计假设不一定成立  
>
> 假设1：不同类别 feature 应近似服从 Gaussian distribution。
>
> 假设2：对于所有类别共享一个协方差矩阵
>
> 实际feature space不满足Mahalanobis的统计假设
>
> Feature Norm 出现异常变化  
>
> 理论上feature norm应该比较集中，在高维高斯空间中集中在附近。通过比较高斯模拟器数据和真实神经网络特征发现真实 feature norm：类别之间差异很大，类别内部差异也很大，存在明显 heavy-tail。 
>
> Feature Norm 干扰 OOD Score  
>
> 通过分析feature norm与的关系，实验发现无论ID还是OOD，具有较大特征范数的样本始终获得较大的 OOD 分数，而具有较小特征范数的样本则相反。导致对于小范数的样本，例如：黑色图像；单色图像；简单 noise image。这些本应很容易检测的 far-OOD，传统 Mahalanobis 反而可能漏检。Feature norm 成为了 Mahalanobis OOD detection 中的一个 confounding factor。
>
> 01
>
> 03
>
> 02
>
> 传统 Mahalanobis 高度依赖 Gaussian + shared covariance 假设，实际深度特征存在显著差异使统计假设失效，并导致 Mahalanobis score 被 feature norm 严重干扰，从而产生跨模型性能不稳定以及 small-norm OOD 漏检问题。
>

### 原 PPT 第 146 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-146.png]]

> [!quote]- 本页可搜索文字
> 本文解决方案
>
> 03
>
> Mahalanobis++ 的核心并不是设计了一个更复杂的 OOD detector，而是通过简单的 feature normalization，使特征空间重新更符合 Mahalanobis distance 所依赖的统计假设。 
>

### 原 PPT 第 147 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-147.png]]

> [!quote]- 本页可搜索文字
>     解决方案  
>
> 去掉 Norm，只保留 Direction
>
> 核心思路
>
> Feature 可以拆成：
>
> 01
>
> Mahalanobis 分数的类均值与协方差矩阵是利用归一化特征进行估计的；而在计算测试样本的分数时，亦对测试特征进行归一化处理。
>
> 解决方法：L2Feature Normalization
>
> 不再使用原始特征，而是使用L2归一化后的特征计算马氏距离,class mean；估计 shared covariance；对测试样本归一化
>
> 02
>
> 由于norm会干扰 Mahalanobis score，因此提出：
>
> 即Feature=Norm  Direction
>
> Mahalanobis
>
> Mahalanobis++
>

### 原 PPT 第 148 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-148.png]]

> [!quote]- 本页可搜索文字
>   核心创新点
>
> 04
>

### 原 PPT 第 149 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-149.png]]

> [!quote]- 本页可搜索文字
>   核心创新点  
>
> [
>
> 方法创新
>
> 极简的 post-hoc Feature Normalization，其优势是：不需要重新训练；不修改 backbone；不改变网络架构；基本不引入额外超参数；
>
> 可以应用于现成 pretrained models。
>
> 理论创新
>
> 解释了 Mahalanobis OOD 失效的机制，将Mahalanobis失效和Gaussian假设失效与Feature Norm异常变化和OOD Score联系起来，并用实际 feature distribution 证明真实模型偏离这一假设。
>
> 性能创新
>
> 跨 44 个模型稳定提升，与Mahalanobis相比，FPR 平均改善7.6%，并在41/44个模型上优于Mahalanobis，并且平均比 ViM 低约 7 个 FPR points
>
> 场景创新
>
> 增强跨模型 post-hoc 适用性，主要拓展了 Mahalanobis-based detector 在大规模、跨架构、跨预训练方案、无需重新训练场景下的稳定适用性。
>
> 覆盖：ImageNet；CIFAR100；CNN，Vision Transformer；ConvNeXt等多个场景
>
> 从机制解释到方法改进：用最简单的特征归一化，解决 Mahalanobis OOD 检测的跨模型不稳定问题。
>

### 原 PPT 第 150 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-150.png]]

> [!quote]- 本页可搜索文字
>   论文有效性
>
> 05
>

### 原 PPT 第 151 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-151.png]]

> [!quote]- 本页可搜索文字
>   论文有效性
>
> 发现性能异常
>
> 比较不同 pretrained models，SwinV2:58.2%FPR和ViT-augreg:31.3%FPR，说明Mahalanobis确实存在明显的跨模型不稳定。
>
> 比较理论 Gaussian feature norm 和实际 neural feature norm，发现高斯假设确实存在严重偏离。shared covariance assumption
>
> 找到关键因素—Feature Norm
>
> 人为改变 OOD sample 的 feature norm，但保持 feature direction 不变，发现特征范数越小 OOD分数越小
>
> 大规模 benchmark 
>
> ImageNet：44 pretrained models，多种 architectures，多种 training schemes。
>
> CIFAR100，更换数据集证明不是只有 ImageNet 有效。
>
> Noise / Far-OOD Unit Tests：进一步证明 Mahalanobis++对极端 far-OOD 的鲁棒性改善
>
> 验证 Mahalanobis++ 是否真的修复了“机制”
>
> 不仅验证：Accuracy/FPR提高，还验证normalization 有没有真正解决前面发现的问题。 
>
> 验证A：Normality improved
>
> 验证B：Variance alignment improved
>
> 验证C：Norm-score correlation decreased
>
> 三个验证结果表明，归一化特征分布更接近高斯分布，不同类别的协方差矩阵更一致且L2归一化后small-norm OOD 也可以正确检测
>

### 原 PPT 第 152 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-152.png]]

> [!quote]- 本页可搜索文字
>   结论与启发
>
> 06
>

### 原 PPT 第 153 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-153.png]]

> [!quote]- 本页可搜索文字
>    结论与启发 
>
> 项目完成进度 
>
> 单击此处输入你的正文，文字是您思想的提炼，为了最终演示发布的良好效果，请尽量言简意赅的阐述观点；根据需要可酌情增减文字，以便观者可以准确理解您所传达的信息。单击此处输入你的正文，文字是您思想的提炼，为了最终演示发布的良好效果，请尽量言简意赅的阐述观点； 
>
> 结论一
>
> Mahalanobis 失效原因
>
> 传统 Mahalanobis 的问题不仅来自距离本身
>
> 真实FeatureSpace可能不满足Mahalanobis假设
>
> 结论二
>
> 特征范数与OOD分数错误耦合
>
> Feature norm 是一个重要影响因素
>
> Norm Variation→Mahalanobis Score Bias
>
> 结论三
>
> L2 特征归一化
>
> 去除特征范数，只保留方向信息
>
> 即可减弱 norm-score correlation，提高OOD检测
>
> 最终结果：Mahalanobis++在41/44个模型上OOD检测性能高于Mahalanobis
>
> 启发1
>
> 先解释失败再设计方法
>
> 在进行方法改进时，发现异常—>寻找原因—>针对设计方法,而不是直接堆模型
>
> 启发2
>
> 数学假设同样重要
>
> 使用数学公式时，不能只关注公式本身，还应该关注实际 neural representation 是否满足这个公式背后的统计假设
>
> 启发3
>
> Magnitude 和 Direction 可以分开研究
>
> feature norm 不一定总是有用信息，在部分任务中甚至可能成为干扰因素。
>
> 启发4
>
> 分类准确率 ≠ OOD能力
>
> 不同 training scheme 会塑造不同的 feature space
>
> 评价 pretrained model 应关注 accuracy 之外的可靠性指标
>

### 原 PPT 第 154 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 1/slide-154.png]]

> [!quote]- 本页可搜索文字
> 感谢老师的批评指正
>
> 王婉越
>
> 9/23
>
> Mahalanobis++: Improving OOD Detection via Feature Normalization
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-W8UL68IN - Fine-Tuning can Distort Pretrained Features and Underperform Out-of-Distribution|Fine-Tuning can Distort Pretrained Features and Underperform Out-of-Distribution]] — 中关联；共同研究内容：鲁棒性与域外泛化。

<!-- content-relations:end -->

<!-- research-integration:start -->
## 研究主题入口

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Robustness & OOD/索引|06 Alignment & Reliability/Robustness & OOD]]

## 概念比较入口

- [[Zotero Knowledge/Concepts/微调策略与泛化鲁棒性|微调策略与泛化鲁棒性]]
<!-- research-integration:end -->
