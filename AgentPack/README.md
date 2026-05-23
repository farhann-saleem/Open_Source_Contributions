# AgentPack

**Workflow Installer for Vibe Coders**

**Repository:** [AgentPack](https://github.com/farhann-saleem/AgentPack)

AgentPack is a CLI tool and workflow layer designed specifically for "vibe coders" using AI agent coding environments. It addresses the gap where AI coding tools are strong at rapid code generation but weak at structured workflow, upfront planning, and long-term memory.

## 🚀 What It Does
AgentPack installs a repo-local workflow layer that provides:
- **Product Thinking:** Forces clarity and design decisions before random implementation.
- **Persistent Memory:** Maintains global, project, and session memory inside `.agentpack/memory/` so the AI remembers context and decisions across long tasks.
- **Session Traceability:** Creates detailed, visible session folders documenting prompts, plans, tests, and security reviews for every `/agentpack` run.
- **Security & Testing Guardrails:** Automates the generation of benchmark gates and test checklists before finalizing code.

## 🛠️ How It Works
Instead of being a constantly running terminal process, AgentPack acts as a one-time installer:
1. Run `npx github:farhann-saleem/agentskill install` in your repo.
2. It injects a suite of skills, steering files, and a `/agentpack` slash command into your coding environment (e.g., `.kiro/skills/agentpack/SKILL.md`).
3. You trigger structured workflows naturally by prompting `/agentpack Build a beautiful marketplace...`, and the agent handles planning, memory updates, and execution autonomously.

## 🌟 Key Features
- **Frontend Taste:** Embeds instructions ensuring the agent outputs polished, modern UI components instead of generic layouts.
- **Visible Planning:** Moves away from hidden chat logic to explicit, version-controlled markdown plans.
- **One-Command Install:** Easily injects the entire workflow system into any project via `npx`.
