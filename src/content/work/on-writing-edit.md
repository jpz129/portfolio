---
title: "Revise Like King"
description: "An AI-powered revision engine that cuts the fat and sharpens your prose using the tough-love rules from Stephen King's 'On Writing.'"
publishDate: 2025-04-25
tags: ["FastAPI", "LangChain", "OpenAI", "Cloud Run", "Pinecone"]
repo: "https://github.com/jpz129/revise-like-king"
demoUrl: "https://on-writing-app-2352728448.us-central1.run.app/docs"
img: "/assets/projects/revise-like-king.png"
img_alt: "Screenshot of the revision API interface"
---

### 📖 The Story

I used to think good writing meant getting it perfect on the first try.  
Then I read *On Writing* by Stephen King and I lost a lot of sleep.

King didn’t bother pretending. Writing starts messy and honest. Characters surface as you go writing the all important story. 

That set me free to write raw, real, with the power to write what I know.   
And it gave me an idea:

> *What if Stephen King could help revise my ugly first drafts?*

So I built **Revise Like King**, a tool that greets you after you’ve wrestled with the rumble of honesty on the page. It makes you feel excited to be the first reader of your work.

---

### 🧠 What It Does

Send it some writing. Behind the curtain, it:

1. **Reads** for sense and style
2. **Hunts** *On Writing* for blunt, battle-tested advice
3. **Builds** a revision prompt tailored to what your draft needs
4. **Returns** a tighter version with your voice, just, better (sorry)

---

### ✍️ Quick Example

**You send:**
```json
{
  "text": "Ben opened the door and immediately knew he was in trouble."
}
```

**You get back:**
```text
Ben opened the door. Trouble waited on the other side, thick in the air and quiet as regret.
```

Juicy! Still yours.

---

### 🧪 Try It Yourself

<script
	type="module"
	src="https://gradio.s3-us-west-2.amazonaws.com/5.26.0/gradio.js"
></script>

<gradio-app src="https://jpz129-on-writing-edit.hf.space"></gradio-app>

---

### ⚙️ How It Works (for the tech-curious)

*(If you’re just here for the magic, class dismissed.)*

- **FastAPI** runs the core engine
- **LangChain** builds smart prompts, fetches fitting advice
- **Pinecone** holds a semantic index of *On Writing*
- **OpenAI GPT-4** does the heavy lifting
- **Docker** keeps it clean
- **Google Cloud Run** handles deployment
- **Gradio** powers the instant demo

Real AI. Real engineering. None of it gets in the way of real writing.

---

### 🔗 Links

- 🐙 [GitHub Repository](https://github.com/jpz129/revise-like-king)
- 📘 [API Documentation](https://on-writing-app-2352728448.us-central1.run.app/docs)