---
type: "literature"
title: "AGFT: Alignment-Guided Fine-Tuning for Zero-Shot Adversarial Robustness of Vision-Language Models"
aliases: ["AGFT"]
zotero_keys: ["TGBY7QJ9"]
year: 2026
authors: ["Cui, Yubo", "Guan, Xianchao", "Xiong, Zijun", "Zhang, Zheng"]
venue: "CVPR 2026"
doi: ""
url: "https://arxiv.org/abs/2603.29410"
collections: ["06 Alignment & Reliability/Robustness & OOD", "90 Projects/Pattern Recognition Course/Project 1/Group 2"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [54, 64]
imported_at: "2026-10-03"
---

# AGFT: Alignment-Guided Fine-Tuning for Zero-Shot Adversarial Robustness of Vision-Language Models

[在 Zotero 打开](zotero://select/library/items/TGBY7QJ9) · [论文来源](https://arxiv.org/abs/2603.29410) · [论文 PDF](https://arxiv.org/pdf/2603.29410)

## 文献导读

利用原预训练模型的软预测指导对抗微调，并通过分布一致性校准保留跨模态关系。需要同时评价对抗鲁棒性与零样本泛化。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Robustness & OOD/索引|06 Alignment & Reliability/Robustness & OOD]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-CDHTS2WR - Learning Transferable Visual Models From Natural Language Supervision|CLIP]]
- [[Zotero Knowledge/Papers/ZK-28MFNY9F - CLIP is Strong Enough to Fight Back  Test-time Counterattacks towards Zero-shot Adver|TTC]]
- [[Zotero Knowledge/Papers/ZK-GDGTULM9 - Unlearning the Noisy Correspondence Makes CLIP More Robust|NCU]]

## 原始摘要

Pre-trained vision-language models (VLMs) exhibit strong zero-shot generalization but remain vulnerable to adversarial perturbations. Existing classification-guided adversarial fine-tuning methods often disrupt pre-trained cross-modal alignment, weakening visual-textual correspondence and degrading zero-shot performance. In this paper, we propose an Alignment-Guided Fine-Tuning (AGFT) framework that enhances zero-shot adversarial robustness while preserving the cross-modal semantic structure. Unlike label-based methods that rely on hard labels and fail to maintain the relative relationships between image and text, AGFT leverages the probabilistic predictions of the original model for text-guided adversarial training, which aligns adversarial visual features with textual embeddings via soft alignment distributions, improving zero-shot adversarial robustness. To address structural discrepancies introduced by fine-tuning, we introduce a distribution consistency calibration mechanism that adjusts the robust model output to match a temperature-scaled version of the pre-trained model predictions. Extensive experiments across multiple zero-shot benchmarks demonstrate that AGFT outperforms state-of-the-art methods while significantly improving zero-shot adversarial robustness.

来源：[论文官方页面](https://arxiv.org/abs/2603.29410)。

## 元数据核对

PPT 作者列中写有 Zihao Wang；[论文官方页面](https://openaccess.thecvf.com/content/CVPR2026/html/Cui_AGFT_Alignment-Guided_Fine-Tuning_for_Zero-Shot_Adversarial_Robustness_of_Vision-Language_Models_CVPR_2026_paper.html)列出的第三位作者为 Zijun Xiong。Zotero 与本页属性采用官方作者信息，原页图保留不改。

## PPT 文献分享原页

来源：[第 2 组原 PPT](file:///C:/Users/amber/Documents/xwechat_files/wxid_ojd0ni9ss2gz12_0e91/msg/file/2026-09/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 54–64 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 54 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-054.png]]

> [!quote]- 本页可搜索文字
> AGFT：用于视觉语言模型零样本对抗鲁棒性的
>
> 对齐引导微调
>
> 会议
>
> 作者
>
> 机构
>
> 汇报人
>
> 日期
>
> CVPR 2026
>
> Yubo Cui, Xianchao Guan, Zihao Wang, Zheng Zhang
>
> Harbin Institute of Technology, Shenzhen; 
>
> Shenzhen Loop Area Institute
>
> 2612190 王滢
>
> 2026 年 9 月 30 日
>
> AGFT: Alignment-Guided Fine-Tuning for Zero-Shot Adversarial Robustness of  
>
> Vision-Language Models
>

### 原 PPT 第 55 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-055.png]]

> [!quote]- 本页可搜索文字
> 强大的零样本泛化能力
>
> 零样本对抗鲁棒性（ZSAR）挑战
>
> 以CLIP为代表的预训练视觉语言模型（VLMs）通过大规模的图文对学习，构建了共享嵌入空间，从而实现视觉特征与文本语义的对齐，在多种下游任务中表现出强大的零样本泛化能力，已成为多模态理解的基础模型。
>
> 研究背景及问题
>
> 视觉语言模型的零样本对抗鲁棒性（ZSAR）
>
> 提升VLM对抗鲁棒性的必要性：与传统深度神经网络类似，VLM易受对抗样本攻击。微小且不易察觉的扰动即可导致模型预测完全错误，在实际应用中引发严重的可靠性危机。
>
> VLM具备强大的零样本泛化能力但易受对抗样本攻击，ZSAR成为可信多模态系统的关键挑战
>
> 更具挑战性的零样本对抗鲁棒性（ZSAR）：零样本场景下的对抗鲁棒性要求模型不仅要抵抗对抗扰动，还要保留预训练阶段学到的跨模态对齐能力，从而支撑超越监督类别的泛化。
>
> Learning Transferable Visual Models From Natural Language Supervision
>
> CLIP的对比预训练与零样本预测流程。通过图文对比学习对齐视觉与文本嵌入，无需下游标注即可实现零样本分类
>
> 尽管CLIP在零样本图像识别任务中表现优异，但当输入对抗性的图像时，其性能仍存在脆弱性。
>
> Understanding zero-shot adversarial robust-ness for large-scale models.
>
> 55
>

### 原 PPT 第 56 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-056.png]]

> [!quote]- 本页可搜索文字
> 研究背景及问题
>
> 硬标签监督只关注单目标类匹配，忽略了图像与所有文本概念的相似性关系
>
> 改变了预训练学到的跨模态相似性对应关系，直接导致零样本泛化性能下降
>
> 两大核心痛点
>
> ZSAR的核心挑战：鲁棒性与跨模态对齐的冲突
>
> 痛点一：破坏预训练跨模态对齐
>
> 痛点二：预测分布不匹配
>
> 对抗微调导致鲁棒模型的预测分布与原始预训练分布不一致
>
> 扰乱固有的跨模态语义关系，加剧零样本泛化能力退化
>
> 研究主流方案
>
> 现有主流的分类引导方法：用硬标签监督，只关注目标类，易破坏预训练的跨模态对齐结构
>
> 理想的对齐引导方法：利用原始模型的概率预测作为软监督，保留跨模态语义结构，提升ZSAR
>
> 对抗微调方法对比
>
> 当前提升ZSAR方法大多采用标签监督的对抗微调范式（如TeCoA、PMG-AFT等）
>
> 将预训练VLM视为传统分类器，使用硬标签监督微调CLIP图像编码器
>
> 让对抗视觉特征向目标类别靠拢、抑制其他类别
>
> 对抗微调前后CLIP模型对不同候选文本的预测结果，微调后目标类别panda的得分由0.60提升至0.98，其余类别得分均显著下降。
>
> 56
>

### 原 PPT 第 57 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-057.png]]

> [!quote]- 本页可搜索文字
> 57
>
> 解决方案
>
> 预备知识：CLIP与对抗攻击
>
> CLIP 基本结构
>
> Learning Transferable Visual Models From Natural Language Supervision
>
> CLIP是一种基础的视觉语言编码器，由两个编码器组成: 
>
> 图像编码器
>
> 文本编码器
>
> 给定图像和文本CLIP通过计算余弦相似度
>
>                     完成零样本分类。其核心思想是：
>
> 语义相关的图文在共享嵌入空间中彼此靠近。
>
> CLIP预训练损失（InfoNCE）
>
>  为温度参数，总损失为
>
>                                                          ，该损失拉近匹配图文、推远不匹配图文，是CLIP零样本泛化能力的来源。
>
> 对抗攻击
>
> 对抗攻击通过向输入图像添加难以察觉的微小扰动误导模型。扰动通常约束在     范数球内。
>
> Mitigation of Adversarial Examples in RF Deep Classifiers Utilizing AutoEncoder Pre-training
>
> 对抗攻击示例。对“熊猫”图像施加微小扰动（ε=0.007），模型即以99.3%置信度误判为“长臂猿”，而扰动本身人眼几乎不可察觉。
>

### 原 PPT 第 58 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-058.png]]

> [!quote]- 本页可搜索文字
>              表示正样本对，否则为0
>
> 58
>
> 解决方案
>
> 预备知识：ZSAR与传统对抗微调
>
> 零样本对抗鲁棒性（ZSAR）
>
> 传统对抗微调（TeCoA）
>
> 零样本对抗鲁棒性（ZSAR）对抗训练 是提升模型鲁棒性最有效的方法，通常被建模为min-max优化问题
>
> 即生成对抗样本以最大化训练损失，同时优化模型参数以提升鲁棒性。与传统对抗鲁棒性不同，ZSAR要求模型的鲁棒性迁移到训练分布之外的未见目标任务，而无需访问目标数据。论文主要考虑白盒威胁模型，例如PGD
>
> ：扰动预算
>
> ：步长
>
>  ：扰动球
>
> 符号说明
>
> 投影梯度下降（PGD）是白盒设定下最强大的攻击模型之一，它沿梯度方向迭代更新输入以最大化损失，再将扰动样本投影回可行扰动集：
>
> 对抗微调已被用于提升VLM的ZSAR。TeCoA在ImageNet上使用类别标签构造文本提示，微调CLIP图像编码器，训练目标基于交叉熵优化：
>
>  为对抗样本，
>
>   为文本输入，
>
> 为真实图文对应关系 
>
> 为继承自预训练的固定超参数
>
> 传统对抗微调中使用的硬标签监督只关注目标类，将对抗视觉特征推向单一目标文本，却忽视了图像与其他文本概念之间的相对相似性关系，导致跨模态对齐被破坏。这正是AGFT要解决的核心问题。
>

### 原 PPT 第 59 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-059.png]]

> [!quote]- 本页可搜索文字
> 59
>
> 解决方案
>
> AGFT：对齐引导的微调框架
>
> AGFT 整体流程图
>
> 核心目标是在提升对抗鲁棒性的同时，保留预训练模型的跨模态语义对齐结构
>
> 避免传统分类引导方法对零样本泛化能力的破坏
>
> 预训练模型
>
>  温度缩放（γ）
>
> 软预测分布
>
> 校准后分布
>
>    软监督对抗训练
>
> 整体流程
>
> 输入图像和文本
>
> 在min-max框架下
>
> 进行对抗训练
>
> 通过温度缩放γ校准得到
>
> 目标分布 ​
>
> 用预训练模型的软概率
>
> 分布替代硬标签
>
> 核心
>
> 思路
>

### 原 PPT 第 60 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-060.png]]

> [!quote]- 本页可搜索文字
> 60
>
> 解决方案
>
> 两大核心组件：文本引导的对抗训练和分布一致性校准
>
> 文本引导的对抗训练
>
> 分布一致性校准
>
> 校准的目标是保持图像与多个文本之间的相对语义关系一致，但允许置信度尺度灵活调整
>
> 温度缩放校准：引入缩放温度          ，降低过度自信的预测，使目标分布匹配鲁棒特征空间
>
> 用预训练 CLIP 的概率预测作为软监督，
>
> 替代硬标签，保留跨模态相似性
>
> 最终目标函数
>
> 虽然文本引导的对抗训练已优于硬标签监督，但直接匹配仍非最优。同时包含相似性结构（各类别的排名和相对比例）和置信度尺度（绝对数值大小）两个因素。前者期望被保留，后者却可能不适配鲁棒特征空间，强行匹配易导致过拟合，进而扭曲特征空间，反而干扰跨模态对齐的保留。
>
> * 未经过对抗攻击的预训练模型对图文相似度的概率预测
>
> * 鲁棒模型（rob）输出的相对语义关系（即各个类别的排名与相对比例）要与原始模型（orig）保持一致
>

### 原 PPT 第 61 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-061.png]]

> [!quote]- 本页可搜索文字
> 从对齐引导而非分类引导的视角重新审视ZSAR问题，指出跨模态对齐的保留是零样本泛化的关键
>
> 核心创新点
>
> 第一步：软分布替代硬标签
>
> 用预训练模型的概率预测作为监督信号，保留图像与所有文本概念的细粒度相似性关系
>
> 第二步：温度缩放校准
>
> 引入温度缩放比例γ，得到，解耦“相似性结构”与“置信度尺度”，使目标分布匹配鲁棒特征空间。
>
> 方法创新
>
> 用校准后的软分布替代硬标签
>
> 作为对抗微调的监督信号
>
>              硬标签                   校准后的软分布
>
> 与现有方法的区别
>
> 方法
>
> 监督信号
>
> 跨模态对齐
>
> 零样本泛化
>
> TeCoA
>
> 硬标签
>
> 破坏
>
> 下降
>
> PMG-AFT
>
> 硬标签+辅助分支
>
> 破坏
>
> 下降但缓解
>
> TGA-ZSR
>
> 硬标签+注意力约束
>
> 破坏
>
> 下降但缓解
>
> GLADIATOR
>
> 硬标签+特征调制
>
> 破坏
>
> 下降但缓解
>
> AGFT（本文）
>
> 校准软分布 prob​
>
> 保留
>
> 保持甚至提升
>
> 61
>

### 原 PPT 第 62 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-062.png]]

> [!quote]- 本页可搜索文字
> 实验逻辑
>
> 实验论证：主实验 + 强化实验 + 机制验证 + 效率验证
>
> 机制验证
>
> 在不同扰动预算、更强白盒攻击、多样未见攻击（15种攻击设置）、跨架构、OOD场景下与四个代表性基线方法对比干净准确率和鲁棒准确率。
>
> 结论是AGFT 的鲁棒性泛化能力在多种条件下均成立。
>
> 强化实验
>
> 62
>
> 在ImageNet上对抗微调，与四个代表性基线方法在15个零样本数据集上对比干净准确率和鲁棒准确率
>
> AGFT鲁棒准确率超越最强基线3.1%，干净准确率超越1.0%，相比TeCoA分别提升8.1%和4.4%。证明AGFT 能够兼顾鲁棒性与泛化性。
>
> 主实验
>
> 与TeCoA、PMG-AFT、TGA-ZSR对比前向/反向传播次数和训练时间。
>
> AGFT仅需1次额外前向传播，训练时间远低于 PMG-AFT 和 TGA-ZSR，AGFT以较低的计算代价取得显著性能提升，具备实际部署的可行性。
>
> 效率验证
>
> 超参数消融（验证 γ 和 1/τ 共同控制鲁棒性与泛化性的权衡，发现存在最优平衡点）
>
> 分布校准实证（对比各方法的置信度和相似度，验证温度缩放是否真的改善分布匹配）
>
> 语义结构保留（用 Top-5 IoU 定量对比、t-SNE 定性可视化验证 AGFT 真的保留了跨模态语义结构）
>
> 代价是否可接受？
>
> 在不同条件下是否依然有效？
>
> AGFT 整体效果如何？
>
> 为什么有效？
>

### 原 PPT 第 63 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-063.png]]

> [!quote]- 本页可搜索文字
> AGFT 用预训练模型的概率预测替代基于标签的监督，在提升ZSAR性能的同时保留跨模态对齐信息，解决了传统对抗微调破坏图文对齐、导致零样本泛化能力下降的问题。
>
> 结论与启发
>
> AGFT 框架为 VLM 微调提供了一种新的有效方法。
>
> 分析了对抗微调破坏跨模态对齐的原因，为方法设计提供了理论依据。
>
> 计算效率高，具备实际应用价值，可扩展至更广泛的 VLM 下游任务。
>
> 对视觉语言模型的贡献
>
> 方法设计的启示
>
> 未来工作方向
>
> 软分布替代硬标签的策略为多模态监督信号设计提供了新思路，可推广到其他需要保留结构信息的任务。
>
> 扩展威胁模型：从 ℓ∞ 扩展到 ℓ₂、文本级攻击、联合文本-图像攻击
>
> 扩展模型架构：从CLIP扩展到其他跨模态模型和Transformer架构
>
> 扩展下游任务：从零样本分类扩展到视觉问答、图像描述等。
>
> 63
>

### 原 PPT 第 64 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-064.png]]

> [!quote]- 本页可搜索文字
> 感谢观看与聆听！
>
> THANKS
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]
