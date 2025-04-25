---
title: "Story Prose Generator"
description: "Create strong, immersive prose for your stories with AI-powered clarity and style."
publishDate: 2025-04-24
tags: ["FastAPI", "LangChain", "Claude", "spaCy", "Docker", "Cloud Run", "Gradio"]
repo: "https://github.com/jpz129/story-prose-generator"
demoUrl: "https://story-prose-generator-415817045199.us-central1.run.app/docs"
img: "/assets/projects/beats.png"
img_alt: "Screenshot of the story prose generator interface"
---

### 📖 The Story

I poured everything I had into this one. Preparing for the Sudowrite interview didn’t feel like any routine coding test, it was closer to stepping into the audition for a life I hadn’t even realized I’d wanted. A life where I could spend my time tinkering at the crossroads of story and machine. I stayed up late, pushing past the edges of the requirements. In truth, I already saw myself among them.

That was the mistake, and I see it now. I’d told myself the job was already mine.

So when the rejection came, the sting was sharp. Not only because they said no, but because I’d already said yes. 

But I didn’t shut the lid on the project folder. I kept going.

This was never just an interview assignment. It was the kind of thing I’d be making anyway. Maybe for the stubborn souls determined to build instead of buy, or for anyone eager to see story and AI pull at each other like two kids on a rope swing. Maybe there’s a little bitterness left. But I meant to create something that could translate a handful of narrative beats into prose that lives, that breathes, that feels. I wanted to build a system that would meet me where I am, as a writer, as a builder, as someone who believes that stories are for living, not just reading.

Disappointment, when you sit with it, can be shaped into purpose. This is what I made, and I’m glad I didn’t stop.

---

### 🧠 What It Does

Feed it story beats and metadata: setting, genre, characters. It:

1. Sends the setup to an LLM (Claude 3.7 Sonnet)
2. Returns a full, vivid story section
3. Runs checks for coherence and style

---

### 🧪 Try It Yourself

<script
  type="module"
  src="https://gradio.s3-us-west-2.amazonaws.com/5.26.0/gradio.js"
></script>

<gradio-app src="https://jpz129-story-prose-generator.hf.space"></gradio-app>

---

### ⚙️ How It Works (for the tech-curious)

- **FastAPI** runs the engine
- **LangChain** gives it memory and spine
- **Claude 3.7 Sonnet** writes the prose
- **spaCy** checks grammar and style
- **Docker** keeps it portable
- **Google Cloud Run** handles deployment
- **Gradio** powers the frontend

Real AI. Real tools. All for real storytelling.

---

### 🔗 Links

- 🐙 [GitHub Repository](https://github.com/jpz129/story-prose-generator)
- 📘 [API Documentation](https://story-prose-generator-415817045199.us-central1.run.app/docs)