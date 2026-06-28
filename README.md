# AI Governance, Security & Production Practices

This repository is a structured knowledge base covering the critical aspects of building **safe, reliable, and production-ready AI systems**. As LLM-powered applications move from prototypes to real-world deployments, engineering them responsibly becomes just as important as engineering them correctly.

The focus here is not on building AI models from scratch — it's on understanding what happens **after** you have a model: how do you secure it, evaluate it, make it remember context intelligently, and observe its behavior in production?

---

## What's Inside

### 🛡️ LLM Guardrails
Security is not optional in production AI systems. This section covers how to protect LLM-based applications from threats like prompt injection, jailbreaking, sensitive topic leakage, and unintended outputs.

Key concepts include:
- **Input Guardrails** — Classifying and filtering user queries before they reach the model
- **Output Guardrails** — Sanitizing and validating model responses before they reach the user
- Frameworks like **NeMo Guardrails** (NVIDIA), **Guardrails AI**, **LLaMA Guard**, and **AWS Bedrock Guardrails**

---

### 🧪 LLM Evals
You can't improve what you don't measure. This section treats evaluation not as a simple metric, but as a **complete testing discipline** for LLM-powered systems.

Key concepts include:
- What makes an eval systematic and repeatable
- Defining clear criteria for what "good" means
- Evaluating RAG pipelines, agent task completion, safety, and factual accuracy
- The difference between model evals and application evals
- Designing eval workflows that answer real engineering questions — *"Is this system good enough to ship?"*

---

### 🧠 Agentic Memory
LLMs are stateless by nature. In agentic systems, memory is what gives an agent the ability to maintain context, reason over past interactions, and behave consistently over time.

Key concepts include:
- **Conversation Buffer Memory** — Storing raw interaction history (and its token cost implications)
- **Sliding Window Memory** — Keeping only the most recent N turns to control context size
- **Summary Memory** — Compressing older conversations into a running summary
- **Summary Buffer Memory** — A hybrid approach balancing recency with compression

---

## Purpose

This is a **learning and reference repository** — built to deeply understand the engineering layer that sits between a raw LLM and a trustworthy, production-grade AI application. Each folder contains notes, breakdowns, and conceptual explanations grounded in real frameworks and research.

> More sections will be added as the scope expands.
