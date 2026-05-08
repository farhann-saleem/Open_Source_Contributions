# Runway Copilot

**The Autonomous AI Inbox Manager for Student Opportunities**  
*Built for SOFTEC 2026 · Powered by DeepSeek V3 & Qwen 2.5-72B*

**Repository:** [Runway Copilot](https://github.com/farhann-saleem/runway-copilot)

## 🌟 The Problem
University students in Pakistan handle chaotic inboxes filled with dense, unstructured emails about scholarships, fellowships, and internships. Critical deadlines are missed, eligibility criteria are misunderstood, and communicating these complex opportunities to parents often creates friction due to language barriers.

## 🚀 Our Solution
Runway Copilot is a local, privacy-first AI engine that acts as an intelligent layer over your inbox. It autonomously ingests your emails, extracts rigid data points using LLMs, calculates your "runway" before a deadline hits, and provides a localized Urdu summary for parents.

## 🔥 Key Innovations & Moats

### 1. Zero-Auth Gmail Ingestion (Chrome Extension)
Instead of forcing users onto complex Google OAuth flows or requiring production developer keys to read their Gmail, we built a standalone DOM-Scraping Chrome Extension.
- It acts as a hyper-fast "Clipper". You open a Gmail thread, click the extension, and the script reliably extracts the sender, subject, and body from Gmail's hidden `.a3s` and `h2.hP` classes.
- It pushes the data directly into the local FastAPI backend bypassing CORS, ensuring 100% privacy and zero setup friction.

### 2. DeepSeek V3 Triaging Engine
Our FastAPI backend uses Pydantic schema enforcement to force DeepSeek V3 to extract unstructured email text into structured data. It scores every email on a 0-100 scale based on:
- **Runway Math:** Offline Semantic calculations (MiniLM) to figure out if you actually have enough time to apply.
- **Trust Checks:** Heuristics to catch lookalike scams (e.g., `.org` vs `.info`), placing them on the Suspicious rail.

### 3. "The Abba Brief" (Qwen 2.5-72B)
To solve the parent-student communication gap, we integrated Qwen 2.5-72B. With a single click, it translates complex corporate internship emails into a localized, respectful Urdu summary ("The Abba Brief") read right-to-left, making family discussions over dinner seamless.

### 4. Context-Aware Student Chatbot
Embedded directly into the Next.js results page, our chatbot is fully context-aware. It knows your exact profile (CGPA, degree, semester) and knows exactly which email opportunity you are looking at. You can ask "Am I eligible for this?", and it answers based on both you and the email text.
