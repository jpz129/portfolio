---
title: "Voicecraft"
description: "A modular, streaming AI framework that iteratively plans, revises, critiques, and refines your drafts with transparent, step-by-step feedback."
publishDate: 2025-05-12
tags: ["FastAPI", "LangGraph", "LangChain", "Hugging Face", "Streamlit"]
repo: "https://github.com/jpz129/voicecraft"
demoUrl: "http://127.0.0.1:8000/docs"
img: "/assets/projects/voicecraft.png"
img_alt: "Screenshot of Voicecraft streaming revision UI"
---

### 📖 The Story

I’ve always believed that great writing comes from relentless refinement—draft, critique, revise, repeat. But most tools treat your draft as a black box: you send text in, get text out, and wonder what happened in between.

Enter **Voicecraft**. Inspired by agentic workflows and chain-of-thought transparency, I set out to build a system that:

- Streams every thought—plans, revisions, critiques, and decisions—so you see exactly how your draft transforms.
- With modular nodes for planning, revising, critiquing, and looping decisions, Voicecraft guides your prose through up to three refinement cycles, all under your control.

---

### 🧠 What It Does

Submit your draft, and Voicecraft:

1. Classifies intent (plan a rewrite vs. answer a specific question)
2. Generates a clear revision plan
3. Revises the text per that plan
4. Critiques the new draft for further improvements
5. Decides whether another cycle is needed (looping up to your cap)
6. Streams each step as JSON lines to FastAPI clients—perfect for real-time UIs

---

### ✍️ Quick Example

**You send:**

```text
Our product launch was a success, but users want clearer feature explanations.
```

**You receive streamed outputs:**

- 📝 **Plan:** “Focus on concise language, highlight key benefits, and address feedback points.”
- ✍️ **Revise:** “Our product launch soared, yet users ask for clearer feature explanations.”
- 🧐 **Critique:** “Make bullet points for benefits.”
- 🔄 **Decision:** “Another cycle needed.”
- …(second loop)…
- ✅ **Final Draft:** “Our launch exceeded expectations. Users praise speed but request clearer benefit breakdowns—here’s an improved summary.”

Each step appears as a discrete “Step” in Chainlit or as a chat message in Streamlit.

---

### ⚙️ How It Works (for the tech-curious)

- **FastAPI** serves a `/stream` endpoint for JSON-line streaming
- **LangGraph** defines a state machine with nodes for intent, plan, revise, critique, and decision
- **LangChain** and **Pydantic** ensure prompts are structured and outputs validated
- **Hugging Face Inference** powers the LLM calls (configurable via `HF_ENDPOINT_URL`)
- **Streamlit** front-end demos live streaming of each node
- **Docker** & **Uvicorn** for local development and production readiness
- **Open Source**: Every component—backend, workflow logic, and frontends—is fully open source, so you can inspect, extend, or self-host any part of the system.

---

### 🔗 Links

- 🐙 [GitHub Repository](https://github.com/jpz129/voicecraft)
