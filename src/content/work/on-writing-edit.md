---
title: "Revise Like King"
description: "An AI-powered revision engine that rewrites your prose using principles from Stephen King's 'On Writing'."
publishDate: 2025-04-25
tags: ["FastAPI", "LangChain", "OpenAI", "Cloud Run", "Pinecone"]
repo: "https://github.com/jpz129/revise-like-king"
demoUrl: "https://on-writing-app-2352728448.us-central1.run.app/docs"
img: "/assets/projects/revise-like-king.png"
img_alt: "Screenshot of the revision API interface"
---

### 📖 The Story

This project was born out of a simple question: what if Stephen King could revise your writing?

I wanted to build a tool that doesn’t just generate text — it *revises* yours. Not a toy, but a trustworthy editor. Something that could meet you halfway — with memory, taste, and humility.

So I taught GPT-4 to think like King. I embedded *On Writing* into Pinecone, used LangChain to retrieve semantic advice, and wired it all together with FastAPI and Cloud Run.

This wasn’t a playground. It was a fully productionalized, containerized, and deployable LLM application that treats your input with the respect good writing deserves.

---

### 🧠 What It Does

You send it a passage of text. The system:

1. Semantically analyzes the passage
2. Queries a Pinecone index of *On Writing* for relevant advice
3. Constructs a revision prompt using GPT-4
4. Returns a new version of your text — clearer, tighter, and more King-like

---

### 🧪 Example Request

```json
{
  "text": "Ben opened the door and immediately knew he was in trouble."
}
```

---

### ✍️ Example Revision

```text
Ben opened the door. Trouble was waiting on the other side, thick in the air and silent as regret.
```

---

### 🧪 Try It Yourself

<script
	type="module"
	src="https://gradio.s3-us-west-2.amazonaws.com/5.26.0/gradio.js"
></script>

<gradio-app src="https://jpz129-on-writing-edit.hf.space"></gradio-app>


---

### ⚙️ Tech Stack

- **FastAPI** for routing and API logic
- **LangChain** for prompt orchestration and semantic retrieval
- **OpenAI GPT-4** for revision generation
- **Pinecone** for semantic document search
- **Docker** for containerization
- **Google Cloud Run** for deployment
- **Gradio** for the demo frontend

---

### 🔗 Links

- 🐙 [GitHub Repository](https://github.com/jpz129/revise-like-king)
- 📘 [API Documentation](https://on-writing-app-2352728448.us-central1.run.app/docs)
