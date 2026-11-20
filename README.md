# 🚀 Vibe Studio OS

**The Startup Operating System for vibe coders and modern founders.**
Turn your app and business ideas into production-ready software without making costly mistakes.

---

## What It Does

Vibe Studio OS is an intelligent orchestrator designed to guide founders from an initial spark of an idea to a deployed product while actively protecting them from typical traps:
* **Zero Secret Leaks:** Prevents accidental commits of `.env` files, Stripe keys, or OpenAI tokens.
* **Cost Runaway Shield:** Enforces token limits, timeouts, and rate limits so you never wake up to an unexpected \$500 API bill.
* **Scope Defense:** Locks in the core MVP value and parks distractions into a v2 Backlog.
* **Tooling Diagnostics:** Checks that prerequisites (like Node or Xcode) are installed *before* writing code, or suggests cross-platform alternatives (like Expo).
* **The Agent Council:** Seamlessly transitions between roles: Product Manager, Tech Lead, Security Gatekeeper, Design Advisor, and Marketing/Legal Lead.

---

## Project Structure

```text
vibe-studio-os/
├── README.md                          # This file
├── antigravity/                       # Native Antigravity Plugin
│   ├── plugin.json                    # Plugin metadata & suggested prompts
│   ├── rules/
│   │   └── AGENTS.md                  # Vibe Coder Shield rules (always active)
│   ├── skills/
│   │   └── vibe-studio-os/
│   │       ├── SKILL.md               # Master orchestrator instructions
│   │       └── references/
│   │           ├── questionnaire.md   # 1-on-1 interview protocol
│   │           ├── board_template.md  # Dynamic project board format
│   │           ├── cost_and_security_shield.md  # Cost cap & secret protection guide
│   │           └── external_skills_catalog.md   # Mapping to Figma, DevTools, GitHub, etc.
│   └── agents/
│       ├── product-manager.md         # Scope defender & board manager
│       ├── tech-lead.md               # Clean, modular code architect
│       ├── security-gatekeeper.md     # Cost & security auditor
│       ├── design-advisor.md          # UI/UX consistency & mobile responsiveness
│       └── marketing-legal.md         # Privacy policies, terms, & launch copy
├── claude/                            # Claude Configuration
│   ├── CLAUDE_PROJECT_PROMPT.md       # Copy/paste prompt for Claude Projects
│   └── CLAUDE.md                      # Context file for Claude Code CLI
└── chatgpt/                           # ChatGPT Configuration
    ├── CUSTOM_GPT_INSTRUCTIONS.md     # Instructions for OpenAI Custom GPT builder
    └── GPT_KNOWLEDGE_BUNDLE.md        # Reference document to upload to Custom GPT
```

---

## How to Use

### 1. In Antigravity
To install `vibe-studio-os` globally in Antigravity:
1. Copy or symlink the plugin folder into your Antigravity plugin directory:
   ```bash
   cp -r /Users/niphomkhwane/Documents/vibe-studio-os/antigravity ~/.gemini/config/plugins/vibe-studio-os
   ```
2. In Antigravity chat, simply type:
   > *"I have an idea for an app, let's start the vibe-studio-os intake."*

### 2. In Claude (Claude Projects & Claude Code)
* **Claude Projects:** Open your Claude Project, click **Set Project Instructions**, and paste the contents of `claude/CLAUDE_PROJECT_PROMPT.md`.
* **Claude Code CLI:** Keep `claude/CLAUDE.md` in the root of your project repository for automatic context.

### 3. In ChatGPT (Custom GPT)
1. Go to [chatgpt.com/gpts/editor](https://chatgpt.com/gpts/editor) and click **Create a GPT**.
2. Go to the **Configure** tab.
3. Paste the contents of `chatgpt/CUSTOM_GPT_INSTRUCTIONS.md` into **Instructions**.
4. Set the conversation starters provided in `chatgpt/CUSTOM_GPT_INSTRUCTIONS.md`.
5. Under **Knowledge**, upload `chatgpt/GPT_KNOWLEDGE_BUNDLE.md`.
6. Click **Save / Publish** (Private, Anyone with link, or Public).
