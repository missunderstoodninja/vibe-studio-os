# 1-on-1 Intake Questionnaire Protocol

This protocol guides the conversational discovery process. It is designed to be friendly, encouraging, and focused on preventing expensive mistakes.

## Conversation Rules
1. **Pacing:** Ask exactly **ONE question at a time**. Never dump all 6 questions in a single turn.
2. **Upfront Expectation:** Start by telling the user you will ask 6 quick questions to understand their vision and build an executable roadmap.
3. **Active Listening:** Acknowledge and summarize the user's answer before asking the next question.

---

## The 6 Questions

### Question 1: The Core Pitch & Target User
> "Let's start with the big picture: In 1 or 2 sentences, what problem does this solve, and who is the exact person who will use or pay for it?"

### Question 2: The Form Factor & Platform
> "What form factor is best for this idea? Is it a Web App, Mobile App (iOS / Android / Cross-platform), Chrome Extension, Desktop tool, or API?"

### Question 3: The 'One Core Action' (MVP Scope Lock)
> "To keep things lean and launch fast: What is the single most important action a user takes in version 1.0?"

### Question 4: Monetization & Accounts
> "Will users need to log in (create accounts)? And how do you plan to monetize (e.g. monthly subscription, one-time payment, free/ad-supported, or internal tool)?"

### Question 5: Data Sensitivity & Paid APIs
> "Will this app store sensitive user data (files, medical, financial records), or call paid AI/third-party APIs (like OpenAI, Claude, Stripe)?"

### Question 6: Existing Assets & Tech Preferences
> "Last question: Do you already have any assets or preferred tools (like a domain, Figma designs, a GitHub account, Supabase, or Vercel)?"

---

## Transition to Generation
Once all 6 questions are answered, summarize the project in 3 bullets, validate alignment with the user, and immediately generate:
1. `PROJECT_BLUEPRINT.md` (Architecture, scope boundaries, lean stack selection).
2. `PROJECT_BOARD.md` (The dynamic Kanban roadmap).
