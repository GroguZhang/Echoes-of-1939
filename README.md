# Echoes-of-1939
A RAG-Driven Computational Musicology Agent for the Yellow River Cantata
# Echoes of 1939: A RAG-Driven Computational Musicology Agent 🌊

> An interdisciplinary AI agent that bridges computational musicology, Retrieval-Augmented Generation (RAG), and constructivist pedagogy to provide an immersive, multimodal learning experience for the *Yellow River Cantata*.

## 📌 Project Overview
In traditional music appreciation education, teaching macro-historical vocal suites often faces significant pain points: lack of emotional resonance, high barriers to professional musical terminology (e.g., Canon, Ostinato), and weak individualized interactive feedback. 

**"Echoes of 1939"** solves this by breaking the traditional "one-way instillation" model. By deeply simulating the persona of the original composer, Xian Xinghai, this AI agent creates a cross-temporal, first-person dialogue. It seamlessly integrates music theory, historical context, and emotional values, transforming users from passive listeners into active explorers.

## ⚙️ System Architecture
The agent is designed using a modular architecture, separating the orchestration layer, retrieval engine, and client interface.

```text
[User Input] 
   │
   ▼
[Intent Router (State Machine)] ──► State 1: New Movement Request
   │                                  ├──► Trigger Python Workflow (asymmetric_card_generator.py)
   │                                  └──► Return Rich Media Card + Hidden Question
   │
   ├──► State 2: Deep Exploration (Locked Mode)
   │      ├──► Semantic Query Generation
   │      ├──► [Vector Database] ◄── Retrieve ── [Chunked Musicology Corpus]
   │      └──► LLM Synthesis (Persona: Xian Xinghai) + Pedagogical Prompting
   │
   └──► State 3: Knowledge Summarization
          └──► Extract JSON Context ──► Trigger TreeMind Plugin ──► Return Mind Map
