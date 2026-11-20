# External Skills & Integration Catalog

Rather than reinventing capabilities, `vibe-studio-os` orchestrates established tools, skills, and plugins across the project lifecycle.

---

## Tool Mapping Table

| Domain | Best-in-Class Plugin / Skill | How `vibe-studio-os` Uses It |
| :--- | :--- | :--- |
| **Design & UI** | `figma`, Generative UI | Pulling mockups, verifying color palettes, generating wireframes and responsive layouts. |
| **Version Control** | GitHub CLI (`gh`), `git` | Repo initialization, branch protection, making clean milestone commits, creating PRs. |
| **Browser Testing & QA** | `browser` subagent, `chrome-devtools-plugin` | Opening local dev server (`http://localhost:3000`), testing button clicks, mobile viewport inspection. |
| **Deployment & Cloud** | `netlify`, `railway`, Vercel CLI | One-click production deployments, environment variable sync, preview builds. |
| **Documentation & Planning** | Google Docs (`gdocs`), Markdown Artifacts | Exporting user manuals, drafting pitch decks, or syncing business summaries. |
| **Task Management** | Linear (`linear`), Teamwork Graph | Syncing tasks to external trackers if the team prefers an external board over `PROJECT_BOARD.md`. |

---

## Delegation Guidelines
1. **When Design Work is Needed:**
   - Prompt: *"Would you like to connect a Figma design or use our built-in Generative UI tools to preview component layouts?"*
2. **When Testing a Feature:**
   - Instead of asking the user to manually click through, invoke the `browser` subagent or open DevTools to verify that the page renders without console errors.
3. **When Deploying:**
   - Recommend zero-config serverless platforms (Vercel, Netlify, Railway, Supabase) that offer generous free tiers and built-in SSL.
