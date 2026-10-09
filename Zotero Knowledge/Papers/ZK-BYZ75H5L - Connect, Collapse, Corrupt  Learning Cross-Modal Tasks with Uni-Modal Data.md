---
type: "literature"
title: "Connect, Collapse, Corrupt: Learning Cross-Modal Tasks with Uni-Modal Data"
aliases: ["C3"]
zotero_keys: ["BYZ75H5L"]
year: 2024
authors: ["Zhang, Yuhui", "Sui, Elaine", "Yeung-Levy, Serena"]
venue: "ICLR 2024"
doi: ""
url: "https://arxiv.org/abs/2401.08567"
collections: ["06 Alignment & Reliability/Representation Alignment", "90 Projects/Pattern Recognition Course/Project 1/Group 2"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [93, 108]
imported_at: "2026-10-03"
---

# Connect, Collapse, Corrupt: Learning Cross-Modal Tasks with Uni-Modal Data

[在 Zotero 打开](zotero://select/library/items/BYZ75H5L) · [论文来源](https://arxiv.org/abs/2401.08567) · [论文 PDF](https://arxiv.org/pdf/2401.08567)

## 文献导读

将跨模态表征失配拆为整体间隙与样本级残差，以 Connect、Collapse、Corrupt 组合校准与鲁棒训练。跨模态匹配正确并不自动意味着解码器输入可以互换。

## 主题与关联

[[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-FWQPPDF7 - Is the Modality Gap a Bug or a Feature  A Robustness Perspective|Modality Gap Robustness]]
- [[Zotero Knowledge/Papers/ZK-8MDVNFZD - Diffusion Bridge  Leveraging Diffusion Model to Reduce the Modality Gap Between Text |Diffusion Bridge]]
- [[Zotero Knowledge/Papers/ZK-I6438ULU - Diffusion-Link  Diffusion Probabilistic Model for Bridging the Audio-Text Modality Ga|Diffusion-Link]]
- [[Zotero Knowledge/Papers/ZK-WFNXHCV8 - Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Languag|ReAlign / ReVision]]

## 原始摘要

Building cross-modal applications is challenging due to limited paired multi-modal data. Recent works have shown that leveraging a pre-trained multi-modal contrastive representation space enables cross-modal tasks to be learned from uni-modal data. This is based on the assumption that contrastive optimization makes embeddings from different modalities interchangeable. However, this assumption is under-explored due to the poorly understood geometry of the multi-modal contrastive space, where a modality gap exists. In our study, we provide a theoretical explanation of this space's geometry and introduce a three-step method, $C^3$ (Connect, Collapse, Corrupt), to bridge the modality gap, enhancing the interchangeability of embeddings. Our $C^3$ method significantly improves cross-modal learning from uni-modal data, achieving state-of-the-art results on zero-shot image / audio / video captioning and text-to-image generation.

来源：[论文官方页面](https://arxiv.org/abs/2401.08567)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 93–108 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 93 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-093.png]]

> [!quote]- 本页可搜索文字
> C³
>
> CONNECT
>
> COLLAPSE
>
> CORRUPT
>
> ICLR 2024
>
> Connect, Collapse, Corrupt
>
> Learning Cross-Modal Tasks
>
> with Uni-Modal Data
>
> 用单模态数据学习跨模态任务
>
> Yuhui Zhang · Elaine Sui · Serena Yeung-Levy
>
> 2026 年 9 月
>
> Stanford University  |  ICLR 2024      汇报人：黄鸾曦  学号：2612198
>

### 原 PPT 第 94 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-094.png]]

> [!quote]- 本页可搜索文字
> Connect, Collapse, Corrupt：单模态数据如何学习跨模态任务？
>
> 01 / 14
>
> Zhang, Sui & Yeung-Levy. ICLR 2024. PDF pp.1–2；原文 Figure 2。
>
> 阅读主线：发现表征失配 → 解释几何来源 → 对应修复 → 用实验检验
>
> 01
>
> 论文问题｜能匹配，为什么还不能直接互换？
>
> Learning Cross-Modal Tasks
>
> with Uni-Modal Data
>
> Yuhui Zhang · Elaine Sui · Serena Yeung-Levy
>
> Stanford University  |  ICLR 2024
>
> 切入点
>
> 训练看文字，测试看图片
>
> 同一个解码器，能否稳定理解两种模态的输入？
>
> 关键词
>
> 可互换性 · 模态间隙 · 噪声鲁棒性
>
> 02
>
> 本文核心视角
>
> 共同偏移与样本残差
>
> 共同影响输入的可互换性。
>

### 原 PPT 第 95 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-095.png]]

> [!quote]- 本页可搜索文字
> 1 研究动机：利用单模态数据，完成跨模态生成
>
> 02 / 14
>
> §1–2，PDF pp.1–3；Algorithm 1，p.19；流程为本汇报重绘。
>
> 关键前提：训练时的文字表征，必须能被测试时的图像表征有效替换
>
> 01
>
> 问题从哪里来？
>
> 需求
>
> 图像描述需要图文对应
>
> 常规训练依赖“图片—描述”配对，收集与标注有成本。
>
> 机会
>
> 预训练空间已经连接语义
>
> CLIP / ImageBind 提供不同模态到共享空间的映射。
>
> 设想
>
> 先学会把文字表征解码
>
> 下游只用文字做重建；推理时改为图片输入。
>
> 02
>
> 训练与测试交换了哪一环？
>
> 训练
>
> 文字 → 文本编码器 → 解码器 → 原句
>
> 测试
>
> 图片 → 图像编码器 → 同一解码器 → 描述
>
> 03
>
> 下游“单模态训练”具体省掉了什么？
>
> 预训练：已有多模态数据；校准：两模态各自取样。
>
> 解码器：用文字重建训练，减少下游配对需求。
>

### 原 PPT 第 96 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-096.png]]

> [!quote]- 本页可搜索文字
> 2 现有研究痛点：相似度排名正确，仍不保证输入可互换
>
> 03 / 14
>
> §1、§2、§6、Appendix A；PDF pp.1–3、9、14。
>
> 研究缺口：不仅要知道“替换后会出错”，还要解释差异在哪里、怎样修复
>
> 01
>
> 对比学习与生成任务，要求并不相同
>
> 对比目标：让正确图文对领先错误配对
>
> 相对相似度足够高，可以使损失很小；
>
> 并不要求对应图文的向量逐点重合。
>
> 生成器接收的是一个具体向量。
>
> 换模态后，输入可能偏离训练分布。
>
> 02
>
> 已有做法
>
> 检索、改写、噪声、先验网络
>
> 操作究竟修复哪一种差异？
>
> 本文切入
>
> 先分析多模态空间的几何
>
> 从已有补救，到几何解释
>
> 前作已能完成跨模态生成，也有噪声等有效操作。
>
> 待解释
>
> 主要差在中心偏移，还是逐对残差？
>
> 先区分共同偏移与局部残差，再设计相应处理。
>

### 原 PPT 第 97 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-097.png]]

> [!quote]- 本页可搜索文字
> 3 本文发现：整体模态间隙 + 样本级对齐噪声
>
> 04 / 14
>
> §3、Table 1、Figure 2；PDF pp.2–6。统计为原文值；几何关系按近似模型解释。
>
> “图文语义相近”与“解码输入可互换”之间，还隔着整体偏移与残余误差
>
> 01
>
> 将差异分解成两个部分
>
> 固定项
>
> Modality gap：整体位置偏移
>
> 近似稳定；可通过平移整个模态点云处理。
>
> 残差项
>
> Alignment noise：逐样本误差
>
> 中心对齐后，对应点仍未必完全重合。
>
> 02
>
> Figure 2｜两种模态占据不同位置
>
> 03
>
> Table 1｜经验统计支持这一解释
>
> 偏移长度约 0.83；组间方向余弦约 0.99。
>
> 偏移与模态内部差向量余弦均值约 0。
>
> ⊥：偏移与模态内部差向量近似正交。
>

### 原 PPT 第 98 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-098.png]]

> [!quote]- 本页可搜索文字
> 3 理论解释：为什么对比优化没有自动消除这些差异？
>
> 05 / 14
>
> §3.1–3.2，Lemmas 1–2，Figures 3、5；PDF pp.4–6；条件推导见 Appendix B。
>
> 01
>
> 模态间隙｜初始化与优化方向
>
> 02
>
> 对齐噪声｜足够好的排名即可低损失
>
> Fig. 5：低损失对应一个区域，而非唯一点。
>
> 温度影响稳定区域；“近零”不等于严格为零。
>
> 初始化时，部分方向的输出变化小，图文中心不同。
>
> 条件分析：表征梯度由另一模态的差向量组合。
>
> Fig. 3：随机初始化的 CLIP；有效维数低于512。
>
> 表征层的条件解释，不等同于任意网络参数更新。
>
> 条件解释：初始化可能留下共同偏移；低对比损失仍容许逐样本残差
>

### 原 PPT 第 99 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-099.png]]

> [!quote]- 本页可搜索文字
> 06 / 14
>
> §4，PDF pp.6–7；Algorithm 1，p.19。方法概览为重绘。
>
> 01
>
> Connect
>
> 复用预训练编码器
>
> 保留已有跨模态语义联系
>
> 02
>
> Collapse
>
> 分别减去模态均值
>
> 降低整体位置差异
>
> 03
>
> Corrupt
>
> 训练表征加入随机扰动
>
> 使解码器适应邻近输入
>
> 04
>
> 改变发生在哪里？
>
> CLIP / ImageBind 编码器冻结；在表征输入侧做校准与扰动，训练下游解码器。
>
> 4 解决方案总览：三步如何改善表征的可互换性？
>
> Connect 复用语义联系；Collapse 校准中心；Corrupt 训练解码鲁棒性
>

### 原 PPT 第 100 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-100.png]]

> [!quote]- 本页可搜索文字
> 4 Collapse：分别去均值，为何能抵消整体模态偏移？
>
> 07 / 14
>
> §4 Collapse，PDF p.6；Algorithm 1，p.19。三维数值为教学示例，未归一化，非论文实测数据。
>
> 去均值只处理中心偏移；它不会自动使逐样本表征或整个分布完全一致
>
> 01
>
> 从统计量到校准操作
>
> 先分别估计两个模态的中心：
>
> 对每个输入，减去所属模态的均值：
>
> 条件：总体语义分布相容，残差均值近零。
>
> 02
>
> 用一个三维例子看清变化
>
> 表征
>
> 文字
>
> 图像
>
> 原始
>
> (2,1,0)
>
> (2.1,0.9,3)
>
> 均值
>
> (1,1,0)
>
> (1,1,3)
>
> 校准后
>
> (1,0,0)
>
> (1.1,−0.1,0)
>
> 03
>
> 能解决什么，不能解决什么？
>
> 同模态各点整体平移，内部差向量不变。
>
> 例子中第三维偏移消失；逐对误差、分布形状差异仍可能存在。
>

### 原 PPT 第 101 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-101.png]]

> [!quote]- 本页可搜索文字
> 4 Corrupt：输入加噪声，为什么反而有利于正确生成？
>
> 08 / 14
>
> §4 Corrupt；Algorithm 1，p.19；Appendix H，p.24。右侧二维图为教学示意，非实测分布或决策边界。
>
> 输入受扰动，目标保持原句 → 解码器学习容忍偏差；测试时只去均值
>
> 01
>
> 训练目标：邻近输入，仍重建同一句话
>
> 训练
>
> 文字表征 + 随机扰动 η
>
> 每次输入略有不同，目标句子仍是原句。
>
> 测试
>
> 图像表征减均值后直接解码
>
> 真实残差 ε 未知；训练学习对偏差的容忍。
>
> 02
>
> 用一个局部邻域理解训练
>
> 示意：去均值后的表征空间
>
> 文字表征
>
> 图像表征（测试）
>
> 浅蓝点：
>
> 训练扰动
>
> 目标保持：
>
> “一只狗在跑”
>
> 03
>
> 噪声的尺度与作用范围
>
> 太小覆盖不足，太大可能损害语义；也能缓解 gap。
>

### 原 PPT 第 102 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-102.png]]

> [!quote]- 本页可搜索文字
> 09 / 14
>
> §5.1；Appendix D–F，PDF pp.7、19–22。流程按图像描述任务重绘；生成图像使用另一套 GAN 目标。
>
> 冻结预训练语义连接，训练 MLP 与 GPT-2；测试时不输入真实答案
>
> 01
>
> 图像描述：输入、校准、生成、更新
>
> 训练
>
> 文字 y
>
> 文本编码器
>
> 去均值 + 噪声
>
> MLP +
>
> GPT-2
>
> 测试
>
> 图片 x
>
> 图像编码器
>
> 去均值
>
> MLP +
>
> GPT-2
>
> 编码器：冻结　　　　　　　　解码器：可训练
>
> 02
>
> 训练损失与 token 预测
>
> 03
>
> 参数与维度
>
> 4 完整流程：训练更新哪些参数，测试替换哪一环？
>
> 训练：真实前文 → 预测下个 token。
>
> 测试：已生成前文 → 继续预测。
>
> 512维 CLIP 向量 → MLP → 前缀序列
>
> 每个前缀位置为768维，送入 GPT-2。
>

### 原 PPT 第 103 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-103.png]]

> [!quote]- 本页可搜索文字
> 5 核心创新：把“可互换”的假设变成可分析、可改进的问题
>
> 10 / 14
>
> §1 contributions；§3–5；PDF pp.2–9。去均值与噪声操作有前作基础；跨任务结果为适用性证据。
>
> 核心增量：解释失配结构，并据此组合校准与鲁棒训练，检验跨任务适用性
>
> 01
>
> 贡献：认识、设计与适用性
>
> 理论
>
> 解释共享空间为何仍不互换
>
> 共同偏移与样本残差；给出条件分析与经验支持。
>
> 方法
>
> 输入校准 + 解码器鲁棒训练
>
> 去均值移动中心；扰动训练提高偏差容忍度。
>
> 应用
>
> 在多个跨模态任务中检验
>
> 图像／音频／视频描述，以及文字生成图像。
>
> 02
>
> 为什么值得学习？
>
> 1
>
> 抓住未经充分检验的假设
>
> 相似度匹配好，生成输入就能互换吗？
>
> 2
>
> 让每个设计有问题依据
>
> 先定位中心偏移与残差，再决定改哪一环。
>
> 3
>
> 用不同对照支撑不同主张
>
> 主效果、组件、机制和适用范围分别检验。
>
> 操作有前作基础；贡献在几何解释及据此形成的方法。
>

### 原 PPT 第 104 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-104.png]]

> [!quote]- 本页可搜索文字
> 11 / 14
>
> Table 1–7；Figures 3–6、10–11；Appendix C、G–I。验证维度为汇报归纳。
>
> 01
>
> 从“论文主张”到“可检查的证据”
>
> 6 实验逻辑：围绕五个问题组织证据
>
> 验证五类主张：几何现象、整体效果、组件贡献、适用范围与机制解释
>
> 主表回答效果；组件与机制实验解释原因；扩展实验检查适用范围。
>
> 要回答的问题
>
> 作者如何检验
>
> 对应证据
>
> 几何现象是否存在？
>
> 偏移长度／方向／正交性／残差统计
>
> Table 1；Fig. 3–5
>
> 方法能否改善任务？
>
> 图像描述与文字生成图像
>
> Table 2–3
>
> 组件贡献是什么？
>
> 固定 Connect；开关去均值与加噪
>
> Table 2–3 消融
>
> 适用范围有多大？
>
> 配对数据量；ImageBind 图像／音频／视频
>
> Fig. 6；Table 4–5
>
> 机制解释是否合理？
>
> 人为平移；移除噪声的 gap 方向；案例
>
> Table 6–7；Fig. 10–11
>

### 原 PPT 第 105 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-105.png]]

> [!quote]- 本页可搜索文字
> 6 主要结果：四种并列配置与结论边界
>
> 12 / 14
>
> Table 2–3、Figure 6，PDF p.8；Table 5，p.20。CIDEr对应描述任务，FID对应文生图；均为原文结果。
>
> 该设置中加噪贡献很大，完整组合更好；效果仍需限定任务、指标与数据条件
>
> 01
>
> 组件消融｜固定 Connect，分别开关
>
> 配置
>
> 去均值
>
> 加噪
>
> CIDEr ↑
>
> FID ↓
>
> Connect
>
> 否
>
> 否
>
> 13.0
>
> 29.8
>
> C²₁
>
> 是
>
> 否
>
> 25.2
>
> 21.7
>
> C²₂
>
> 否
>
> 是
>
> 87.6
>
> 19.8
>
> C³
>
> 是
>
> 是
>
> 93.3
>
> 19.6
>
> 四行均有 Connect；C²₂ 没有去均值。
>
> C³ 描述 CIDEr：93.3±0.3，不是准确率。
>
> 文生图 FID 改善0.2，不能据此判断显著性。
>
> 02
>
> Figure 6｜加入配对数据后的微调
>
> 1% 配对微调：C³ 96.4，ClipCap 71.1。
>
> 与左表零配对优化是不同协议。
>
> 03
>
> 适用条件也约束结论
>
> 100% 配对微调：C¹ 109.7 > C³ 108.9。
>
> Table 2 的 METEOR 也不是 C³ 最高。
>

### 原 PPT 第 106 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-106.png]]

> [!quote]- 本页可搜索文字
> 6 结果边界：明确支持了什么，也明确还没有验证什么
>
> 13 / 14
>
> Algorithm 1；Table 1–7；Appendix E–F。右栏为对原文证据范围的判断。
>
> 把结论限定在证据覆盖的范围，才能据此提出可靠的新研究问题
>
> 01
>
> 资源与协议｜“单模态”的含义
>
> 预训练
>
> 已借用多模态数据建立语义联系
>
> Connect 依赖现成 CLIP / ImageBind，不是从零训练。
>
> 校准
>
> 两模态集合分别估计均值
>
> 不需逐对对应，但需要说明集合来源与数据划分。
>
> 下游训练
>
> 图像描述阶段使用文字重建
>
> 验证、测试和少量配对微调应另行记录，不能混为一种协议。
>
> 02
>
> 证据范围｜不能自动推广的结论
>
> 理论
>
> 统计支持近似，不是普适精确分布
>
> 还不能证明任意领域的残差均为各向同性高斯。
>
> 评测
>
> 生成分数改善，不等于全部语义正确
>
> CIDEr / FID 和少量案例不完整衡量幻觉与文本遵循。
>
> 持续学习
>
> 本文没有任务序列与遗忘验证
>
> 将它用于旧知识保持，需要重新定义协议并取得证据。
>

### 原 PPT 第 107 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-107.png]]

> [!quote]- 本页可搜索文字
> 7 论文总结与研究演进：后续文献如何承接 C³？
>
> 14 / 14
>
> [1] Diffusion Bridge, CVPR 2025, §3  [2] Diffusion-Link, arXiv:2510.11330v1, §1–2  [3] ReAlign/ReVision, arXiv:2602.07026v1, §2–5
>
> 研究启发：顺着前作的解释，继续检验假设、改进对齐方式，并扩展适用任务
>
> 01
>
> C³ 留下了什么？
>
> 1
>
> 把问题拆开
>
> 图文能匹配，不代表输入可互换。
>
> 整体偏移与样本残差需要区分。
>
> 2
>
> 让操作对应解释
>
> 去均值处理整体偏移；加噪声
>
> 训练提高解码器对扰动的容忍。
>
> 3
>
> 留下可继续追问的假设
>
> 残差该怎样建模？能否学习映射？
>
> 其他模态和大模型能否受益？
>
> 02
>
> 后续文献｜承接点与推进
>
> Diffusion
>
> Bridge
>
> CVPR 2025
>
> 直接承接 C³
>
> 从“适应残差”到“学习去噪映射”
>
> 沿用残差分析，学习文本表征的扩散去噪；
>
> 推理时将图像表征转为类文本表征。
>
> 承接 C³ 的几何分析与去均值处理。
>
> Diffusion-Link
>
> arXiv 2025 · v1
>
> 沿扩散桥接扩展
>
> 从图像—文本桥接到音频—文本桥接
>
> 接续 Diffusion Bridge，将音频映射到文本分布，
>
> 增加拓扑约束，并用于音频描述。
>
> 条件变化：桥接模块训练使用配对音频—文本。
>
> ReAlign /
>
> ReVision
>
> arXiv 2026 · v1
>
> 重新审视 C³ 假设
>
> 从各向同性近似到方向相关残差分析
>
> 提出统计对齐，并用于文字替代视觉预训练；
>
> 将模态间隙问题带入多模态大模型训练。
>
> 条件变化：第二阶段仍使用真实图像做指令微调。
>
> 右栏为后续论文的工作；两篇 arXiv 文献按所读预印本版本标注。
>

### 原 PPT 第 108 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-108.png]]

> [!quote]- 本页可搜索文字
> C³
>
> CONNECT
>
> COLLAPSE
>
> CORRUPT
>
> ICLR 2024
>
> 感谢聆听
>
> 欢迎批评指正与交流
>
> Connect, Collapse, Corrupt
>
> Learning Cross-Modal Tasks with Uni-Modal Data
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-8MDVNFZD - Diffusion Bridge  Leveraging Diffusion Model to Reduce the Modality Gap Between Text |Diffusion Bridge: Leveraging Diffusion Model to Reduce the Modality Gap Between Text and Vision for Zero-Shot Image Captioning]] — 强关联；共同研究内容：对比学习与跨模态编码、模态间隙。
- [[Zotero Knowledge/Papers/ZK-FWQPPDF7 - Is the Modality Gap a Bug or a Feature  A Robustness Perspective|Is the Modality Gap a Bug or a Feature? A Robustness Perspective]] — 强关联；共同研究内容：对比学习与跨模态编码、模态间隙。
- [[Zotero Knowledge/Papers/ZK-WFNXHCV8 - Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Languag|Modality Gap-Driven Subspace Alignment Training Paradigm For Multimodal Large Language Models]] — 中关联；共同研究内容：对比学习与跨模态编码、模态间隙。
- [[Zotero Knowledge/Papers/ZK-I6438ULU - Diffusion-Link  Diffusion Probabilistic Model for Bridging the Audio-Text Modality Ga|Diffusion-Link: Diffusion Probabilistic Model for Bridging the Audio-Text Modality Gap]] — 中关联；共同研究内容：对比学习与跨模态编码、模态间隙。

<!-- content-relations:end -->
