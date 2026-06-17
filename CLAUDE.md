# CLAUDE.md — Suryakant's Portfolio Site

## What this is
A single-page portfolio for **Suryakant Kumar**, a freelance developer who builds
**AI lead-gen automations (n8n) + landing pages**. The site's one job: make a
non-technical small-business owner or agency trust him fast and click a CTA
(Hire me / Watch demo / Message). Audience is **clients, not developers**.

## File
- `index.html` — the entire site. HTML, CSS, and JS are all in this one file. Keep it single-file.

## Design system (do not drift from this)
The look is **deep technical navy + a single warm "signal amber" accent**. The amber
is deliberate: it's the "🔥 hot lead" color from Suryakant's actual product. Don't
add a second bright accent — spend boldness in one place.

Color tokens (defined in `:root`, always use the variables, never hardcode hex):
- `--ink` #0a0e1a — page background
- `--ink-2 / --ink-3` — raised surfaces / cards
- `--line` #243149 — hairline borders
- `--text` #e8edf6 — primary text
- `--muted` #8a97ad — secondary text
- `--signal` #ff8a3d — THE accent (amber). Used for CTAs, active states, highlights.
- `--ok` #39d98a — pipeline "success" green only

Type:
- Body: Inter / system sans
- `.mono` class = JetBrains Mono, used for data, labels, code-like readouts. The
  monospace is part of the identity (it speaks "automation"). Don't replace it with sans.

## The signature element — protect this
The hero contains a **live, self-running pipeline** (`.stage` / `#pipe`): a lead flows
through 5 nodes (Lead in → AI scores → Logged → Auto-reply → You're pinged), with a
travelling amber dot and a cycling data readout. This is the single most important,
most memorable part of the page. **Do not remove or simplify it.** If editing it,
keep the JS animation timing (5s loop, 5 nodes) and the node activation in sync with
the travelling dot.

## Copy rules
- Write from the **client's** side, in plain language. "Leads slipping through the
  cracks," not "webhook configuration."
- Active voice, sentence case, no filler. A button says exactly what happens.
- Don't make it sound AI-generated or templated. Specific > clever.

## Quality floor (keep these working)
- Responsive down to mobile (there are `@media(max-width:640px/720px)` blocks — test them).
- `prefers-reduced-motion` is respected (animations disabled). Keep that.
- Visible keyboard focus / accessible links.

## TODO placeholders to fill in
1. **Demo video** — the `.demo-vid` play button is a placeholder that currently shows
   an alert. Replace with the real Loom embed once recorded. (This is the
   make-or-break element — the page only "works" once the video is in.)
2. **WhatsApp number** — `#waLink` uses `916299991463`. Confirm/replace.
3. **Email** — `jnvsuryakant@gmail.com` in the contact button. Confirm/replace.

## How to preview
Right-click `index.html` in VS Code → "Open with Live Server" → auto-refreshes on save.

## When making changes
- Keep everything in the one file.
- Use the CSS variables, never hardcode colors.
- After changes, sanity-check mobile layout and that the hero pipeline still animates.
