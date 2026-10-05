---
type: "literature-note"
title: "State, Action, and Transition: A Bottleneck-Driven Survey of World Models"
aliases: ["State, Action, and Transition: A Bottleneck-Driven Survey of World Models"]
zotero_keys: ["RM5XURCS"]
year: null
authors: ["Yuxi Lu", "Zhidong Li", "Kunqi Li", "Chenya Huang", "Bin Liang"]
venue: ""
venue_field: null
doi: ""
url: ""
collections: ["04 World Models/Concepts & Design"]
source_tags: []
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# State, Action, and Transition: A Bottleneck-Driven Survey of World Models

[Zotero 条目 RM5XURCS](zotero://select/library/items/RM5XURCS)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Concepts & Design/索引|04 World Models/Concepts & Design]]

## 原始摘要

> Zotero 尚无摘要。该条目需要补录或核读原文。

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### 06/08/2026, 10:28:48

[在 Zotero 查看](zotero://select/library/items/U8M4BZXI)

**06/08/2026, 10:28:48**

**gpt-5-chat-latest:**

Here’s a concise but comprehensive summary of the **core survey incentives** and their **corresponding outcomes** from *“State, Action, and Transition: A Bottleneck-Driven Survey of World Models.”*

### **Core Survey Incentives**

The authors’ motivation stems from the **fragmentation** of research on world models across domains such as **video generation**, **autonomous driving**, and **robotics**. This fragmentation has led to inconsistent representations, evaluation metrics, and bottlenecks that obscure comparison. 
To resolve this, the paper sets out three central **incentives**:

#### 1. **Unification through Minimal Transition Formalism**

- 
**Incentive:** Provide a unified analytical lens for all world models, using the general transition formula

$$s_{t+1} \sim p_\theta(\cdot | s_t, a_t)$$

where future states depend on the current state and an interventional action via a transition function.

- 
**Purpose:** This abstraction reduces every world model to three *irreducible design dimensions*:

- 
**State representation (sₜ):** how the world is perceived.

- 
**Action representation (aₜ):** how agents intervene.

- 
**Transition modeling (pθ):** how the world evolves.

#### 2. **Bottleneck-Driven Taxonomy**

- 
**Incentive:** Diagnose where and why world models break down—specifically in *physical consistency*, *interaction reliability*, and *long-horizon stability*—by analyzing choices in these three dimensions.

- 
**Motivation:** Previous surveys classified models by domain (e.g., driving, video) or architecture type (e.g., transformers, diffusion), which obscures cross-domain comparisons and hides underlying design failures.

#### 3. **Synthesis of Future Research Directions**

- 
**Incentive:** Integrate the identified bottlenecks into conceptual pathways for advancing towards **Interactive Cognitive World Models**—systems that combine stable world understanding, intentional control, and reliable long-term dynamics.

### **Corresponding Outcomes**

The paper organizes outcomes around **the three core dimensions** and the **new research directions** they inspire.

#### **1. State Representation**

**Findings:**

- 
**2D Paradigm (videos/images):**

- 
Pros: Scales easily with internet data; captures coarse motion regularities.

- 
Cons: Lacks 3D metric structure → causes geometric drift and poor physical grounding.

- 
**3D/4D Paradigm (occupancy grids, LiDAR, NeRF/GS):**

- 
Pros: Encodes spatial consistency and viewpoint invariance.

- 
Cons: Faces *data scarcity* and fails to internalize *latent physical variables* (e.g., material or fluid dynamics).

**Outcome:** 
A clear trade-off emerges: 2D models excel at *scale* but lack *structure*; 3D/4D models enforce *structure* but lack *scalable data*.

#### **2. Action Representation**

**Findings:**

- 
**Semantic Actions:**

- 
High-level natural language prompts enable open-vocabulary control but are underspecified physically.

- 
**Executable Actions:**

- 
Low-level, machine-controllable signals offer reliable control but are narrow and non-transferable.

**Outcome:** 
There is a tension between *expressive intent* and *operational precision*. Future models must link semantic intent to executable, grounded dynamics.

#### **3. Transition Modeling**

**Findings:**

- 
**Implicit Transition Models (data-driven):**

- 
Include autoregressive (AR), diffusion, JEPA, and RSSM families.

- 
Pros: Scalable, flexible, and effective for long-horizon generative rollouts.

- 
Cons: Typically lack verifiable physical mechanisms and suffer from roll-out instability and computational cost.

- 
**Explicit Transition Models (physics-driven):**

- 
Include simulation-based engines like MuJoCo, Brax, and DiffTaichi.

- 
Pros: Enforce physical consistency and causal validity.

- 
Cons: Limited by human-specified rules and narrow generalization capacity.

**Outcome:** 
Implicit and explicit models exhibit **complementary bottlenecks**—data-driven models generalize widely but drift physically; physics-driven ones are faithful but narrow.

### **Synthesized Research Directions**

The authors integrate the above findings into **three concrete strategies for next-generation world models**:

 | 

Direction

 | 

Aim

 | 

Core Idea

 | 

**Active Intervention Loop**

 | 

Move beyond passive video prediction

 | 

Couple action, prediction, and feedback so models learn through active, counterfactual interventions.

 | 

**Physical Laws Internalization**

 | 

Prevent long-term drift

 | 

Embed universal physical constraints (e.g., momentum conservation, rigidity) into learned dynamics.

 | 

**Progressive Structural Integration**

 | 

Reconcile data imbalance

 | 

Combine large-scale unlabeled video with limited structured 3D or action-labeled data through self-supervised, multi-view consistency and hierarchical learning.

**Outcome:** 
These pathways jointly aim to achieve **Interactive Cognitive World Models**—systems capable of *stable representation*, *intentional control*, and *reliable long-horizon prediction*.

### **Overall Contribution**

**In summary:**

- 
The paper reframes the scattered world-model literature into a **minimal, bottleneck-oriented framework** with three axes (state, action, transition).

- 
It exposes **cross-domain bottlenecks** in scalability, physical grounding, and control precision.

- 
It synthesizes **principled future directions** that integrate active learning, physics-informed priors, and progressive structural representation.

**Ultimate Outcome:** 
A coherent research agenda for evolving from generative visual models toward *Interactive Cognitive World Models*—models that not only see and predict the world but *understand, act, and reason within it*.

Written by AIdea plugin

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/7LXIDWF2)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
