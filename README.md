Trae AI Rules (Web Stack Guardrails)
Repository of rules and guardrails for Trae IDE to maintain consistency in architecture, security, performance, SEO, and UX/UI for projects using React, Astro, Next.js, and NestJS.

Objective
Reduce common errors when coding with AI agents (destructive changes, duplication, assumptions).

Ensure best practices in frontend (TS/TSX), backend (NestJS), and design (UX/UI).

Maintain a single standard for teams and repositories.

What it contains
General rules (quality, safe refactoring, no-deletion, anti-duplication).

Framework-specific rules:

React (TSX + hooks).

Astro (islands + client:* directives).

Next.js (App Router + metadata/SEO + caching).

NestJS (modular architecture + security + versioning + CORS + JWT).

UX/UI rules to avoid generic interfaces.

Quick checklists (pre-commit / pre-PR).

Repo structure
rules/00-general.md

rules/02-frontend-astro.md

rules/03-frontend-nextjs.md

rules/04-backend-nestjs.md

rules/05-ux-ui.md

rules/99-checklists.md

How to use in Trae
Copy the content of the rules file you need (for example rules/03-frontend-nextjs.md).

Paste it into your agent's "Rules" configuration in Trae.

Keep only what is necessary for your project (many agents have character limits).

Recommendation: use rules/00-general.md as a base and add only 1–2 files per project (e.g., Next.js + NestJS).

Conventions for writing rules
Each rule must be actionable and verifiable (avoid "make it pretty").

Use "DO / DON'T" or imperative phrases.

If a rule has an exception, document the exception explicitly.

If a rule involves risk (security/SEO), it requires confirmation before applying large changes.

Contribute / Maintain
If you add a rule, include:

Motivation (what bug it avoids).

Short example (optional).

Scope (global / framework / module).

Avoid duplicate rules: reference the general rule when applicable.

Roadmap (optional)
Ready-to-use templates for copying and pasting depending on the project type (landing page, dashboard, app with auth, etc.).

"Compact rules" (<1000 chars) per stack for agents with strict limits.
