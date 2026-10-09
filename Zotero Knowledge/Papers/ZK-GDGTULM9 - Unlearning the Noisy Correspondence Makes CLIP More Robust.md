---
type: "literature"
title: "Unlearning the Noisy Correspondence Makes CLIP More Robust"
aliases: ["NCU"]
zotero_keys: ["GDGTULM9"]
year: 2025
authors: ["Han, Haochen", "Wang, Alex Jinpeng", "Ye, Peijun", "Liu, Fangming"]
venue: "ICCV 2025"
doi: ""
url: "https://arxiv.org/abs/2507.03434"
collections: ["06 Alignment & Reliability/Robustness & OOD", "90 Projects/Pattern Recognition Course/Project 1/Group 2", "02 Representation & Perception/Vision-Language Representation"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2", "concept/微调策略与泛化鲁棒性", "concept/跨模态对齐与模态间隙", "concept-primary/微调策略与泛化鲁棒性"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [79, 92]
imported_at: "2026-10-03"
---

# Unlearning the Noisy Correspondence Makes CLIP More Robust

[在 Zotero 打开](zotero://select/library/items/GDGTULM9) · [论文来源](https://arxiv.org/abs/2507.03434) · [论文 PDF](https://arxiv.org/pdf/2507.03434)

## 文献导读

对预训练 CLIP 中的错误图文对应关系进行遗忘，通过最难负语义提供遗忘方向，并用最优传输构造统一目标。分别检查错误正样本与错误负样本的处理。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Robustness & OOD/索引|06 Alignment & Reliability/Robustness & OOD]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-CDHTS2WR - Learning Transferable Visual Models From Natural Language Supervision|CLIP]]
- [[Zotero Knowledge/Papers/ZK-2IQ6RLSK - Sigmoid Loss for Language Image Pre-Training|SigLIP]]
- [[Zotero Knowledge/Papers/ZK-TGBY7QJ9 - AGFT  Alignment-Guided Fine-Tuning for Zero-Shot Adversarial Robustness of Vision-Lan|AGFT]]

## 原始摘要

The data appetite for Vision-Language Models (VLMs) has continuously scaled up from the early millions to billions today, which faces an untenable trade-off with data quality and inevitably introduces Noisy Correspondence (NC) samples. Undoubtedly, such semantically unrelated data significantly impairs the performance of VLMs. Previous efforts mainly address this challenge by estimating refined alignment for more precise guidance. However, such resource-intensive pipelines that train VLMs from scratch struggle to meet realistic data demands. In this paper, we present a brand new perspective that seeks to directly eliminate the harmful effects of NC in pre-trained VLMs. Specifically, we propose NCU, a Noisy Correspondence Unlearning fine-tuning framework that efficiently enhances VLMs' robustness by forgetting learned noisy knowledge. The key to NCU is learning the hardest negative information, which can provide explicit unlearning direction for both false positives and false negatives. Such twin goals unlearning process can be formalized into one unified optimal transport objective for fast fine-tuning. We validate our approach with the prevailing CLIP model over various downstream tasks. Remarkably, NCU surpasses the robust pre-trained method on zero-shot transfer while with lower computational overhead. The code will be released upon acceptance.

来源：[论文官方页面](https://arxiv.org/abs/2507.03434)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 79–92 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 79 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-079.png]]

> [!quote]- 本页可搜索文字
> Unlearning the Noisy Correspondence 
>
> Makes CLIP More Robust
>
> 作者
>
> 作者: Haochen Han, Alex Jinpeng Wang, Peijun Ye, Fangming Liu，
>
> Peng Cheng Laboratory Central South University
>
> 汇报人
>
> 汇报人:  2612155 王语凡
>
> 专业: 软件工程
>
> 通过遗忘噪声图文对应关系提升 CLIP 鲁棒性
>

### 原 PPT 第 80 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-080.png]]

> [!quote]- 本页可搜索文字
> ROADMAP
>
> 汇报目录
>
> 01
>
> 研究背景与动机
>
> CLIP为什么会受到噪声影响
>
> 02
>
> NCU 方法与关键机制
>
> 如何同时遗忘FP和FN
>
> 03
>
> 实验验证与结论
>
> 性能、组件和效率是否得到验证
>

### 原 PPT 第 81 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-081.png]]

> [!quote]- 本页可搜索文字
> 01 · BACKGROUND
>
> CLIP 的能力来自大规模图文对，但规模也带来噪声
>
> CLIP基本训练方式
>
> CLIP包含两个编码器
>
> 图像编码器
>
> 文本编码器
>
> 对于一个图像和文本对:
>
> CLIP目标：
>
> 让正确匹配的图像和文本相似
>
> 让batch中其他不匹配的图像和文本不相似
>
> 缺陷：
>
> 如果训练图文对本身错误，CLIP 会把错误关系学进视觉表示空间
>
> 噪声来源
>
> 来源：
>
> 视觉语言模型经常使用网页爬取的图像和文本
>
> 数据规模很大，很难保证每一对图文都准确匹配
>
> 问题：
>
> 图文对本身就是错误的
>
> batch中存在语义相近但没有配对的样本
>
> 错误监督会被模型记住
>
> CLIP存在训练监督关系问题
>

### 原 PPT 第 82 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-082.png]]

> [!quote]- 本页可搜索文字
> 01 · BACKGROUND
>
> 传统方法的不足
>
> 梯度上升：
>
> 通过最大化错误样本上的损失，让模型忘掉这些样本
>
> 没有告诉模型朝哪个方向修改，模型可能学到无意义的替代方式
>
> 问题：
>
> 遗忘方向不明确；
>
> 可能破坏原有语义结构；
>
> 可能把有用信息一起遗忘
>
> 模型需要“有方向的遗忘”
>
> 直接梯度上升
>
> 从头进行鲁棒性训练
>
> 已有方法：预训练阶段处理噪声
>
> 从头训练
>
> 重新读取大规模数据
>
> 计算资源使用量大
>
> 依赖完整的训练数据
>
> 存在问题：
>
> 原训练数据已经无法完整访问
>
> 一部分数据属于私有数据
>
> 重新训练成本过高
>
> 模型已训练完成，没必要全部推倒重来
>
> 论文需要一种“低成本且有方向的遗忘”
>

### 原 PPT 第 83 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-083.png]]

> [!quote]- 本页可搜索文字
> 01 · BACKGROUND
>
> 两类噪声
>
> 两类Noisy Correspondence
>
> False Positive：
>
> 本来不匹配的图文，被错误地当成了正样本
>
> 图配了 （错误文本）,应该匹配
>
> False Negative：
>
> 本来语义相关的图文，被训练过程错误地当成了负样本
>
> （图）配了 （漏掉关键信息的文本）,真正应该匹配
>
> NCU：
>
> 学习最难负样本
>
> FP：作为上界，把错误正样本 从图像旁边推开
>
> FN：作为下界，把本应相关却被漏掉的  拉近，从而建模 "一对多" 的关系（一张图可以有多个正确文本描述）
>
> 本文要直接消除它们
>
> FP是错误拉近，FN是错误推远
>

### 原 PPT 第 84 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-084.png]]

> [!quote]- 本页可搜索文字
> 数据集定义：
>
> Forget Set:,表示可能是FP的图文对
>
> Retain Set:，表示相对可信的图文对
>
> 满足条件
>
> 双向匹配置信度：
>
> NCU使用预训练CLIP当前的表示能力计算匹配置信度
>
> 图像到文本方向为：
>
> 文本到图像方向为：
>
> 双向置信度越低，越可能存在错误图文对应
>
> 样本划分：
>
> 每个batch中，最低的P%图文对划入
>
> 表示剩余样本
>
> 最难负样本生成：
>
> 原始文本,NCU在其文本token前加入m个可学习的共享prompt向量，作为文本前缀
>
> 例如“the image has no…”“this picture lacks…”
>
> 02 · METHOD
>
> 样本划分
>
> 与原样本适度分离：
>
> 原样本与其他负样本关系保持一致：
>
> 负样本可以对其他图像提供监督：
>
> 总损失
>
> 样本划分
>
> 最大负样本损失定义
>

### 原 PPT 第 85 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-085.png]]

> [!quote]- 本页可搜索文字
> 最大化L2距离：
>
> 直接将推到原文本最远的地方
>
> 无法为未配对图像提供有意义的监督
>
> Similarity Bound：
>
> 限制
>
> 允许的位置区域较大
>
> 多个完全不同的负文本位置均满足约束
>
> Relation Opposite：
>
> 利用batch中的关系结构限制负样本的位置
>
> 与原样本分离、不脱离语义空间、与其他样本保持合理关系
>
> 02 · METHOD
>
> 最难负样本划分
>
> 最难负样本样本划分
>

### 原 PPT 第 86 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-086.png]]

> [!quote]- 本页可搜索文字
> NCU完整流程
>
> 输入图像和文本：
>
> 输入一个batch:
>
> 图像输入视觉编码器，文本输入文本编码器（均为冻结的预训练CLIP）
>
> 生成负样本：
>
> 对原始文本加入可学习prompt，生
>
> 每个图像不只对应原始文本，还多了一个负文本候选
>
> 扩展成本矩阵：
>
> 图文余弦距离，越相近，对齐代价越小
>
> NCU增加了一个负文本列：专门留给最难负样本
>
> 掩码矩阵：
>
> FP错误行，对角线设为0，最难负样本列设为1
>
> 其他行，最难负样本列设为0
>
> OT Plan：
>
> 求解的分配矩阵，每个格子表示从图像流向文本的概率大小
>
> 灰色越深，表示匹配的质量越大
>
> 02 · METHOD
>
> 模型基本框架
>
> Aligning对齐：
>
> 评判最优传输后和调整前的图文分布应该长什么样
>
> 微调目标：
>
> 使用KL散度微调，让模型预测接近软目标
>
> 特征空间：
>
> （图1）、（错配的文本）、（另一个文本）、（另一张图）、（最难负文本）。
>
> Unlearn FP：把  从错误的 旁边拉开，方向指向 。
>
> Unlearn FN：把本该和  相关、却离得远的  这一对互相拉近。
>

### 原 PPT 第 87 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-087.png]]

> [!quote]- 本页可搜索文字
> 构造OT：
>
> ：图像与候选文本之间的代价矩阵；
>
> ：要优化的传输／匹配分布；
>
> ：熵正则项，让分配不必是僵硬的一对一结果；
>
> ：满足行列边缘约束的可行分布集合。
>
> 在 Mask 允许的关系中，Sinkhorn 求出代价较低、同时满足边缘约束的软匹配分布。
>
> 02 · METHOD
>
> Optimal Transport最优传输
>
> 解决问题：
>
> OT结果通过对齐得到微调目标：
>
> 是融合后的软匹配目标， 是模型当前CLIP预测的匹配分布；
>
> 用 KL 散度让模型当前的图文匹配分布接近 OT 给出的软目标：
>

### 原 PPT 第 88 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-088.png]]

> [!quote]- 本页可搜索文字
> 03 · EXPERIMENT
>
> 主要实验结果
>
> 零样本迁移
>
> 验证内容与结果：
>
> 论文比较原始 CLIP 和经过 NCU 微调后的 CLIP，观察 NCU 能否消除 noisy correspondence 对模型的影响。
>
> 在多个数据集和模型结构上，NCU 的 zero-shot 分类结果整体优于原始 CLIP，相比原始CLIP提升4.0%
>
> CC3M + ViT-B/16：16.0 → 20.0；
>
> CC12M + ViT-B/16：40.6 → 43.4；
>
> YFCC15M-R + ViT-B/32：17.8 → 21.9
>
> 跨任务迁移能力
>
> 验证内容与结果：
>
> 论文进一步使用图文检索任务来验证 NCU 是否真正改善了跨模态对齐能力。
>
> NCU 在绝大多数图文检索指标上都优于原始 CLIP。
>
> Flickr30K：43.1 → 50.1；
>
> MSCOCO：26.1 → 30.5。
>

### 原 PPT 第 89 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-089.png]]

> [!quote]- 本页可搜索文字
> 03 · EXPERIMENT
>
> 主要实验结果
>
> 视觉特征迁移能力
>
> 验证内容与结果：
>
> 论文使用线性探测方法验证图像编码器提取的视觉特征是否更适合下游任务。
>
> 冻结视觉编码器后，NCU 的视觉特征仍然更容易被线性分类器利用。
>
> NCU 不仅改善了图文对齐，也改善了图像编码器本身的视觉表示，使其更容易迁移到下游分类任务。
>
> 与已有鲁棒方法比较
>
> 验证内容：
>
> NCU 相比简单遗忘方法和已有鲁棒预训练方法，是否具有优势？
>
> 原始 CLIP；
>
> Gradient Ascent：直接在疑似噪声样本上进行梯度上升，遗忘方向模糊
>
> SoftCLIP：通过更柔性的对齐方式从头训练模型，计算成本高
>
> NCU
>
> 结果：
>
> NCU 的优势来自“有方向的联合遗忘”，而不是简单地对噪声样本进行梯度上升或重新训练一个更鲁棒的模型。
>

### 原 PPT 第 90 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-090.png]]

> [!quote]- 本页可搜索文字
> 03 · EXPERIMENT
>
> 主要实验结果
>
> 消融实验
>
> 验证内容：
>
> 论文通过消融实验验证 NCU 的关键组成部分是否有效
>
> Hardest Negative Prompt；
>
> Text Relation Opposite；
>
> False Positive Unlearning；
>
> False Negative Unlearning。
>
> 结果：
>
> NCU 的性能提升不是由某一个单独组件造成的，而是由 hardest negative、relation opposite 以及 FP/FN 联合遗忘共同产生的。
>
> 数据效率
>
> 验证内容：
>
> 论文研究在只使用部分数据进行 unlearning 的情况下，NCU 是否仍然有效
>
> 使用不同数量的图文数据进行遗忘
>
> 结果：
>
> 只使用约 0.5M 数据，即低于 CC3M 的 20%，仍然可以获得明显收益。
>
> NCU 不需要完整访问原始预训练数据，也可以通过部分数据实现有效的噪声遗忘。
>

### 原 PPT 第 91 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-091.png]]

> [!quote]- 本页可搜索文字
> 03 · EXPERIMENT
>
> 主要实验结果
>
> 可视化
>
> 验证内容：
>
> 论文使用相似度分布可视化比较：
>
> 原始 CLIP；
>
> NCU。
>
> 主要观察：
>
> 正样本对的相似度分数
>
> 负样本对的平均相似度分数
>
> 负样本对中最高相似度分数排名前 5% 的分布情况
>
> 结果：
>
> NCU 生成的正样本相似度分数分布范围更广，能够捕捉正样本对之间更细粒度的匹配程度
>
> NCU 增强了特征区分能力，从而使得正样本对与负样本对之间呈现出更显著的分离度能够表达更细粒度的图文匹配程度；
>
> NCU 为困难负样本提供了更适宜的度量标准，既能与正样本对保持区分，也能与其他负样本对保持区分
>

### 原 PPT 第 92 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-092.png]]

> [!quote]- 本页可搜索文字
> 04 · CONCLUSION
>
> 结论
>
> 局限与展望
>
> • 目前主要验证 CLIP
>
> • 数据规模仍是百万级
>
> • 需扩展到 BLIP-2、LVLM 等更大模型
>
> NCU 用最难负语义提供明确遗忘方向，
>
> 在保留 CLIP 能力的同时削弱 FP/FN 噪声关系。
>
> • 首次将 noisy correspondence unlearning 引入预训练 CLIP
>
> • 一个最优传输目标统一处理 FP 与 FN
>
> • 低成本、部分数据即可提升下游鲁棒性
>
> 结论
>
> 贡献
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-CDHTS2WR - Learning Transferable Visual Models From Natural Language Supervision|Learning Transferable Visual Models From Natural Language Supervision]] — 强关联；本篇摘要提到模型 CLIP（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-2IQ6RLSK - Sigmoid Loss for Language Image Pre-Training|Sigmoid Loss for Language Image Pre-Training]] — 中关联；共同研究内容：对比学习与跨模态编码。
- [[Zotero Knowledge/Papers/ZK-88IZNLUX - Understanding Contrastive Representation Learning through Alignment and Uniformity on|Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere]] — 中关联；共同研究内容：对比学习与跨模态编码。

<!-- content-relations:end -->

<!-- research-integration:start -->
## 研究主题入口

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Robustness & OOD/索引|06 Alignment & Reliability/Robustness & OOD]]
- [[Zotero Knowledge/Topics/02 Representation & Perception/Vision-Language Representation/索引|02 Representation & Perception/Vision-Language Representation]]

## 概念比较入口

- [[Zotero Knowledge/Concepts/微调策略与泛化鲁棒性|微调策略与泛化鲁棒性]]
- [[Zotero Knowledge/Concepts/跨模态对齐与模态间隙|跨模态对齐与模态间隙]]
<!-- research-integration:end -->
