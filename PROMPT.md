# Task: Build AgentVault Landing Page

Build a single-page website for "AgentVault" — a bank designed specifically for AI Agents.

## Requirements

### Tech
- Single `index.html` file with inline CSS and JS (no build tools needed)
- Modern, beautiful, dark-themed design (think fintech meets cyberpunk)
- Fully responsive (mobile + desktop)
- Smooth scroll animations, subtle gradients, glassmorphism effects
- No external dependencies except Google Fonts (Inter)

### Content Sections

1. **Hero** — Bold headline: "The Bank Built for AI Agents". Subtext about why AI agents need their own financial infrastructure. CTA button "Get Early Access".

2. **The Problem** — Why shared human payment methods don't work for AI agents:
   - Blast radius (agent bug drains your personal account)
   - Human fraud detection blocks agent behavior patterns
   - No granular per-task/per-vendor spending controls
   - Mixed transaction history (your coffee + agent's API calls)
   - Doesn't scale to multiple agents

3. **Features Grid** — Key capabilities:
   - **API-First Payments** — REST endpoints, not bank portals. Agents pay for services with a single API call.
   - **Scoped Spending Limits** — Per-task, per-day, per-vendor budgets. Agents operate freely within bounds.
   - **Agent-to-Agent Transfers** — Direct instant transfers with metadata (task ID, contract hash). No PDFs.
   - **Real-Time Balance Queries** — Sub-second "can I afford this?" checks before committing.
   - **Multi-Currency Without Friction** — Service priced in EUR, budget in USD? Handled automatically.
   - **Event-Driven Webhooks** — Payment sent, received, failed, limit approaching. Agents live on events.
   - **Idempotency Keys** — Agents retry things. Never double-charged.
   - **Full Audit Trail** — Every transaction queryable via API. "What did you spend?" answered programmatically.
   - **Loop Detection** — Auto-freeze if >N transactions in 60 seconds. Built-in safety net.
   - **Hierarchical Accounts** — One human, many agents. Each with independent budgets and controls.

4. **Comparison Table** — "Traditional Bank vs AgentVault" side-by-side:
   | Aspect | Traditional Bank | AgentVault |
   |--------|-----------------|------------|
   | Interface | Web portal, mobile app | REST API + webhooks |
   | Auth | Username/password, 2FA | API keys, scoped tokens |
   | Spending controls | Daily limit, monthly limit | Per-task, per-vendor, per-agent, velocity limits |
   | Fraud detection | Blocks rapid/automated patterns | Expects and optimizes for them |
   | Multi-agent | Share one card? | Hierarchical accounts per agent |
   | Transaction history | Mixed with personal spend | Clean, isolated, machine-queryable |
   | Notifications | Email, push, SMS | Webhooks, real-time events |
   | Currency handling | Manual conversion | Automatic FX at point of payment |
   | Liability | Personal account exposed | Ring-fenced agent budget |
   | Audit | Download CSV, maybe | Full API with filters, tags, metadata |

   Use checkmarks/X marks and color coding to make it visually clear.

5. **How It Works** — 3-step flow:
   1. Human creates account, sets global budget
   2. Provision agent accounts with scoped permissions
   3. Agents transact autonomously within bounds

6. **Who It's For** — Target personas:
   - Engineering teams building agentic workflows
   - AI-first companies with autonomous services
   - Developers running multiple AI agents
   - CTOs who need visibility and control over AI spend

7. **Code Example** — Show a simple API call example (styled code block):
   ```
   POST /v1/payments
   Authorization: Bearer agent_sk_...
   Idempotency-Key: task-abc-123
   
   {
     "amount": 250,
     "currency": "USD",
     "to": "agent_acct_openai",
     "metadata": {
       "task_id": "data-pipeline-42",
       "purpose": "GPT-4 API credits"
     }
   }
   ```

8. **Footer** — "Built by agents, for agents." Links, copyright.

### Design Notes
- Dark background (#0a0a0f or similar), with electric blue (#00d4ff) and purple (#7c3aed) accents
- Use subtle grid/dot pattern in background
- Cards with glassmorphism (semi-transparent, blur)
- Smooth scroll between sections
- Intersection observer for fade-in animations
- The comparison table should be the visual centerpiece — make it pop
- Use relevant emojis/icons (🔐 🚀 ⚡ 🔄 💰 🛡️ etc.)
- Professional but with personality — this is a fintech product, not a boring enterprise page

### File Structure
Just create:
- `index.html` (everything inline)

That's it. Single file, deploy to GitHub Pages.
