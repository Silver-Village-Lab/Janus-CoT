# 1.0
This is the homepage for showcasing Janus-CoT.
<div align="center">

<h1>Janus-CoT: A Reasoning Framework Based on Bidirectional Multimodal Chain of Thought with Fusion Nodes</h1>


<p align="center">
  <a href="https://huggingface.co/your-org/Janus-CoT"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Models-yellow?style=flat-square"></a>
  <a href="https://github.com/Silver-Village-Lab/Janus-CoT"><img src="https://img.shields.io/badge/Project-Page-blue?style=flat-square"></a>
  <a href="https://github.com/Silver-Village-Lab/Janus-CoT/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-Apache%202.0-green.svg?style=flat-square"></a>
</p>

</div>

---

## 🔥 News
* [cite_start]**[2026/04/18]** 🚀 We released the training and inference code for **Janus-CoT**. 
* [cite_start]**[2026/04/18]** 📚 We released the **BR1** dataset (18,000 samples of 8-node sequences with paired forward and reverse CoT paths). 
* **[2026/04/18]** 📄 The paper has been submitted to IEEE Transactions on Emerging Topics in Computing.

---

## 📖 Abstract

[cite_start]Multimodal reasoning presents a fundamental challenge in embodied intelligence. [cite_start]While Multimodal Large Language Models (MLLMs) have advanced the field, existing approaches predominantly rely on unidirectional Chain of Thought (CoT) reasoning, which frequently suffers from error accumulation and modality misalignment due to a lack of global causal foresight. 

[cite_start]To address this limitation, we present **Janus-CoT**, a novel closed-loop reasoning paradigm featuring:
1.  [cite_start]**Bidirectional Reasoning:** A dual-stream architecture coupling a **Forward Deductive Stream** for task decomposition with a **Reverse Abductive Stream** that performs goal-directed verification to proactively detect contradictions.
2.  [cite_start]**Dynamic Fusion Nodes:** These nodes act as stage-wise multimodal memory anchors to synchronize and physically ground the parallel reasoning streams in a strict (Text, Image, Audio) representation.
3.  [cite_start]**Encoder-Free Architecture:** A lightweight multimodal alignment mechanism that achieves latency comparable to single-chain models by directly projecting sensory signals into the semantic space.

[cite_start]Extensive evaluations on **OmniBench**, **UNO-Bench**, and diverse embodied reasoning tasks (BridgeData V2, RoboVQA, HoloAssist, AV) demonstrate that Janus-CoT achieves state-of-the-art performance.

---

## 🏗️ Architecture

<div align="center">
  <img src="assets/architecture.png" width="95%" alt="Janus-CoT Architecture"/>
</div>

> [cite_start]**Overview of Janus-CoT:** The system processes multimodal input through a bidirectional CoT comprising a forward CoT and a reverse CoT. [cite_start]Triggered by a synchronized decision mechanism, critical states from both streams are progressively condensed into fusion nodes. 

---

## ⚡ Quick Start

### Installation

```bash
git clone [https://github.com/Silver-Village-Lab/Janus-CoT.git](https://github.com/Silver-Village-Lab/Janus-CoT.git)
cd Janus-CoT
conda create -n januscot python=3.10
conda activate januscot
pip install -r requirements.txt
