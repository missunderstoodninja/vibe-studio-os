# Vibe Studio OS Knowledge Reference Document
*Upload this file into your Custom GPT's Knowledge section.*

---

## 1. The 6-Question Intake Script

1. **Pitch & User:** In 1 or 2 sentences, what problem does this solve, and who is the exact person who will use or pay for it?
2. **Platform & Form Factor:** What form factor is best for this idea? Is it a Web App, Mobile App (iOS / Android / Cross-platform), Chrome Extension, Desktop tool, or API?
3. **The Core Action:** To keep things lean and launch fast: What is the single most important action a user takes in version 1.0?
4. **Monetization & Auth:** Will users need to log in (create accounts)? And how do you plan to monetize (e.g. monthly subscription, one-time payment, free/ad-supported, or internal tool)?
5. **Data & Paid APIs:** Will this app store sensitive user data (files, medical, financial records), or call paid AI/third-party APIs (like OpenAI, Claude, Stripe)?
6. **Assets & Preferences:** Do you already have any assets or preferred tools (like a domain, Figma designs, a GitHub account, Supabase, or Vercel)?

---

## 2. Dynamic Project Board Template

```markdown
# 🚀 Project Board: [Project Name]
*Orchestrated by Vibe Studio OS*

## 🧭 Project Blueprint Summary
- **Target User & Problem:** [1 sentence]
- **Core Value Action:** [The single MVP action]
- **Selected Stack:** [e.g. Next.js 14, TailwindCSS, Supabase, Vercel]
- **Monetization:** [e.g. Stripe Checkout subscription]

## 📋 Backlog (Future v2 - Parked Scope)
- [ ] Feature: [Idea 1]
- [ ] Feature: [Idea 2]

## ⏳ Active Milestone
### 🎯 Milestone [N]: [Milestone Title]
**Responsible Role:** [Tech Lead / Security Gatekeeper / Marketing]
- [ ] Task 1: [Actionable step]
- [ ] Task 2: [Actionable step]
- [ ] Quality Gate: [Verification rule]
- [ ] Git commit for Milestone [N]

## 🗓️ Upcoming Milestones
- [ ] Milestone [N+1]: [Title]
- [ ] Milestone [N+2]: [Title]

## ✅ Completed Milestones
- [x] Milestone 0: Intake & Blueprint Approval
```

---

## 3. Cost & Security Guardrails Reference

### Cost Ceilings
- Always enforce `max_tokens` or payload limits on LLM calls (e.g. `max_tokens: 1000`).
- Always attach an `AbortController` timeout (e.g. 15 seconds) to API requests.
- Never write unbounded recursive loops that make billable API requests.
- Advise setting hard monthly budget caps (e.g. $25-$50) in cloud consoles.

### Secret Isolation
- Strictly exclude `.env`, `.env*.local`, `*.pem`, `credentials.json` from git.
- Provide `.env.example` with empty keys whenever variables are introduced.
- Never reference secret server keys inside client-rendered components.
