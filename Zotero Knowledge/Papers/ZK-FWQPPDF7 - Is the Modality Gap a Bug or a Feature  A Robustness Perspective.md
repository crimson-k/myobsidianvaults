---
type: "literature"
title: "Is the Modality Gap a Bug or a Feature? A Robustness Perspective"
aliases: ["Modality Gap Robustness"]
zotero_keys: ["FWQPPDF7"]
year: 2026
authors: ["Chowers, Rhea", "Naparstek, Oshri", "Barzelay, Udi", "Weiss, Yair"]
venue: "CVPR 2026"
doi: ""
url: "https://arxiv.org/abs/2603.29080"
collections: ["06 Alignment & Reliability/Robustness & OOD", "90 Projects/Pattern Recognition Course/Project 1/Group 2", "06 Alignment & Reliability/Representation Alignment", "02 Representation & Perception/Vision-Language Representation"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2", "concept/跨模态对齐与模态间隙", "concept/微调策略与泛化鲁棒性", "concept-primary/跨模态对齐与模态间隙"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [109, 120]
imported_at: "2026-10-03"
---

# Is the Modality Gap a Bug or a Feature? A Robustness Perspective

[在 Zotero 打开](zotero://select/library/items/FWQPPDF7) · [论文来源](https://arxiv.org/abs/2603.29080) · [论文 PDF](https://arxiv.org/pdf/2603.29080)

## 文献导读

研究模态间隙与嵌入扰动下稳定性的关系，通过有条件的正交平移减少间隙。理论的欧氏排序保证与重新归一化、真实输入扰动需要分别检查。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Robustness & OOD/索引|06 Alignment & Reliability/Robustness & OOD]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-BYZ75H5L - Connect, Collapse, Corrupt  Learning Cross-Modal Tasks with Uni-Modal Data|C3]]
- [[Zotero Knowledge/Papers/ZK-TGBY7QJ9 - AGFT  Alignment-Guided Fine-Tuning for Zero-Shot Adversarial Robustness of Vision-Lan|AGFT]]
- [[Zotero Knowledge/Papers/ZK-28MFNY9F - CLIP is Strong Enough to Fight Back  Test-time Counterattacks towards Zero-shot Adver|TTC]]

## 原始摘要

Many modern multi-modal models (e.g. CLIP) seek an embedding space in which the two modalities are aligned. Somewhat surprisingly, almost all existing models show a strong modality gap: the distribution of images is well-separated from the distribution of texts in the shared embedding space. Despite a series of recent papers on this topic, it is still not clear why this gap exists nor whether closing the gap in post-processing will lead to better performance on downstream tasks. In this paper we show that under certain conditions, minimizing the contrastive loss yields a representation in which the two modalities are separated by a global gap vector that is orthogonal to their embeddings. We also show that under these conditions the modality gap is monotonically related to robustness: decreasing the gap does not change the clean accuracy of the models but makes it less likely that a model will change its output when the embeddings are perturbed. Our experiments show that for many real-world VLMs we can significantly increase robustness by a simple post-processing step that moves one modality towards the mean of the other modality, without any loss of clean accuracy.

来源：[论文官方页面](https://arxiv.org/abs/2603.29080)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 109–120 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 109 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-109.png]]

> [!quote]- 本页可搜索文字
> 模态间隙：缺陷，还是特性？
>
> 01 / 12
>
> 来源：论文标题、摘要、图1b
>
> Is the Modality Gap a Bug or a Feature?
>
> A Robustness Perspective
>
> Rhea Chowers 等 · CVPR 2026
>
> 同一张图片，文字换个说法，为什么模型可能改口？
>
> 汇报人：王郅杰 · 2631762
>
> 电子与信息工程学院
>

### 原 PPT 第 110 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-110.png]]

> [!quote]- 本页可搜索文字
> 先看模型怎样判断一张图片
>
> 02 / 12
>
> 来源：论文§1、§3.1；图片取自图1b
>
> 候选描述：“狗的照片”“青蛙的照片”
>
> 1  图片和文字，各自变成一串数字
>
> 这串数字叫“向量”，也称“嵌入”
>
> 可以把它想成空间里一个点的坐标
>
> 2  放在同一个空间里比较
>
> 图片是一个点，每句候选文字也是一个点
>
> 在这里，用点之间的距离表示匹配程度
>
> 3  选择离图片最近的文字
>
> 这叫“最近邻匹配”
>
> 我们要研究：稍有变化，选择会不会改变？
>

### 原 PPT 第 111 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-111.png]]

> [!quote]- 本页可搜索文字
> 研究动机：能匹配，为什么还要关心间隙？
>
> 03 / 12
>
> 来源：论文图1a、图2、§1
>
> 什么叫模态间隙？
>
> 模态就是数据形式，这里指图片和文字
>
> 间隙是两团点的平均位置之差
>
> 配对成功，只需要“比其他候选更近”
>
> 正确文字不必和图片点完全重合
>
> 所以：匹配正确，仍可以有间隙
>
> 本文关心：模型是否容易改口？
>
> 小变化后仍能稳定判断，称为“鲁棒性”
>
> 目标：让模型更稳，同时保留原来的判断
>
> 已有结果：拉近两团点，对不同任务的准确率影响不一致。
>

### 原 PPT 第 112 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-112.png]]

> [!quote]- 本页可搜索文字
> 为什么训练好了，两团点仍没有重合？
>
> 04 / 12
>
> 来源：论文图3、式2、§3.2
>
> 训练鼓励正确配对领先其他候选
>
> 原文式（2）：正确配对的相对分数
>
> xᵢ：文字点；yᵢ：配对的图片点；Y：候选图片
>
> 分子：正确配对的分数
>
> 分母：所有候选分数的总和
>
> τ：控制分数是否更集中在最近的候选上
>
> 正确配对明显领先，训练目标就能较好满足；图片点与文字点仍可能相隔一段距离。
>

### 原 PPT 第 113 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-113.png]]

> [!quote]- 本页可搜索文字
> 解决思路：模型不重训，只调整文字点的位置
>
> 05 / 12
>
> 来源：论文§3–4、定理3.4–3.5
>
> 模型保持原样
>
> 直接使用已经训练好的编码器，得到图片点和文字点。
>
> 需要调整的是输出的数字坐标。
>
> 文字点一起移动
>
> 每个文字点都沿相同方向、移动相同距离。
>
> 图片点保持原位，再比较它与文字点之间的距离。
>
> 方向必须先选好
>
> 希望受到小干扰后更稳定，同时保留没有干扰时的原答案。
>
> 因此，方法的关键是找到满足这一要求的移动方向。
>

### 原 PPT 第 114 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-114.png]]

> [!quote]- 本页可搜索文字
> 为什么间隙大，模型可能更容易改口？
>
> 06 / 12
>
> 来源：论文图7、式10、定理3.4、附录A
>
> 文字一动，分界线也会动
>
> 线的两侧，模型选择不同文字
>
> 边界稍一转动，离文字更远的
>
> 图片点可能被划到另一边
>
> 本文的稳定性：加了干扰后，仍选原来答案的比例
>
> 原来答错、后来仍答错，也算“没改口”。因此，还必须一起看准确率。
>
> 上述关系有几何与噪声条件，不能直接推广到任意输入变化。
>

### 原 PPT 第 115 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-115.png]]

> [!quote]- 本页可搜索文字
> 怎样移动，才能保住原来的答案？
>
> 07 / 12
>
> 来源：论文定理3.5、附录A.5、式45；表中数值为教学示例
>
> “正交”就是垂直
>
> 把文字点想成同一桌面上的点，沿垂直方向一起移动。
>
> 所有候选的平方距离改变相同的量，远近顺序就不变。
>
> 教学示例
>
> 到“狗”的平方距离
>
> 到“猫”的平方距离
>
> 移动前
>
> 9
>
> 13
>
> 整体上移后
>
> 1
>
> 5
>
> 原文式（45）：y 是图片点，xᵢ、xⱼ 是文字点，v 是正交方向，α 控制移动多少。
>
> 两项都减 8，“狗”仍然最近。这里保证的是按欧氏距离选出的原答案。
>

### 原 PPT 第 116 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-116.png]]

> [!quote]- 本页可搜索文字
> 具体怎么做：找中心、选方向、一起移动
>
> 08 / 12
>
> 来源：论文§4、式4与11、附录G
>
> 1  找到两团点各自的中心
>
> 坐标取平均，得到图片中心与文字中心
>
> X、Y：文字／图片集合；N、M：各自数量
>
> μ：中心；g：从文字中心指向图片中心
>
> 2  只保留垂直于文字展开方向的部分
>
> 用 PCA 找出文字点展开的方向，记为 V
>
> VVᵀg：间隙中沿文字展开方向的部分
>
> 减掉这部分，得到垂直分量 g′
>
> 3  所有文字点一起移动
>
> 给每个文字向量加上相同的 αg′
>
> α 控制移动量，0 到 1 表示逐步靠近
>
> 图片点不动，再按距离选择文字
>
> 什么时候有保证？
>
> 严格垂直时，原来的选择保持不变
>
> 近似选择方向时，需要重新检查结果
>
> 如果 g′ 为零，就没有可移动的分量
>
> 排序保证按欧氏距离比较。平移后若再改变向量长度，需要重新检查。
>

### 原 PPT 第 117 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-117.png]]

> [!quote]- 本页可搜索文字
> 创新点一：解释间隙为何影响稳定性
>
> 09 / 12
>
> 来源：论文§2、§3.2–3.3、定理3.1–3.4
>
> 要解释的问题
>
> 本文做了什么
>
> 带来的认识
>
> 为什么训练后还有间隙？
>
> 分析训练开始时点的位置
>
> 以及训练怎样移动这些点
>
> 解释间隙怎样形成
>
> 为什么能够保留下来
>
> 间隙会影响什么？
>
> 研究受到小干扰以后
>
> 模型是否改变原答案
>
> 原来能答对
>
> 不代表答案足够稳定
>
> 什么时候成立？
>
> 给出几何与噪声条件
>
> 再证明间隙与稳定性的关系
>
> 明确理论适用范围
>
> 为后面的调整方法提供依据
>
> 新增认识：除了“原来答得对不对”，还要看“小变化后是否容易改口”。
>

### 原 PPT 第 118 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-118.png]]

> [!quote]- 本页可搜索文字
> 创新点二：把理论变成不用重训的调整方法
>
> 10 / 12
>
> 来源：本文§2–4
>
> 模型照常使用，调整发生在输出向量之后
>
> 用理论选择移动方向，在正交条件下保留原来的答案。
>
> 做法
>
> 改动的位置
>
> 主要操作
>
> 再训练模型
>
> 模型内部的参数
>
> 用训练数据更新参数
>
> 使用时修正图片
>
> 输入模型的图片
>
> 为输入求一个修正扰动
>
> 本文的方法
>
> 模型输出的文字向量
>
> 先找正交方向，再整体平移
>
> 方法贡献：用理论约束移动方向，把稳定性改善与原答案保持结合起来。
>

### 原 PPT 第 119 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-119.png]]

> [!quote]- 本页可搜索文字
> 实验从哪四个方面检查这些说法？
>
> 11 / 12
>
> 来源：论文图4–6、§5.1–5.3、图8–10
>
> 验证方面
>
> 怎么检查
>
> 要回答的问题
>
> 间隙的形成
>
> 观察训练过程和实际模型
>
> 中图片点、文字点的位置
>
> 前面的形成解释
>
> 是否有实际依据？
>
> 人为加入小干扰
>
> 控制干扰大小，比较答案是否改变
>
> 同时检查没有干扰时的表现
>
> 是否更稳定？
>
> 原来的判断是否保留？
>
> 数字存得更粗
>
> 降低向量数值的存储精度
>
> 这叫“量化”
>
> 出现精度误差时
>
> 方法还有没有用？
>
> 文字换一种说法
>
> 改变表达，检查答对的比例
>
> 不完全满足理论条件时
>
> 是否仍有实际效果？
>
> 模型是否“没改口”和是否“答对”，是两件事，需要分别检查。
>

### 原 PPT 第 120 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-120.png]]

> [!quote]- 本页可搜索文字
> 总结：让模型不仅能匹配，也更经得起小变化
>
> 12 / 12
>
> 来源：论文§6
>
> 为什么研究？
>
> 原来答得对，不代表受到小干扰后还能稳定判断。
>
> 怎样解决？
>
> 模型不重训，先选正交方向，再把所有文字点一起移动。
>
> 新在哪里？
>
> 解释间隙与稳定性的关系，并据此设计有条件保证的调整方法。
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-CDHTS2WR - Learning Transferable Visual Models From Natural Language Supervision|Learning Transferable Visual Models From Natural Language Supervision]] — 强关联；本篇摘要提到模型 CLIP（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-BYZ75H5L - Connect, Collapse, Corrupt  Learning Cross-Modal Tasks with Uni-Modal Data|Connect, Collapse, Corrupt: Learning Cross-Modal Tasks with Uni-Modal Data]] — 强关联；共同研究内容：对比学习与跨模态编码、模态间隙。
- [[Zotero Knowledge/Papers/ZK-WFNXHCV8 - Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Languag|Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Language Models]] — 中关联；共同研究内容：对比学习与跨模态编码、模态间隙。

<!-- content-relations:end -->

<!-- research-integration:start -->
## 研究主题入口

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Robustness & OOD/索引|06 Alignment & Reliability/Robustness & OOD]]
- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]]
- [[Zotero Knowledge/Topics/02 Representation & Perception/Vision-Language Representation/索引|02 Representation & Perception/Vision-Language Representation]]

## 概念比较入口

- [[Zotero Knowledge/Concepts/跨模态对齐与模态间隙|跨模态对齐与模态间隙]]
- [[Zotero Knowledge/Concepts/微调策略与泛化鲁棒性|微调策略与泛化鲁棒性]]
<!-- research-integration:end -->
