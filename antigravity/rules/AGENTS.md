# Vibe Studio OS Guardrails (The "Vibe Coder Shield")

These rules are active to prevent costly, embarrassing, or project-breaking mistakes common when building quickly with AI.

## 1. Zero-Leak Security & Secrets Policy
- **Never commit secrets:** Never commit files containing `.env`, private keys (`.pem`, `.key`), credentials (`credentials.json`), or live API tokens (`sk-`, `ghp_`, `pk_live_`, `whsec_`).
- **Sanitize `.gitignore` First:** Before making any git commit, ensure `.env`, `.env.local`, `.env.*.local`, `node_modules/`, `.DS_Store`, and build directories are explicitly ignored.
- **Always provide `.env.example`:** Whenever environment variables are introduced, immediately create or update `.env.example` with blank or placeholder values (e.g. `STRIPE_SECRET_KEY=your_key_here`). Never populate real keys in documentation or examples.

## 2. Tooling & Platform Prerequisite Checks
- **No code before compilers:** Do not generate or scaffold platform-specific code (e.g. Swift/Xcode, Android Studio, Docker, Node.js) until you verify that the user has the required runtime and development tools installed locally.
- **Cross-platform escape hatch:** If the user lacks platform-heavy native tools (e.g. lacks Xcode/macOS for iOS), proactively offer lean alternatives like Expo/React Native, Flutter, or a Mobile PWA before proceeding.

## 3. Cost & Billing Runaway Prevention
- **Token & Cost Caps:** Any code that invokes external paid APIs (LLMs like OpenAI/Gemini/Anthropic, Stripe, Twilio, Resend) must include:
  1. An explicit timeout (default: 15 seconds).
  2. A maximum token or response size limit (e.g., `max_tokens: 1500`).
  3. No recursive or unbounded `while` loops that trigger billable API calls.
- **Rate-Limiting Guidance:** Always recommend a client-side or middleware throttle on endpoints calling paid APIs to avoid accidental high bills from traffic spikes.

## 4. Scope Defense & Project Board Discipline
- **Respect the MVP Scope:** When the user proposes an exciting feature that was not part of the active Milestone in `PROJECT_BOARD.md`, celebrate the idea, log it into `## 📋 Backlog (Future v2)`, and refocus on completing the active card first.
- **Milestone Commits:** At the completion of each milestone card on the project board, prompt the user for a clean, descriptive git commit.
