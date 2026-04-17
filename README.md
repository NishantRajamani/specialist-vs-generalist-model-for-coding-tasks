# 🧠 Multi-Model vs Single LLM for Code Generation

This project compares a **modular multi-model pipeline** against a **single large language model** for solving competitive programming problems.

## 🚀 Approach

### 🔹 Single Model (Baseline)
A large model handles:
- reasoning
- problem solving
- code generation  

Example: `Qwen2.5-Coder-14B (GGUF via llama.cpp)`

---

### 🔹 Multi-Model Pipeline
Problem → Reasoning Model → Plan → Coder Model → Code


- **Reasoning model**: breaks down the problem and generates a plan  
- **Coder model**: converts the plan into executable code  

---

## ⚙️ Setup

- Apple Silicon (M-series Mac)
- `llama-cpp-python` (GGUF models with Metal acceleration)
- Local inference (no API usage)

---

## 📊 Evaluation

- Tasks: Competitive programming problems  
- Metrics:
  - `pass@1` (single attempt)
  - `pass@5` (best of multiple attempts)

### Generation Strategy
- Low temperature (`0.1–0.2`) → pass@1  
- Higher temperature (`0.6–0.7`) → pass@5  

---

## 🧠 Key Idea

> Can separating reasoning and coding across smaller models match or outperform a single larger model?

---

## 👨‍💻 Author

Nishant Rajamani  
MSc Applied Data Science, Utrecht University
