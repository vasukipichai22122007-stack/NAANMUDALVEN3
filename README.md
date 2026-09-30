# EduGenie Core Engine | Adaptive Educational Intelligence

An interactive, futuristic web platform and backend engine for **EduGenie**, combining high-density text summarization, multi-level concept simplification (LaMini-Flan-T5 logic), direct authoritative knowledge retrieval (Google Gemini 1.5 Pro), strict 3-MCQ quiz generation, and adaptive curriculum roadmaps.

---

## ⚡ Quick Start

### Option 1: Run with Python Server (Recommended)
EduGenie includes a zero-dependency Python 3 backend server that serves the web application and handles all 5 API endpoints:

```bash
# 1. Run automated self-verification tests
python server.py --test

# 2. Launch the EduGenie server
python server.py
```

Then open your browser to:
👉 **[http://localhost:8000](http://localhost:8000)**

### Option 2: Direct Browser Launch
You can also directly open `index.html` in any modern web browser (Chrome, Edge, Firefox, Safari). The frontend contains a built-in client-side engine mirror that runs 100% offline without needing any setup or dependencies.

---

## 🚀 The 5 Core Modules

| Module | Endpoint | Model / Logic | Description |
| :--- | :--- | :--- | :--- |
| **Summarizer** | `/summarize` | High-Yield Distillation | Condenses dense academic text, calculates reading time saved & compression ratio, outputs core takeaways. |
| **Explainer** | `/explain` | LaMini-Flan-T5 Logic | Multi-tier simplification (*👶 ELI5*, *🎓 High School*, *🔬 College*) with visual bullet trees (`├─`, `└─`). |
| **Quiz Engine** | `/quiz` | Strict Schema Generator | Generates 3-question MCQs (`{"quiz": [{"question", "options", "answer"}]}`) with interactive grading & confetti. |
| **Q&A Oracle** | `/qa` | Google Gemini 1.5 Pro | Direct, high-precision single-paragraph answers with accuracy ratings. |
| **Curriculum** | `/learn/recommendations` | Adaptive Roadmap | Generates 3-tier learning roadmaps (*Beginner ➔ Intermediate ➔ Advanced*) with milestone checkboxes and practice goals. |

---

## 🛡️ Zero-Break Protocol

EduGenie is engineered with a strict **Zero-Break Exception Protocol**. Empty, corrupted, or malformed queries will never throw a 500 error or crash the UI. Instead, the engine catches edge cases and delivers a standardized fallback payload:

```json
{
  "status": "handled_error",
  "endpoint": "/summarize",
  "message": "⚠️ Request processed with default parameters.",
  "fallback_data": "EduGenie captured an ambiguous or empty prompt. Default zero-break parameters applied."
}
```

You can test this behavior in real time by clicking the **"🛡️ Test Zero-Break Protocol (Edge Cases)"** button on the website.

---

## 🎨 Pedagogical Stylistic Signature

All visual outputs adhere to EduGenie's signature pedagogical standards:
- **Core Concept Blocks**: Highlighted takeaways in bold context sections.
- **Tree Visual Markers**: Structured hierarchies using `├─` and `└─`.
- **Knowledge Nuggets**: Every concept finishes with an actionable `💡 Key Insight` banner.

---

## 🛠️ File Structure

```
jeevidhya k/
├── index.html        # Interactive Single-Page Application (Tailwind + Glassmorphism)
├── app.js            # Frontend state manager, router, quiz engine, audio TTS
├── styles.css        # Cyber-pedagogy theme, tree diagrams, animations, glowing borders
├── server.py         # Zero-dependency Python server with API endpoints & test suite
└── README.md         # Documentation & guide
```
