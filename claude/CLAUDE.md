# Vibe Studio OS - Project Context for Claude Code

This repository uses the **Vibe Studio OS** framework.

## Project Guardrails
- **Zero Secret Commits:** Never stage or commit `.env`, `.pem`, or API keys. Always update `.env.example` when adding environment variables.
- **Cost Protection:** External API/LLM calls must have `max_tokens` ceilings and request timeouts.
- **Modular Code:** Keep files focused and modular. Avoid giant monolithic components.
- **Board Alignment:** Refer to `PROJECT_BOARD.md` to see the active milestone and parked v2 backlog items before making architectural changes.
