# Causal-Aware LLM Agents for PHM Co-Pilots  
**Health Monitoring and Intervention Planning**  

## 📄 Overview  
This repository accompanies the paper:  
**"Causal-Aware LLM Agents for PHM Co-Pilots: Health Monitoring and Intervention Planning"** (PHM Society Annual Conference, 2025).  

The paper introduces a **proof-of-concept PHM Copilot** that integrates:  
- **Large Language Models (LLMs)** for reasoning and plan generation  
- **Causal Inference frameworks** for robust decision-making  
- **Retrieval-Augmented Generation (RAG)** for context grounding  
- **Evaluator modules** to validate LLM actions with counterfactual simulation  

This approach demonstrates how **localized causal reasoning** can address limitations of standard LLM + RAG pipelines in high-stakes maintenance scenarios.

---

## 🧩 System Components
1. **Sensor Trigger Inference**  
   - Identifies derived events from multivariate sensor streams.  

2. **Top-k Historical Retrieval**  
   - Matches similar operational states using FAISS-based nearest neighbor search.  

3. **Localized Causal Graph**  
   - Constructs a graph-of-triggers to enable interpretable causal reasoning.  

4. **Recommender Module**  
   - Generates candidate diagnostic and corrective action plans.  
   - Uses **DR-Learner** for causal effect estimation (ATE, ITE).  

5. **Evaluator Module**  
   - Performs counterfactual reasoning on historical data.  
   - Validates recommender output against injected synthetic counterfactuals.  

---

## 📊 Key Results  
- **Recommender Effectiveness (Mean ATE)**: LLM-generated actions generally improved outcomes.  
- **ATE Lift Over Control**: Demonstrated competitive advantage over historical baselines.  
- **Policy Value Estimation**: Higher policy value compared to control strategies.  
- **ATE Agreement with Injection**: High internal consistency (> 90%).  

---

## 🚀 Future Directions  
- Multi-step intervention modeling with **Structural Causal Models (SCMs)**.  
- Scaling retrieval from **localized top-k** to **global embedding search**.  
- Integrating **symbolic causal reasoning** into LLM prompts.  
- Benchmarking on **synthetic + real-world PHM datasets**.  

---

