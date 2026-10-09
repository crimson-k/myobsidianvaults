---
type: "literature"
title: "Sigmoid Loss for Language Image Pre-Training"
aliases: ["SigLIP"]
zotero_keys: ["2IQ6RLSK"]
year: 2023
authors: ["Zhai, Xiaohua", "Mustafa, Basil", "Kolesnikov, Alexander", "Beyer, Lucas"]
venue: "ICCV 2023"
doi: ""
url: "https://arxiv.org/abs/2303.15343"
collections: ["02 Representation & Perception/Vision-Language Representation", "90 Projects/Pattern Recognition Course/Project 1/Group 2"]
tags: ["zotero", "literature", "course/pattern-recognition", "ppt/group-2"]
reading_status: "presentation-import"
ppt_role: "main"
ppt_pages: [39, 53]
imported_at: "2026-10-03"
---

# Sigmoid Loss for Language Image Pre-Training

[在 Zotero 打开](zotero://select/library/items/2IQ6RLSK) · [论文来源](https://arxiv.org/abs/2303.15343) · [论文 PDF](https://arxiv.org/pdf/2303.15343)

## 文献导读

将批次级 softmax 对比损失改为图文对级 sigmoid 损失，减少全局归一化依赖。比较时保留批次规模、负样本比例、训练资源与数据条件。

## 主题与关联

[[Zotero Knowledge/Topics/02 Representation & Perception/Vision-Language Representation/索引|02 Representation & Perception/Vision-Language Representation]] · [[Zotero Knowledge/Topics/90 Projects/Pattern Recognition Course/Project 1/索引|项目一文献分享]]

以下为阅读比较建议，并非已经证实的文献依赖关系。

- [[Zotero Knowledge/Papers/ZK-CDHTS2WR - Learning Transferable Visual Models From Natural Language Supervision|CLIP]]
- [[Zotero Knowledge/Papers/ZK-W84DWQI5 - LiT  Zero-Shot Transfer with Locked-image text Tuning|LiT]]
- [[Zotero Knowledge/Papers/ZK-TVYG4KJ8 - SigLIP 2  Multilingual Vision-Language Encoders with Improved Semantic Understanding,|SigLIP 2]]

## 原始摘要

We propose a simple pairwise Sigmoid loss for Language-Image Pre-training (SigLIP). Unlike standard contrastive learning with softmax normalization, the sigmoid loss operates solely on image-text pairs and does not require a global view of the pairwise similarities for normalization. The sigmoid loss simultaneously allows further scaling up the batch size, while also performing better at smaller batch sizes. Combined with Locked-image Tuning, with only four TPUv4 chips, we train a SigLiT model that achieves 84.5% ImageNet zero-shot accuracy in two days. The disentanglement of the batch size from the loss further allows us to study the impact of examples vs pairs and negative to positive ratio. Finally, we push the batch size to the extreme, up to one million, and find that the benefits of growing batch size quickly diminish, with a more reasonable batch size of 32k being sufficient. We release our models at this https URL and hope our research motivates further explorations in improving the quality and efficiency of language-image pre-training.

来源：[论文官方页面](https://arxiv.org/abs/2303.15343)。

## PPT 文献分享原页

来源：[第 2 组原 PPT](../Assets/Original%20PPTs/%E9%A1%B9%E7%9B%AE%E4%B8%80%E7%AC%AC%E4%BA%8C%E7%BB%84%E6%96%87%E7%8C%AE%E5%88%86%E4%BA%AB%EF%BC%88%E4%BF%AE%E6%94%B9%E7%89%88%EF%BC%89.pptx)，原文件第 39–53 页。

页面图保留原图表、公式和排版；下方折叠文本供搜索。汇报中的解释、教学示例和实验数字均属于来源材料，尚未逐项对照论文全文复核。

### 原 PPT 第 39 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-039.png]]

> [!quote]- 本页可搜索文字
> ICCV 2023 · Google DeepMind (Zürich)
>
> SigLIP: Sigmoid Loss
>
> for Language Image Pre-Training
>
> 把图文对比学习从「多选」改成「判断」
>
> 汇报人：韩敬霄　·　2026 年 9 月 30 日
>
> 论文：Xiaohua Zhai, Basil Mustafa, Alexander Kolesnikov, Lucas Beyer
>

### 原 PPT 第 40 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-040.png]]

> [!quote]- 本页可搜索文字
> TLDR：SigLIP做了三件事
>
> 2
>
> 换损失
>
> softmax → sigmoid：每一对图文独立判断「配 / 不配」
>
> 不再需要跨整个 batch 做归一化，也不再有方向不对称的问题
>
> 省资源
>
> 损失可以分块计算：显存从 |B|² 降到 b²，去掉 all-gather
>
> 同样硬件下 batch 能开得更大，而小 batch 时反而更准
>
> 改认知
>
> 性能在 32k batch 就饱和，继续加大几乎无收益
>
> batch 推到 100 万也没用，「对比学习需要超大 batch」的思想需要修正
>
> 全篇只改了损失函数和两个初始化值，没动模型结构。
>

### 原 PPT 第 41 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-041.png]]

> [!quote]- 本页可搜索文字
> 背景：CLIP 怎么让图文对齐
>
> 3
>
> T₁
>
> T₂
>
> T₃
>
> T₄
>
> I₁
>
> 正对
>
> 负对
>
> 负对
>
> 负对
>
> I₂
>
> 负对
>
> 正对
>
> 负对
>
> 负对
>
> I₃
>
> 负对
>
> 负对
>
> 正对
>
> 负对
>
> I₄
>
> 负对
>
> 负对
>
> 负对
>
> 正对
>
> 一个 mini-batch 里 |B| 对图文，两两组合出 |B|×|B| 张分数表。
>
> 对角线上那 |B| 个是正对，其余 |B|²−|B| 个都是负对。
>
> 这张表里的两件事
>
> 正对：本来就在同一条数据里的图和文，也就是对角线。
>
> 负对：同一 batch 里别人的配文，是「凑」出来的假设，不是标注出来的。
>
> 训练目标：让配对的两条向量接近，不配对的远离。
>
> “This assumption is usually noisy and imperfect.”一批数据里可能有两张狗的图、两条相似的配文，那这个「负对」其实就是误标。这句话是后面两个消融实验的伏笔。
>

### 原 PPT 第 42 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-042.png]]

> [!quote]- 本页可搜索文字
> 背景：softmax 损失的三个代价
>
> 4
>
> 通信
>
> 分母跨越整个 batch
>
> 每张卡必须先把全部图文嵌入 all-gather 过来，算完还要减最大值做数值稳定，等于再遍历一遍 batch。
>
> 显存
>
> 要同时物化 |B|×|B| 的相似度矩阵
>
> 矩阵规模随 batch 平方增长：batch 翻倍，显存需求变成四倍。
>
> 任务
>
> batch 被写进损失的定义里
>
> 换一个 batch 就等于换了一个任务；小 batch 下负例太少，softmax 明显吃亏。
>
> 于是「大 batch」变成了必需品。但大 batch 意味着更多芯片、更大显存、更贵的通信——这正是SigLIP想绕开的东西。
>

### 原 PPT 第 43 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-043.png]]

> [!quote]- 本页可搜索文字
> 核心改动：从「多选」变成「判断」
>
> 5
>
> softmax 对比损失（原 CLIP）
>
> 对每张图，从 |B| 段文本里挑出正确的那一段。分母 Σⱼ 跨越整个 batch，图像方向和文本方向还要各归一化一次。
>
> sigmoid 损失（本文）
>
> 每一对图文独立做一个二分类，没有任何一项跨越样本。损失天然对称，一遍算完。
>
> 一句话：softmax 是「从 |B| 个里选一个」，sigmoid 是「这一对配不配」。
>
> softmax 对比损失
>
> sigmoid 损失
>
> 任务形态
>
> |B| 类的分类问题
>
> |B|² 个独立二分类
>
> 跨 batch 归一化
>
> 需要
>
> 不需要
>
> 负对的作用
>
> 只作分母里的干扰项
>
> 每一对都直接产生一个损失项
>
> 显存占用
>
> |B|×|B| 全矩阵必须同时在位
>
> 每对独立，可以拆成分块
>

### 原 PPT 第 44 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-044.png]]

> [!quote]- 本页可搜索文字
> 方法细节：b = −10 让训练起点接近先验
>
> 6
>
> 1 : 16384
>
> 16k 的 batch 里有 268M 个负对，正对只有 16k 个。
>
> 初始时 logit ≈ 0，模型对每一对都预测「五五开」。但正对实际只占 0.006%，于是损失几乎全由负例贡献，训练一开始就会产生巨大的过校正步长。
>
> 解法：加一个可学习偏置 b
>
> b 和温度 t′ 一起初始化：t′ = log 10（即 t = 10）、b = −10，让训练起点接近真实先验，不需要大幅纠偏。
>
> b
>
> t′
>
> INet-0
>
> Pet-0
>
> C100-0
>
> 无偏置
>
> log 10
>
> 62.0
>
> 81.8
>
> 59.9
>
> −10
>
> log 10
>
> 63.0
>
> 82.4
>
> 61.0
>
> 0
>
> log 10
>
> 61.7
>
> 79.9
>
> 59.0
>
> 0
>
> log 1
>
> 53.7
>
> 73.2
>
> 53.8
>
> 表 4：Base 架构、8k batch、900M 样本，ImageNet / Pet / CIFAR-100 零样本准确率。
>
> 论文的表述：b = −10 使训练「starts roughly close to the prior」，不需要 massive over-correction。消融结果：加偏置比不加稳定高 1.0 分；而随机初始化（b = 0）反而更差，温度初始化小的时候直接崩到 53.7。
>

### 原 PPT 第 45 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-045.png]]

> [!quote]- 本页可搜索文字
> 工程实现：分块计算，显存 |B|² → b²
>
> 7
>
> 论文 Figure 1：3 张设备、全局 batch 为 12 的分块示例
>
> 不需要 all-gather
>
> D 次 collective permute 通常比 2 次 all-gather 更快
>
> 显存 |B|² → b²
>
> 每张卡任意时刻只需要装下 b×b 的分块，b = |B| / D
>
> 各卡独立算再求和
>
> 损失的加法性质让分块计算在数学上完全等价
>

### 原 PPT 第 46 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-046.png]]

> [!quote]- 本页可搜索文字
> 实验在回答什么：四个问题
>
> 8
>
> 要回答的问题
>
> 对应的实验
>
> 结论
>
> 换成 sigmoid，效果会不会变差？
>
> SigLiT / SigLIP 在完全相同的设定下只换损失，扫一遍 batch size
>
> 小 batch 明显更好；大 batch 略好
>
> batch 还要不要很大？
>
> batch 从 512 实验到 100 万；多语言设定另外扫一遍
>
> 32k 就饱和，再大没有收益甚至更差
>
> 省下来的资源真能用上吗？
>
> 用 4 / 16 / 32 张 TPUv4 训练，并给出配套工程配方
>
> 4 张卡 2 天训到 84.5%
>
> 负对假设出错会怎样？
>
> 遮蔽负例调整正负比；往训练数据里注入标签噪声
>
> 对噪声更鲁棒；难负例是主要信号
>
> 三个指标
>
> ImageNet 零样本 top-1（INet-0）
>
> 模型没在 ImageNet 上训过，靠「a photo of a {类}」这类文本去匹配分类，数字就是准确率。
>
> XM3600 recall@1
>
> 覆盖 36 种语言的跨模态检索；T→I 指「给文找图」，数值是正确项排第一的比例。
>
> ImageNet 10-shot 线性分类
>
> 冻结图像塔只训一个线性分类头，用来检验图像特征本身好不好。
>

### 原 PPT 第 47 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-047.png]]

> [!quote]- 本页可搜索文字
> 实验一：batch 越小，sigmoid 的优势越大
>
> 9
>
> 差距在 16k batch 以内最明显，batch 越大差距越小。
>
> 128k 时 softmax 短暂反超 0.2 分，说明大 batch 下两者基本持平。
>
> 原因：softmax 只把负例放在分母里，负例少时学不充分；sigmoid 每一对都直接产生损失项。
>
> 数据：论文 Table 8（SigLiT，3B 样本，ImageNet 零样本）
>

### 原 PPT 第 48 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-048.png]]

> [!quote]- 本页可搜索文字
> 实验二：32k batch 就饱和，再大没有收益
>
> 10
>
> SigLIP（9B 样本）
>
> sigmoid 峰值在 32k，73.4%；softmax 要到 98k 才到 73.2%，仍低 0.2 分；307k 时两者都退化。
>
> SigLiT（18B 样本）
>
> 64k / 128k / 256k / 1024k 全都是 84.7%，完全持平——百万级 batch 是能训，不是有用。
>
> mSigLIP（100+ 语言，30B 样本）
>
> XM3600 36 语言平均 T→I recall@1：32k 34.9 → 64k 34.4 → 128k 33.6 → 240k 32.7，越大越差。
>
> 限定：大 batch 只有在训练足够长时才划算。论文 Figure 3 里 262k batch 要训得足够久才超过 8k；短 schedule 下大 batch 的更新步数太少，反而更差。
>
> 数据：论文 Table 5（SigLIP 9B）、Table 8（SigLiT）、Table 2（mSigLIP）
>

### 原 PPT 第 49 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-049.png]]

> [!quote]- 本页可搜索文字
> 实验三：四张 TPUv4 两天，训到 84.5%
>
> 11
>
> 设定
>
> 图像塔
>
> 文本塔
>
> batch
>
> 芯片
>
> 时间
>
> INet-0
>
> SigLiT
>
> B/8（冻结）
>
> L*
>
> 32k
>
> 4
>
> 1 天
>
> 79.8
>
> SigLiT
>
> g/14（冻结）
>
> L
>
> 20k
>
> 4
>
> 2 天
>
> 84.5
>
> SigLIP
>
> B/16（预训练塔微调）
>
> B
>
> 16k
>
> 16
>
> 3 天
>
> 71.0
>
> SigLIP
>
> B/16（从零）
>
> B
>
> 32k
>
> 32
>
> 2 天
>
> 72.1
>
> SigLIP
>
> B/16（从零）
>
> B
>
> 32k
>
> 32
>
> 5 天
>
> 73.4
>
> Adam& AdaFactorβ₂：0.999 → 0.95大 batch 下梯度范数尖峰会打崩训练。
>
> 微调预训练图像塔时关掉 weight decay否则 10-shot 线性分类几乎不比从零好。
>
> 多语言用瓶颈嵌入（K = 96, W = 768）相比完整 250k 词表只掉约 0.5 分。
>
> · 前两行是 SigLiT 设定：图像塔是冻结的，而且图片嵌入是预先算好存下来的，这部分成本不在「1 天 / 2 天」里。· 作为参照，论文引用 FLIP 的数据：CLIP 达到 72.6% 大约需要 2500 TPUv3-days。
>

### 原 PPT 第 50 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-050.png]]

> [!quote]- 本页可搜索文字
> 实验四：负例不均衡不可怕，标签噪声也不可怕
>
> 12
>
> 负例比例
>
> SigLiT，16k batch，900M 步
>
> 随机遮蔽负例，把正负比调到 1:1.6 —— 掉点
>
> 只保留最简单的负例 —— 完全训不动
>
> 只保留最难的负例 —— 几乎不掉点；在匹配总配对数的设定下还略有提升
>
> 结论：不平衡本身不是主要问题，难负例才是主要的学习信号。
>
> 标签噪声
>
> M/16 + M 文本塔，16k batch，3.6B 样本
>
> 污染方式：以概率 p 把图片换成随机噪声、把文本换成随机 token、打乱 batch 内的图文对齐
>
> 结果：随污染加重，sigmoid 训练的模型始终优于对应的 softmax 基线
>
> 这两组实验都在回应第 3 页那句「负对假设是有噪声的」。
>
> 怎样高效地把更多难负例放进 batch「有希望，但并不简单」—— 这个问题没有被真正解决。
>

### 原 PPT 第 51 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-051.png]]

> [!quote]- 本页可搜索文字
> Baseline：400M 的模型超过 5B 的 EVA-CLIP
>
> 13
>
> 方法
>
> 图像塔
>
> patches
>
> ImageNet 零样本
>
> CLIP
>
> B
>
> 196
>
> 68.3
>
> OpenCLIP
>
> B
>
> 196
>
> 70.2
>
> EVA-CLIP
>
> B
>
> 196
>
> 74.7
>
> SigLIP
>
> B
>
> 1024
>
> 79.2
>
> CLIP
>
> L
>
> 576
>
> 76.6
>
> SigLIP
>
> L
>
> 576
>
> 82.1
>
> EVA-CLIP
>
> E (5B)
>
> 256
>
> 82.0
>
> SigLIP
>
> SoViT (400M)
>
> 729
>
> 83.2
>
> 同样是 B 档、同样 196 patches：SigLIP 76.2，CLIP 68.3，OpenCLIP 70.2，EVA-CLIP 74.7。
>
> L 档、576 patches：82.1，比 CLIP-L 的 76.6 高 5.5 分。
>
> 400M 参数的 SoViT 版做到 83.2%，超过 5B 参数的 EVA-CLIP（82.0%）。
>
> 这是跨论文比较：训练数据、分辨率、算力预算都不对齐，只能当量级参照，不是受控实验。Table 3 的完整表更长，需要细节可以问。
>
> 数据：论文 Table 3（精选 8 行）
>

### 原 PPT 第 52 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-052.png]]

> [!quote]- 本页可搜索文字
> 总结与评价
>
> 14
>
> 总结
>
> 换损失：sigmoid 让图文预训练不再需要跨 batch 归一化 —— 对称、单遍、省内存。
>
> 改工程：损失因此可以分块算，显存 |B|² → b²、无 all-gather，支撑百万级 batch。
>
> 改认知：性能在 32k 就饱和，大 batch 不再是必需品，预算有限的团队也能做。
>
> 局限
>
> 主要数据 WebLI 是私有的；SigLiT 还依赖预计算好的冻结嵌入，外部完全复现门槛高。
>
> 32k 是在 WebLI 系数据、特定模型规模和 schedule 下得到的经验值，换setup未必成立。
>
> 「非同图文本视为负例」这个假设本身有噪声，论文没有真正解决。
>
> 论文没有独立的 Limitations 章节，算力开销也只给了一个单点对比。
>
> 可学习的点：
>
> 做对比学习先试 sigmoid 损失；
>
> batch 先开 32k；
>
> β₂ 调成 0.95；
>
> 微调预训练图像塔时关掉 weight decay。
>

### 原 PPT 第 53 页

![[Zotero Knowledge/Assets/PPT Import 2026-10-03/Group 2/slide-053.png]]

> [!quote]- 本页可搜索文字
> 延伸
>
> 15
>
> SigLIP 2（2025，Google）
>
> 动机：补原版两个短板 —— 多语言强但英文变弱；只做全局图文匹配，密集特征与定位能力弱。
>
> 手段：加入 captioning 生成式目标、用冻结教师做自蒸馏、掩码预测类目标（TIPS）、多语言数据扩充与去偏。
>
> 结果：多语言与英文同时提升，密集特征和定位任务明显改善，同等性能下训练更省。
>
> 档位：B / L / So400m / g，并新增可变分辨率的 NaFlex 版本。
>
> 被大量多模态模型当作视觉塔
>
> 后续工作
>
> 使用
>
> PaLI-3（同组，2023）
>
> 直接以 SigLIP 作视觉塔
>
> PaliGemma / PaliGemma 2（2024）
>
> 视觉塔为 SigLIP-So400m
>
> Idefics2（HuggingFace, 2024）
>
> 使用 SigLIP-SO400M
>
> Gemma 3（2025）
>
> SigLIP 系视觉编码器
>
> Prismatic VLMs / OpenVLA（2024）
>
> DINOv2 + SigLIP 特征融合
>
> 值得注意的分工：SigLIP 管语义对齐，DINOv2 管空间细节 —— 恰好补上原版密集特征的短板。
>
> 一篇只改损失函数的论文，最后成了多模态模型视觉编码器的常见默认选项之一。
>

## 我的阅读与思考

<!-- 在此补充个人笔记；导入内容与个人结论分开记录。 -->

[[Zotero Knowledge/知识库首页|知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-TVYG4KJ8 - SigLIP 2  Multilingual Vision-Language Encoders with Improved Semantic Understanding,|SigLIP 2: Multilingual Vision-Language Encoders with Improved Semantic Understanding, Localization, and Dense Features]] — 强关联；对方摘要提到模型 SigLIP（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-88IZNLUX - Understanding Contrastive Representation Learning through Alignment and Uniformity on|Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere]] — 强关联；共同研究内容：对比学习与跨模态编码。
- [[Zotero Knowledge/Papers/ZK-GDGTULM9 - Unlearning the Noisy Correspondence Makes CLIP More Robust|Unlearning the Noisy Correspondence Makes CLIP More Robust]] — 中关联；共同研究内容：对比学习与跨模态编码。
- [[Zotero Knowledge/Papers/ZK-YMBWZADV - A Simple Framework for Contrastive Learning of Visual Representations|A Simple Framework for Contrastive Learning of Visual Representations]] — 中关联；共同研究内容：对比学习与跨模态编码。

<!-- content-relations:end -->
