# 🐧 ChatVector Linux Docs

## 📌 Context
**Repository:** [chatvector-ai/chatvector-ai](https://github.com/chatvector-ai/chatvector-ai)  
**PR:** [#37](https://github.com/chatvector-ai/chatvector-ai/pull/37)

ChatVector is an AI project that requires a specific environment setup to run.

## ⚠️ The Problem
The project's documentation included setup instructions for macOS and Windows but completely omitted instructions for Linux users. This left Linux developers guessing about the correct virtual environment commands and dependencies.

## 🛠️ The Solution
I added a dedicated section for Linux Virtual Environment setup to the documentation.

**Contribution:**
- Documented commands for creating a virtual environment: `python3 -m venv venv`
- Documented activation commands: `source venv/bin/activate`
- Unified the instruction flow for all major operating systems.

## 🚀 Impact
Linux users can now set up the project environment immediately without external research, making the project more inclusive and developer-friendly.
