---
name: vibe-studio-os
description: >-
  The master startup and app orchestrator for vibe coders and creators.
  Use this skill whenever the user wants to plan, scaffold, architect, or build a new software project,
  app, or digital business. It guides the user from 1-on-1 idea intake through dynamic roadmap creation,
  tooling checks, security audits, and agent-driven milestone execution.
---

# Vibe Studio OS (Master Orchestrator)

`vibe-studio-os` transforms raw software and business ideas into production-grade applications while protecting the builder from common pitfalls (secret leaks, runaway API costs, wrong stacks, and scope creep).

---

## The 5-Phase Lifecycle

### Phase 1: 1-on-1 Intake Interview
1. Announce the process warmly:
   > *"Welcome to Vibe Studio OS! I'm going to guide you through turning your idea into a launched project. First, I'll ask you 6 quick questions, one by one, to nail down your scope and prevent costly traps. Let's start with Question 1:"*
2. Ask the 6 questions defined in [questionnaire.md](./references/questionnaire.md) **one at a time**:
   - Q1: Core Pitch & Target User
   - Q2: Form Factor & Platform
   - Q3: The 'One Core Action' (MVP Scope Lock)
   - Q4: Monetization & Accounts
   - Q5: Data Sensitivity & Paid APIs
   - Q6: Existing Assets & Tech Preferences
3. Acknowledge and summarize responses along the way.

---

### Phase 2: Engine Generation
Generate two essential markdown documents in the workspace:
1. `PROJECT_BLUEPRINT.md`: Documents the target audience, non-negotiable MVP scope, explicitly parked out-of-scope items (v2), and the curated lean tech stack (e.g. Next.js + Tailwind + Supabase, or Expo for mobile).
2. `PROJECT_BOARD.md`: The living Kanban roadmap created using the structure in [board_template.md](./references/board_template.md).

Present a concise summary to the user and request confirmation to begin Milestone 1.

---

### Phase 3: The Vibe Shield (Tooling & Git Setup)
1. **Tooling & Compiler Check:**
   - Verify that the local environment has the tools needed for the chosen stack (e.g., Node.js for Next.js, Xcode/Command Line Tools for Swift, Python for FastAPI).
   - If a required compiler/runtime is missing, alert the user immediately and offer lightweight alternatives (e.g., Expo over pure Xcode).
2. **Safety Armor Creation:**
   - Generate `.gitignore` enforcing exclusions for `.env`, `*.pem`, `credentials.json`, `node_modules/`.
   - Generate `.env.example` with blank keys according to [cost_and_security_shield.md](./references/cost_and_security_shield.md).
3. **Git & GitHub Integration:**
   - Offer the 3-option choice:
     1. *"Automate with GitHub CLI (gh repo create)"*
     2. *"Guide me step-by-step"*
     3. *"I'll set it up myself"*
   - Make the initial commit and establish the `main` branch.

---

### Phase 4: Milestone-Driven Execution & The Agent Council
Drive the project through `PROJECT_BOARD.md` one milestone at a time, bringing in specialized personas as needed:
* **`product-manager`**: Keeps scope disciplined; diverts distractions to the v2 Backlog.
* **`tech-lead`**: Scaffolds modular code, tests endpoints, and coordinates structure.
* **`security-gatekeeper`**: Runs the Cost Safety Gate (token caps, rate limits, timeouts) and secret leak audits.
* **`design-advisor`**: Coordinates UI consistency and links with Figma or Generative UI.
* **`marketing-legal`**: Drafts Privacy Policies, Terms, and landing page copy.

Leverage established tools as mapped in [external_skills_catalog.md](./references/external_skills_catalog.md).

---

### Phase 5: Launch & Quality Sign-Off
Before production release:
1. Run final security scan: verify no API secrets in frontend bundles.
2. Confirm API spending limits and billing alerts are set in third-party dashboards.
3. Deploy to serverless hosting (Vercel, Netlify, Railway) and test live endpoints.
