# Project Board & Roadmap Specification

The `PROJECT_BOARD.md` is the living heartbeat of the project. It turns the initial conversation into an executable sequence of milestones.

## Markdown Format Template

```markdown
# 🚀 Project Board: [Project Name]
*Generated and orchestrated by Vibe Studio OS*
*Last Updated: [YYYY-MM-DD]*

---

## 🧭 Project Blueprint Summary
- **Target User & Problem:** [1 sentence]
- **Core Value Action:** [The single MVP action]
- **Selected Stack:** [e.g. Next.js 14, TailwindCSS, Supabase, Vercel]
- **Monetization:** [e.g. Stripe Checkout subscription]

---

## 📋 Backlog (Future v2 - Parked to Defend Scope)
> *Ideas that are good, but would delay the initial launch.*
- [ ] Feature: [Idea 1]
- [ ] Feature: [Idea 2]

---

## ⏳ Active Milestone
### 🎯 Milestone [N]: [Milestone Title]
**Responsible Agent:** [e.g., Tech Lead / Security Gatekeeper / Marketing]
**Required Skills/Tools:** [e.g., git, npm, figma]

#### Tasks:
- [ ] Task 1: [Specific actionable step]
- [ ] Task 2: [Specific actionable step]
- [ ] Task 3: [Specific actionable step]

#### Quality & Safety Gate:
- [ ] Gate: [e.g. Code builds without warnings, no hardcoded API keys, rate limits in place]
- [ ] Git commit created for Milestone [N]

---

## 🗓️ Upcoming Milestones
- [ ] **Milestone [N+1]:** [Title] (Owner: [Role])
- [ ] **Milestone [N+2]:** [Title] (Owner: [Role])
- [ ] **Milestone [N+3]:** [Title] (Owner: [Role])

---

## ✅ Completed Milestones
- [x] **Milestone 0: Intake & Blueprint Approval** (Owner: Product Manager)
```

## Milestone Orchestration Rules
1. **One Milestone at a time:** Keep focus razor-sharp. Never run multiple milestones concurrently unless explicitly requested.
2. **Handoff Prompts:** When an active milestone is marked complete, the orchestrator announces the next milestone and the primary agent taking over.
3. **Scope Defense:** When the user asks for a new feature, add it under `## 📋 Backlog` and ask: *"I've saved this to your v2 backlog. Would you like to finish the current milestone first, or swap this into the active scope?"*
