# 🧠 Multi-Model vs Single LLM for Code Generation

This project compares a **modular multi-model pipeline** against a **single large language model** for solving competitive programming problems using a subset of problems from LiveCodeBench and APPS dataset.

## 🚀 Approach

### 🔹 Single Model (Baseline)
A large model handles:
- reasoning
- problem solving
- code generation  

Example: `Qwen2.5-Coder-14B`

---

### 🔹 Multi-Model Pipeline
Problem → Reasoning Model → Plan → Coder Model → Code


- **Reasoning model**: decomposes the problem and generates a plan  
- **Coder model**: converts the plan into executable code  

---

## ⚙️ Setup
Not much do to :) just run the notebook on (preferably powerful) GPU

- NVIDIA GPU (CUDA-enabled)
- HuggingFace Transformers / vLLM
- Local inference

---

## 📊 Evaluation

- Tasks: Competitive programming problems  
- Metrics:
  - `pass@1`
  - `pass@5`

### Generation Strategy
- Low temperature (`0.1–0.2`) → pass@1  
- Higher temperature (`0.6–0.7`) → pass@5  

---

## 🧠 Key Idea

> Can structured reasoning across smaller models compete with a single larger model?
