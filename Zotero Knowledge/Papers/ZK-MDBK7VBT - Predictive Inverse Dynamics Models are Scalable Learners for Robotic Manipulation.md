---
type: "literature-note"
title: "Predictive Inverse Dynamics Models are Scalable Learners for Robotic Manipulation"
aliases: ["Predictive Inverse Dynamics Models are Scalable Learners for Robotic Manipulation"]
zotero_keys: ["MDBK7VBT"]
year: 2024
authors: ["Yang Tian", "Sizhe Yang", "Jia Zeng", "Ping Wang", "Dahua Lin", "Hao Dong", "Jiangmiao Pang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2412.15109"
url: "http://arxiv.org/abs/2412.15109"
collections: ["05 Robot Learning/World-Action Models"]
source_tags: ["Computer Science - Robotics"]
tags: ["zotero", "literature", "concept/动作接口与逆动力学", "concept-primary/动作接口与逆动力学"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Predictive Inverse Dynamics Models are Scalable Learners for Robotic Manipulation

[Zotero 条目 MDBK7VBT](zotero://select/library/items/MDBK7VBT)

[DOI 原文](https://doi.org/10.48550/arxiv.2412.15109)

[来源网页](http://arxiv.org/abs/2412.15109)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/World-Action Models/索引|05 Robot Learning/World-Action Models]]

概念地图：[[Zotero Knowledge/Concepts/动作接口与逆动力学|动作接口与逆动力学]]

补充阅读入口：[[Zotero Knowledge/Topics/05 Robot Learning/Planning & Inverse Control/索引|05 Robot Learning/Planning & Inverse Control]]

## 原始摘要

Current efforts to learn scalable policies in robotic manipulation primarily fall into two categories: one focuses on "action," which involves behavior cloning from extensive collections of robotic data, while the other emphasizes "vision," enhancing model generalization by pre-training representations or generative models, also referred to as world models, using large-scale visual datasets. This paper presents an end-to-end paradigm that predicts actions using inverse dynamics models conditioned on the robot's forecasted visual states, named Predictive Inverse Dynamics Models (PIDM). By closing the loop between vision and action, the end-to-end PIDM can be a better scalable action learner. In practice, we use Transformers to process both visual states and actions, naming the model Seer. It is initially pre-trained on large-scale robotic datasets, such as DROID, and can be adapted to realworld scenarios with a little fine-tuning data. Thanks to large-scale, end-to-end training and the synergy between vision and action, Seer significantly outperforms previous methods across both simulation and real-world experiments. It achieves improvements of 13% on the LIBERO-LONG benchmark, 21% on CALVIN ABC-D, and 43% in real-world tasks. Notably, Seer sets a new state-of-the-art on CALVIN ABC-D benchmark, achieving an average length of 4.28, and exhibits superior generalization for novel objects, lighting conditions, and environments under high-intensity disturbances on real-world scenarios. Code and models are publicly available at https://github.com/OpenRobotLab/Seer/.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### 06/02/2026, 20:56:20

[在 Zotero 查看](zotero://select/library/items/UGVPT75I)

**06/02/2026, 20:56:20**

**gpt-5-chat-latest:**

Here’s a comprehensive analysis and summary of **“Predictive Inverse Dynamics Models are Scalable Learners for Robotic Manipulation” (Yang Tian et al., 2024)**.

### **1. Motivation**

The authors address two key challenges in **scalable robot manipulation learning**:

- **Decoupled vision–action modeling**

   Prior works tend to either:

- Focus on *actions only* (e.g., behavior cloning from large robot datasets like RT-1, Octo), or

- Focus on *vision and representation learning* using visual pre-training (e.g., R3M, MVP, CLOVER).

   This decoupling limits generalization because vision and action are trained independently rather than in a **closed loop**, unlike human perception-action coordination.

- **Inefficient scaling and poor synergy**

   Training separate vision and control components fails to leverage their mutual information. The authors hypothesize that **jointly optimizing visual prediction and action generation**, in a temporally consistent manner, can yield more scalable and generalizable policies.

### **2. Core Innovation — “Predictive Inverse Dynamics Model” (PIDM)**

#### **a. Traditional Inverse Dynamics Model (IDM)**

A standard IDM learns a mapping:

$$f_{\text{IDM}}(o_t, o_{t+1}) \to a_t$$

That is, given **current** and **next** observations, it predicts the **action** that transitions between them.  
However:

- The future state $o_{t+1}$ is **observed**, not *predicted*.

- IDM training is **supervised** on existing trajectory pairs — no imagination or foresight.

- This limits generalization when encountering unseen situations, since the policy cannot anticipate novel future states.

#### **b. Predictive Inverse Dynamics Model (PIDM)**

The key innovation is **adding prediction into the loop** — hence the “predictive” in the name.

The proposed Seer model **first predicts** a *future visual state* ($\hat{o}_{t+n}$) via a **visual foresight module**, and then conditions the action policy on this prediction using an inverse dynamics predictor.

This modifies the standard IDM pipeline into a *closed-loop predictive system*:

- **Conditional Visual Foresight**

   Learn $f_{\text{fore}}(g, h_t) \to \hat{o}_{t+n}$  
   where $g$ is the goal (language or robot state), and $h_t$ are the previous visual and state histories.

   → This module “imagines” what the robot should *see next* to achieve the goal.

- **Inverse Dynamics Prediction**

   Learn $f_{\text{inv}}(g, h_t, \hat{o}_{t+n}^l) \to \hat{a}_{t:t+n-1}$  
   where $\hat{o}_{t+n}^l$ is the latent version of the predicted image.

   → This module predicts the sequence of actions that transform current to *predicted* visual states.

- **Joint Loss & End-to-End Optimization**

   The two modules are trained **synergistically**:

$$L = \alpha L_{\text{fore}} + L_{\text{inv}}$$

   where

- $L_{\text{fore}}$: Mean-squared pixel reconstruction of predicted image,

- $L_{\text{inv}}$: Sum of arm and gripper losses.

By closing the loop between **vision prediction** and **action inference**, the model internally simulates *future consequences* of actions — unlike traditional IDMs which only react to observed data.

### **3. Methodology (Architecture: Seer)**

**Seer** integrates these modules inside a **Transformer-based multimodal architecture**:

 | Component | Description

 | **Input Tokenizers** | Encode text (CLIP), images (MAE-based ViT + Perceiver resampler), and robot states (MLP).

 | **Tokens** | Two special readout tokens: [FRS] for foresight and [INV] for inverse dynamics.

 | **Multi-modal Encoder** | GPT-2-style transformer integrating visual, linguistic, and state tokens. A **unidirectional attention mask** allows [INV] to attend to [FRS] (future predictions).

 | **Decoders** | ViT decoder reconstructs the predicted image; MLP decoder outputs the action vector.

 | **Training** | Pre-train on large robot datasets (e.g., DROID), then fine-tune with limited task-specific data.

Crucially, this design allows [INV] (action) tokens to *use the predicted future image representation* from [FRS] — closing the perception-action loop *in latent space*.

### **4. Experimental Results**

**Benchmarks & Results**

 | Benchmark | Domain | Seer vs SOTA | Highlights

 | LIBERO-LONG | Simulation (10 long-horizon tasks) | +9% over baseline | Achieves 87.7% success rate

 | CALVIN ABC-D | Language-conditioned manipulation | +0.75 task length; +21% average success | New SOTA (Avg. Length 4.28 for Seer-Large)

 | Real-world (6 tasks) | Franka robot | +18% success rate | Robust under lighting, background, and object disturbances

**Key findings:**

- End-to-end pretraining (with both $L_{\text{fore}} + L_{\text{inv}}$) clearly outperforms vision-only or action-only pretraining.

- Works well with **limited fine-tuning data (10–40%)**, maintaining strong performance (∼2× improvement under data scarcity).

- Demonstrates *robustness* to disturbances (lighting, unseen objects).

### **5. Why “Predictive” and How It Differs from Prior PIDM Works**

Several earlier works (e.g., CLOVER, Susie, GR-1) already use two-stage “predictive inverse dynamics” setups — *predict future visual goals → train inverse dynamics policy*.  
However, **this paper is the first to make it *end-to-end***.

 | Aspect | Previous Two-Stage PIDM | This Paper’s End-to-End PIDM

 | Vision prediction | Pre-trained separately on videos | Jointly learned with action model

 | Supervision | Sequential (frozen world model → train controller) | Simultaneous (shared gradients through foresight)

 | Visual grounding | Fixed | Adaptively refined during policy optimization

 | Data source | Purely visual or mixed | Large-scale robot datasets (e.g., DROID)

 | Integration | Loose connection | Tight “closed-loop” between predicted vision and action

Thus, *“Predictive”* reflects the model’s capacity to **forecast the future visual state** *and* use it as a conditioning signal for action prediction **within the same optimization loop**.

### **6. Achievements and Significance**

- Establishes **a new paradigm**: *closing the loop between foresight (vision) and inverse dynamics (action).*

- Demonstrates **state-of-the-art performance** with fewer parameters than prior mammoth-scale models (e.g., OpenVLA 7B vs Seer 316M total).

- Shows **scalability and data efficiency**, essential for practical robotics.

- Reinforces the idea that **predictive modeling of sensory feedback** (imagination) is key to robust robot control — echoing cognitive learning principles.

### **7. Summary of Differences vs Classical IDM**

 | Criterion | Classic IDM | Predictive IDM (Seer)

 | Input states | $(o_t, o_{t+1})$ (observed) | $(o_t, \hat{o}_{t+n})$ (predicted)

 | Vision–action coupling | Disconnected | End-to-end coupled

 | Temporal foresight | None | Predictive horizon $n$

 | Training data | Reactive (paired demos) | Simulative (visual imagination)

 | Learning scope | Short-term, local | Long-horizon, generalizable

 | Optimization | Action-only | Joint vision + action

 | Nature | Reactive mapping | Predictive modeling

#### **In essence:**

The “Predictive” Inverse Dynamics Model makes the inverse dynamics **anticipatory** — it *imagines future visual outcomes first,* then chooses actions consistent with that prediction, learned jointly in one framework.

**In one sentence:**  

*Seer transforms the Inverse Dynamics Model from a reactive action mapper into a predictive, end-to-end vision–action learner that closes the perception-action loop and scales effectively across datasets and real-world tasks.*

Written by AIdea plugin

### Comment: Project page: https://nimolty.github.io/Seer/

[在 Zotero 查看](zotero://select/library/items/B5WPRIS5)

Comment: Project page: https://nimolty.github.io/Seer/

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/MQH5VZUB)

[批注 7KS63KUQ · 第 3 页](zotero://open-pdf/library/items/MQH5VZUB?annotation=7KS63KUQ&page=3)

> In contrast, we pre-train policies by integrating conditional visual foresight and inverse dynamics prediction, allowing for comprehensive utilization of robotic data

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/9R7JEQ5P)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-KCN9NGKR - World Action Verifier  Self-Improving World Models via Forward-Inverse Asymmetry|World Action Verifier: Self-Improving World Models via Forward-Inverse Asymmetry]] — 强关联；都将未来状态与逆向动作推断连接；比较预测验证与机器人策略学习。
- [[Zotero Knowledge/Papers/ZK-YFP6L7BZ - Masked Visual Actions for Unified World Modeling|Masked Visual Actions for Unified World Modeling]] — 中关联；共同研究内容：想象与模型式强化学习、策略评测与模拟可靠性、逆动力学与潜在动作。
- [[Zotero Knowledge/Papers/ZK-DJRBHBIA - Learning inverse dynamics models in O(n) time with LSTM networks|Learning inverse dynamics models in O(n) time with LSTM networks]] — 中关联；共同研究内容：基准与数据合成、语言模型与语言表征、逆动力学与潜在动作。

<!-- content-relations:end -->
