---
type: "literature-note"
title: "Learning inverse dynamics models in O(n) time with LSTM networks"
aliases: ["Learning inverse dynamics models in O(n) time with LSTM networks"]
zotero_keys: ["DJRBHBIA"]
year: 2017
authors: ["Elmar Rueckert", "Moritz Nakatenus", "Samuele Tosatto", "Jan Peters"]
venue: "2017 IEEE-RAS 17th International Conference on Humanoid Robotics (Humanoids)"
venue_field: "proceedingsTitle"
doi: "10.1109/HUMANOIDS.2017.8246965"
url: "https://ieeexplore.ieee.org/document/8246965"
collections: ["05 Robot Learning/Planning & Inverse Control"]
source_tags: ["Computational modeling", "Gaussian processes", "Inverse problems", "Predictive models", "Robot sensing systems", "Training"]
tags: ["zotero", "literature", "concept/动作接口与逆动力学", "concept-primary/动作接口与逆动力学"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Learning inverse dynamics models in O(n) time with LSTM networks

[Zotero 条目 DJRBHBIA](zotero://select/library/items/DJRBHBIA)

[DOI 原文](https://doi.org/10.1109/humanoids.2017.8246965)

[来源网页](https://ieeexplore.ieee.org/document/8246965)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Planning & Inverse Control/索引|05 Robot Learning/Planning & Inverse Control]]

概念地图：[[Zotero Knowledge/Concepts/动作接口与逆动力学|动作接口与逆动力学]]

## 原始摘要

Inverse dynamics model learning is crucial for modern robots where analytic models cannot capture the complex dynamics of compliant actuators, elasticities, mechanical inaccuracies, frictional effects or sensor noise. However, such models are highly nonlinear and millions of samples are needed to encode a large number of motor skills. Thus, current state of the art model learning approaches like Gaussian Processes which scale exponentially with the data cannot be applied. In this work, we developed an inverse dynamics model learning approach based on a long-short-term-memory (LSTM) network with a time complexity of O(n). We evaluated the approach on a KUKA robot arm that was used in object manipulation skills with various loads. In a comparison to Gaussian Processes we show that LSTM networks achieve better prediction performances and that they can be trained on large datasets with more than 100,000 samples in a few seconds. Moreover, due to the small training batch size of for example 128 samples, the network can be continuously improved in life-long learning scenarios.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### 06/02/2026, 20:54:58

[在 Zotero 查看](zotero://select/library/items/ZWLZKXIR)

**06/02/2026, 20:54:58**

**gpt-5-chat-latest:**

Here’s a comprehensive analysis and summary of the paper **“Learning inverse dynamics models in O(n) time with LSTM networks”** (Rueckert et al., 2017), focusing on its **core innovations, motivations, reasoning, achievements**, and **relevance to your 2026 world model application**.

### **Core Innovations**

#### 1. **Problem Addressed**

The paper tackles the challenge of learning **inverse dynamics models** for modern robots, i.e., predicting joint torques ($\tau$) given joint states (positions, velocities, accelerations).  
Traditional analytic models often fail due to:

- Compliant and elastic actuators,

- Mechanical inaccuracies,

- Frictional effects and sensor noise,

- Complex unmodeled dynamics (contacts, vibrations, etc.).

Learning these models is crucial for **model-based control**, **planning**, and **manipulation**, but data volumes (millions of samples) make existing methods computationally infeasible.

#### 2. **Motivation**

State-of-the-art regression-based model learning methods like **Gaussian Processes (GPs)** are effective but scale poorly:

- **GPs:** $O(n^3)$ for kernel inversion; even sparse/local approximations are $O(n^2)$.

- Hence, impractical for large-scale or lifelong learning scenarios in robotics.

The authors sought a solution that scales **linearly (O(n))** with data size — enabling both online and lifelong learning on real robots.

#### 3. **Core Method**

They proposed a **Long Short-Term Memory (LSTM)-based inverse dynamics model**.  
Motivations for why they expected it to work:

- **Temporal Correlation Exploitation:**

  Real robot trajectories are sequential, and LSTMs can exploit temporal dependencies (unlike GPs).

- **Memory and Robustness to Noise:**

  The gating and cell-state mechanisms in LSTMs prevent vanishing gradients and integrate long-term dependencies—advantageous in noisy, sequential motion data.

- **Scalability:**

  LSTMs can be trained with small batch sizes and incremental updates, providing **O(n)** scalability with respect to data size.

Their theoretical foundation:  

$$\tau = M(q)\ddot q + h(q, \dot q) + \epsilon(q, \dot q, \ddot q)$$

They learn $f(x)$ mapping $x = [q, \dot q, \ddot q]$ → $\tau$ using LSTM regression.

### **Experimental Achievements**

- **Benchmarks:**

- Synthetic dataset (sine, triangle, sawtooth functions) with varying Gaussian noise.

- Real KUKA robot arm experiments (predicting joint torques while pushing flasks filled with varying liquid levels).

- **Findings:**

- **Better noise robustness:** LSTMs achieved lower MSE than GPs even under high noise.

- **Temporal advantage:** When data temporal order was shuffled, LSTM’s performance dropped—but GP’s didn’t—showing LSTM’s beneficial exploitation of temporal structure.

- **Scalability:**

- GP training: ~25 hours for 10k samples.

- LSTM training: ~28 sec for 10k samples.

- LSTM scales linearly (O(n)); GP scales cubically (O(n³)).

- **Performance:**

- Prediction error decreased exponentially with more data.

- Eventually outperformed GPs for large datasets (>1000 samples).

- Real-time feasible: 282 seconds for 112,761 samples on a desktop PC.

- **Limitations Noted:**

- No built-in output variance estimate (uncertainty).

     The authors suggested extending with Bayesian or dropout-based uncertainty modeling ([Gal & Ghahramani, 2016]).

### **Expected Mechanistic Rationale**

They expected LSTM-based inverse dynamics learning to work because:

- The robot’s **temporal transitions** (action → next state) are structured sequentially.

- LSTM’s recurrent memory **captures causality** across time, unlike static regression.

- Nonlinearities and noise could be absorbed in hidden recurrent representations.

- Linearity in training computation makes it practical for **lifelong, high-dimensional robotic learning**.

### **Relation to World Model Development (2026)**

You’re exploring **action-conditioned world models**, where:

- The **world model** generates state transitions and action sequences.

- Overfitting occurs when generated actions mimic training data too rigidly.

- You wish to **extract inverse dynamics relations** to cross-examine generated actions against desired ones.

#### 1. **How this paper’s idea could help**

This paper’s approach offers a **data-efficient and temporally grounded inverse model** (mapping from state trajectories to actions). In your case:

- **Inverse Dynamics Regularization:**

  You could train an LSTM-based inverse model on physical robot or simulation data to infer action sequences from generated world-model rollouts.

- **Cross-Consistency Check:**

  Compare model-generated actions with those predicted by the inverse model, enforcing physical and temporal consistency.

- **Noise Robustness:**

  Helps counter overfitting in world models by learning realistic action-state couplings even under stochastic noise.

- **Scalability:**

  Makes sense for large generative datasets — its O(n) complexity fits modern large-scale reinforcement learning and simulation regimes.

#### 2. **Is it outdated in 2026?**

Not *conceptually*. The core insight — using **sequence-aware, scalable inverse models** to maintain physical consistency — remains highly relevant.

However, the technique (LSTM-based) is **technically superseded** by more advanced architectures:

- **Transformers and diffusion models** (more flexible than LSTMs in long-horizon temporal modeling);

- **Neural ODEs / Physics-informed networks** for continuous-time dynamics;

- **Hybrid world models** (e.g., DreamerV3, Pla, UniSim, PhysDiff, 2023–2026) that integrate stochastic recurrent latent state dynamics and physics priors.

Yet, the **conceptual role of inverse dynamics learning** in constraining generative world models is *still foundational* — only the model class (LSTM) is outdated.

### **Summary Table**

 | Aspect | Description | Modern Relevance

 | **Innovation** | Linear-time inverse dynamics learning with LSTM | Concept still valid

 | **Motivation** | Handle complex robot dynamics, large-scale data infeasibility of GPs | Still applicable in data-heavy world model training

 | **Expected Benefit** | Use memory to exploit temporal correlations and scale efficiently | Temporal structure crucial for world models

 | **Achievement** | 100k+ samples trained in O(n), outperforming GPs | Excellent computational benchmark

 | **Limitations** | No uncertainty estimation, limited to LSTMs | Replace with modern stochastic sequence models

 | **Use in 2026** | Good reference for grounding generated action sequences via inverse modeling | Should be implemented with newer architectures

### **Final Takeaway for Your Use Case**

You can **extract the conceptual and methodological essence** of this paper:

- Treat inverse dynamics learning as a **validator and regularizer** for your world model’s generated actions.

- Use a modern **transformer-based or stochastic recurrent inverse model** (instead of LSTM).

- Keep the paper as a **foundational reference** for the idea of scalable inverse dynamics integration in learning-based world modeling — but **not as the latest algorithmic reference**.

**In short:**  
✔ Use the idea — inverse dynamics as cross-checking mechanism.  
✖ Do not use vanilla LSTM implementation; upgrade to transformer or physics-informed recurrent models.

Written by AIdea plugin

**06/02/2026, 20:54:59**

**gpt-5-chat-latest:**

Here’s a comprehensive analysis and summary of the paper **“Learning inverse dynamics models in O(n) time with LSTM networks”** (Rueckert et al., 2017), focusing on its **core innovations, motivations, reasoning, achievements**, and **relevance to your 2026 world model application**.

### **Core Innovations**

#### 1. **Problem Addressed**

The paper tackles the challenge of learning **inverse dynamics models** for modern robots, i.e., predicting joint torques ($\tau$) given joint states (positions, velocities, accelerations).  
Traditional analytic models often fail due to:

- Compliant and elastic actuators,

- Mechanical inaccuracies,

- Frictional effects and sensor noise,

- Complex unmodeled dynamics (contacts, vibrations, etc.).

Learning these models is crucial for **model-based control**, **planning**, and **manipulation**, but data volumes (millions of samples) make existing methods computationally infeasible.

#### 2. **Motivation**

State-of-the-art regression-based model learning methods like **Gaussian Processes (GPs)** are effective but scale poorly:

- **GPs:** $O(n^3)$ for kernel inversion; even sparse/local approximations are $O(n^2)$.

- Hence, impractical for large-scale or lifelong learning scenarios in robotics.

The authors sought a solution that scales **linearly (O(n))** with data size — enabling both online and lifelong learning on real robots.

#### 3. **Core Method**

They proposed a **Long Short-Term Memory (LSTM)-based inverse dynamics model**.  
Motivations for why they expected it to work:

- **Temporal Correlation Exploitation:**

  Real robot trajectories are sequential, and LSTMs can exploit temporal dependencies (unlike GPs).

- **Memory and Robustness to Noise:**

  The gating and cell-state mechanisms in LSTMs prevent vanishing gradients and integrate long-term dependencies—advantageous in noisy, sequential motion data.

- **Scalability:**

  LSTMs can be trained with small batch sizes and incremental updates, providing **O(n)** scalability with respect to data size.

Their theoretical foundation:  

$$\tau = M(q)\ddot q + h(q, \dot q) + \epsilon(q, \dot q, \ddot q)$$

They learn $f(x)$ mapping $x = [q, \dot q, \ddot q]$ → $\tau$ using LSTM regression.

### **Experimental Achievements**

- **Benchmarks:**

- Synthetic dataset (sine, triangle, sawtooth functions) with varying Gaussian noise.

- Real KUKA robot arm experiments (predicting joint torques while pushing flasks filled with varying liquid levels).

- **Findings:**

- **Better noise robustness:** LSTMs achieved lower MSE than GPs even under high noise.

- **Temporal advantage:** When data temporal order was shuffled, LSTM’s performance dropped—but GP’s didn’t—showing LSTM’s beneficial exploitation of temporal structure.

- **Scalability:**

- GP training: ~25 hours for 10k samples.

- LSTM training: ~28 sec for 10k samples.

- LSTM scales linearly (O(n)); GP scales cubically (O(n³)).

- **Performance:**

- Prediction error decreased exponentially with more data.

- Eventually outperformed GPs for large datasets (>1000 samples).

- Real-time feasible: 282 seconds for 112,761 samples on a desktop PC.

- **Limitations Noted:**

- No built-in output variance estimate (uncertainty).

     The authors suggested extending with Bayesian or dropout-based uncertainty modeling ([Gal & Ghahramani, 2016]).

### **Expected Mechanistic Rationale**

They expected LSTM-based inverse dynamics learning to work because:

- The robot’s **temporal transitions** (action → next state) are structured sequentially.

- LSTM’s recurrent memory **captures causality** across time, unlike static regression.

- Nonlinearities and noise could be absorbed in hidden recurrent representations.

- Linearity in training computation makes it practical for **lifelong, high-dimensional robotic learning**.

### **Relation to World Model Development (2026)**

You’re exploring **action-conditioned world models**, where:

- The **world model** generates state transitions and action sequences.

- Overfitting occurs when generated actions mimic training data too rigidly.

- You wish to **extract inverse dynamics relations** to cross-examine generated actions against desired ones.

#### 1. **How this paper’s idea could help**

This paper’s approach offers a **data-efficient and temporally grounded inverse model** (mapping from state trajectories to actions). In your case:

- **Inverse Dynamics Regularization:**

  You could train an LSTM-based inverse model on physical robot or simulation data to infer action sequences from generated world-model rollouts.

- **Cross-Consistency Check:**

  Compare model-generated actions with those predicted by the inverse model, enforcing physical and temporal consistency.

- **Noise Robustness:**

  Helps counter overfitting in world models by learning realistic action-state couplings even under stochastic noise.

- **Scalability:**

  Makes sense for large generative datasets — its O(n) complexity fits modern large-scale reinforcement learning and simulation regimes.

#### 2. **Is it outdated in 2026?**

Not *conceptually*. The core insight — using **sequence-aware, scalable inverse models** to maintain physical consistency — remains highly relevant.

However, the technique (LSTM-based) is **technically superseded** by more advanced architectures:

- **Transformers and diffusion models** (more flexible than LSTMs in long-horizon temporal modeling);

- **Neural ODEs / Physics-informed networks** for continuous-time dynamics;

- **Hybrid world models** (e.g., DreamerV3, Pla, UniSim, PhysDiff, 2023–2026) that integrate stochastic recurrent latent state dynamics and physics priors.

Yet, the **conceptual role of inverse dynamics learning** in constraining generative world models is *still foundational* — only the model class (LSTM) is outdated.

### **Summary Table**

 | Aspect | Description | Modern Relevance

 | **Innovation** | Linear-time inverse dynamics learning with LSTM | Concept still valid

 | **Motivation** | Handle complex robot dynamics, large-scale data infeasibility of GPs | Still applicable in data-heavy world model training

 | **Expected Benefit** | Use memory to exploit temporal correlations and scale efficiently | Temporal structure crucial for world models

 | **Achievement** | 100k+ samples trained in O(n), outperforming GPs | Excellent computational benchmark

 | **Limitations** | No uncertainty estimation, limited to LSTMs | Replace with modern stochastic sequence models

 | **Use in 2026** | Good reference for grounding generated action sequences via inverse modeling | Should be implemented with newer architectures

### **Final Takeaway for Your Use Case**

You can **extract the conceptual and methodological essence** of this paper:

- Treat inverse dynamics learning as a **validator and regularizer** for your world model’s generated actions.

- Use a modern **transformer-based or stochastic recurrent inverse model** (instead of LSTM).

- Keep the paper as a **foundational reference** for the idea of scalable inverse dynamics integration in learning-based world modeling — but **not as the latest algorithmic reference**.

**In short:**  
✔ Use the idea — inverse dynamics as cross-checking mechanism.  
✖ Do not use vanilla LSTM implementation; upgrade to transformer or physics-informed recurrent models.

Written by AIdea plugin

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/S5Q4GIU4)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/I6TQE4K6)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-MDBK7VBT - Predictive Inverse Dynamics Models are Scalable Learners for Robotic Manipulation|Predictive Inverse Dynamics Models are Scalable Learners for Robotic Manipulation]] — 中关联；共同研究内容：基准与数据合成、语言模型与语言表征、逆动力学与潜在动作。

<!-- content-relations:end -->
