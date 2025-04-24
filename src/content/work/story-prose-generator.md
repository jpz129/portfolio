---  
title: "Story Prose Generator"  
description: "A generative prose engine born from rejection and built for storytelling with soul."  
publishDate: 2025-04-24  
tags: ["FastAPI", "LangChain", "Claude", "Cloud Run"]  
repo: "https://github.com/jpz129/story-prose-generator"  
demoUrl: "https://story-prose-generator-415817045199.us-central1.run.app/docs"  
img: "/assets/projects/beats.png"  
img_alt: "Screenshot of the prose generator endpoint"  
---  

### 📖 The Story

I put my heart into this one. When I was preparing for the Sudowrite interview, it didn’t feel like a typical coding test, it felt like an audition for the kind of life I didn't know I wanted to live. That in which I could spend my time building tools at the intersection of storytelling and AI. I stayed up late refining prompts. I built beyond the spec. I imagined myself already part of the team.

I made the mistake of thinking the job was mine.

So when the rejection came, it hit harder than I expected. Not because they didn’t choose me, but because I’d already said yes in my own mind. I’d brought my whole self into it.

But instead of closing the project folder, I kept going.

This wasn’t just an interview assignment. This was something I would’ve built anyway for someone if they wanted to, say, not pay for Sudowrite (maybe I'm a little bitter... jk, I swear!). I wanted to take a handful of narrative beats and turn them into immersive, emotionally intelligent prose. I wanted a system that could meet me where I am as a writer, a builder, and someone who believes that stories are meant to be formed and lived by humans like us.

That’s what this project is. *A way forward.* A way to turn disappointment into purpose, into something I’m proud to have made.

---  

### 🧠 What It Does  

You give it story beats and character or setting metadata. It sends that context to an LLM (Claude 3.7 Sonnet), then returns a complete story section with coherence and style evaluations baked in.  

---  

### 🧪 Example Request

```json
{
  "beats": [
    "A strange light appears in the sky",
    "The townspeople gather in awe",
    "A child reaches for it"
  ],
  "memory_strategy": "full",
  "enable_coherence_eval": false,
  "temperature": 0.85,
  "metadata": {
    "setting": "A sleepy mountain town in autumn",
    "genre": "Mystery",
    "style": "Dreamlike and atmospheric",
    "characters": [
      {
        "name": "Eli",
        "description": "A curious child drawn to the unknown"
      }
    ]
  },
  "metadata_threshold": 0.7
}
```

### 📖 Final Story

#### *A Whisper Above*

Eli paused at the edge of the pine forest, breath catching in his throat. The October air carried whispers of frost, but it wasn't the chill that made him stop.

Above the sleepy rooftops of Pinecrest, where smoke curled from chimneys like gentle questions, the evening sky had torn open. A light—not the amber glow of sunset or the silver of stars—but something altogether different, pulsed between layers of cloud. It shimmered with an impossible green-blue luminescence, like the northern lights had fallen and gotten caught in the mountain's embrace.

Eli's heart quickened. The light seemed to breathe, expanding and contracting with a rhythm that matched the wind through the autumn leaves. Something about it felt ancient, a secret written in a language the town had long forgotten but that Eli, somehow, could almost understand.

The townspeople of Pinecrest emerged from their homes like cautious deer, eyes lifted skyward. They gathered in driveways and street corners, conversation fading to reverent murmurs. Mrs. Walsh from the bakery stood beside Principal Harmon, their usual formalities dissolved by wonder. Children slipped from parental grasps to edge closer, their faces painted in that otherworldly glow.

Eli watched them all from his forest vantage, feeling oddly separate—as if he existed in the breath between the light's pulsations while everyone else remained firmly grounded. The strange radiance reflected in dozens of upturned faces, casting shadows that seemed to whisper secrets across weathered mountain features. Some pointed, others clasped hands, a few made hurried signs of protection learned from grandparents who'd known these mountains when the world was younger and wilder.

And still, the light breathed on.

In the gathered crowd, seven-year-old Mira Donovan broke free from her father's grasp. Something in that pulsing light called to her with the same irresistible pull that drew moths to flame. She raised her small hand skyward, fingers splayed against the darkening backdrop, as if she might catch the phenomenon like summer fireflies.

"I can touch it," she whispered, her voice carrying on the mountain air.

Eli watched, transfixed, as the luminescence seemed to respond—a tendril of azure-green light unfurling downward, reaching back toward Mira's outstretched hand. The crowd's collective breath caught, suspended in the space between wonder and fear. Parents lunged forward, but too late.

The light kissed Mira's fingertips, and for one heartbeat, the child's eyes reflected the same ancient knowledge that Eli felt stirring in his bones.

### 📥 Response (metadata)

```json
{
  "beat_evaluations": [
    {
      "beat_index": 1,
      "word_count": 139,
      "length_ok": true,
      "beat_coverage_score": 0.8493253588676453
    },
    {
      "beat_index": 2,
      "word_count": 139,
      "length_ok": true,
      "beat_coverage_score": 0.7417855858802795
    },
    {
      "beat_index": 3,
      "word_count": 134,
      "length_ok": true,
      "beat_coverage_score": 0.8206523060798645
    }
  ],
  "coherence_evaluations": null,
  "metadata_evaluations": [
    {
      "beat_index": 1,
      "metadata_similarity": 0.8828220367431641,
      "metadata_evaluation": "Good (spaCy similarity: 0.88)",
      "passes": true
    },
    {
      "beat_index": 2,
      "metadata_similarity": 0.8769888281822205,
      "metadata_evaluation": "Good (spaCy similarity: 0.88)",
      "passes": true
    },
    {
      "beat_index": 3,
      "metadata_similarity": 0.8716734051704407,
      "metadata_evaluation": "Good (spaCy similarity: 0.87)",
      "passes": true
    }
  ]
}
```

---  

### 🧪 Try It Yourself

<iframe 
  src="https://huggingface.co/spaces/jpz129/story-prose-generator"
  width="100%" 
  height="600" 
  style="border: 1px solid #ccc; border-radius: 8px;" 
  allow="clipboard-write; microphone; camera">
</iframe>

---

### ⚙️ Tech Stack  

- **FastAPI** for the API  
- **LangChain** for memory logic  
- **Claude 3.7 Sonnet** for prose generation  
- **spaCy** for semantic checks  
- **Google Cloud Run** for deployment  

---  

### 🔗 Links
Play with it on your own!

- 🐙 [GitHub Repository](https://github.com/jpz129/story-prose-generator)
- 📘 [API Documentation](https://story-prose-generator-415817045199.us-central1.run.app/docs)

