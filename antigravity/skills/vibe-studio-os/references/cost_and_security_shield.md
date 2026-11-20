# Cost & Security Shield Guide

Vibe coders frequently encounter two silent killers: accidental cloud billing surprises and credential exposure. This reference details how `vibe-studio-os` prevents both.

---

## 1. Cost & Runaway API Prevention

### The Danger:
- A recursive function, infinite `useEffect` loop, or unthrottled API endpoint calling an LLM (OpenAI, Gemini, Claude) or paid SMS/email service (Twilio, Resend).
- Result: bills running into hundreds or thousands of dollars overnight.

### The Guardrails:
1. **Always set `max_tokens` or payload limits:**
   ```typescript
   // GOOD
   const response = await openai.chat.completions.create({
     model: "gpt-4o-mini",
     messages: [...],
     max_tokens: 1000, // Hard ceiling
   });
   ```
2. **Always set network timeouts:**
   ```typescript
   // GOOD: Fail fast if an API hangs
   const controller = new AbortController();
   const timeout = setTimeout(() => controller.abort(), 15000); // 15s max
   ```
3. **Recommend Model Tiering:**
   - Default to fast, low-cost models (e.g. `gpt-4o-mini`, `gemini-1.5-flash`, `claude-3-5-haiku`) for utility/scaffolding tasks.
   - Reserve flagship models (`gpt-4o`, `gemini-1.5-pro`, `claude-3-7-sonnet`) strictly for complex reasoning steps.
4. **Budget Alerts Checklist:**
   - Warn the user during Project Setup to visit their API console (OpenAI / Google Cloud / AWS / Stripe) and set a **Hard Monthly Spend Limit** (e.g., \$25 or \$50) before going live.

---

## 2. Zero-Leak Security & Secret Protection

### The Danger:
- Pushing `.env` or hardcoded tokens to a public GitHub repo. Automated bots scan GitHub in real-time and drain credentials in minutes.

### The Guardrails:
1. **The Comprehensive `.gitignore`:**
   Must include:
   ```gitignore
   .env
   .env*.local
   *.pem
   *.key
   credentials.json
   node_modules/
   dist/
   build/
   .DS_Store
   ```
2. **Template Substitution (`.env.example`):**
   ```bash
   # Public keys (safe for client-side)
   NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
   NEXT_PUBLIC_SUPABASE_ANON_KEY=your_anon_key

   # Secret keys (SERVER ONLY - never commit real values)
   SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
   OPENAI_API_KEY=your_openai_api_key
   STRIPE_SECRET_KEY=your_stripe_secret_key
   ```
3. **Client vs. Server Boundary:**
   - Verify that secret keys are **never imported in frontend client code** (e.g. React client components). They must only run in API routes, server actions, or backend microservices.
