# JOONS-ME Consulting Agency Ltd — Website Handoff

## Context
This is the marketing site for **JOONS-ME Consulting Agency Ltd**, a Nigerian consulting agency (parent company to a portfolio of ventures including Zee Fashion, Ohmoworld, and Eziza). The agency consults on: software, hardware, team/management, and offers programming tutoring.

A single-file HTML/CSS/JS prototype has already been designed and approved for direction. It lives at:

```
index.html
```

This file is currently **one static HTML file** with embedded `<style>` and `<script>` — no build tooling, no framework. Open it directly in a browser to see the current state before making changes.

## Design system already established (keep consistent)

**Colors**
- `--navy: #0A0A32` / `--navy-2: #0D0D3E` / `--navy-panel: #14144a` — dark backgrounds
- `--purple: #6C3483` / `--purple-dark: #4A1480`
- `--gold: #E8A838` / `--gold-soft: #f3c976`
- `--teal: #00C3E3`
- `--cream: #F7F4EC` — light section background / dark-on-light text base (`--ink: #0D0D3E`)

**Type**
- Display: `Space Grotesk` (headings)
- Body: `Inter`
- Mono/utility: `JetBrains Mono` (used for eyebrows, tags, terminal UI, form labels — this is a deliberate signature, not incidental)

**Signature design elements — preserve these, don't genericize them**
1. **Terminal/console hero panel** — a fake terminal window that types out consulting commands (`consult --practice=software`, `tutor --language=python,dart,php,js`, etc.) and prints mock outputs. This is the page's core visual identity, tying "we consult on software + teach code" into the UI itself.
2. **Mono `$` eyebrows** instead of numbered section markers (e.g. `$ services.list()`, `$ portfolio.list()`) — reinforces the terminal/code motif throughout, not just in the hero.
3. **Angled section dividers** — light (`.light`) sections use `clip-path: polygon(...)` to cut in on a diagonal at the top instead of a flat rule.
4. **Circuit-trace SVG watermark** faintly behind the hero — ties into hardware/software subject matter.
5. Portfolio cards use each subsidiary's **own brand gradient** as a swatch (Zee Fashion purple, Ohmoworld navy/teal, Eziza gold/purple) with a subtle grid overlay.

Do not replace these with generic patterns (numbered 01/02/03 markers, plain icon-plus-stat hero, stock card grids) — they were deliberately chosen against the brief's subject matter.

## Known placeholder content that needs real data
- **Portfolio section**: Zee Fashion / Ohmoworld / Eziza cards have placeholder links (`href="#"`) and generic one-line descriptions — replace with real links and, if desired, real screenshots/logos instead of solid-color swatches.
- **Testimonials section**: three testimonial cards are entirely placeholder quotes and "Client Name / Role, Company" — replace with real client feedback once available, or keep hidden until then.
- **Contact form**: submit handler is a placeholder `alert()`. It needs to actually send somewhere — options:
  - Wire to **Resend** (already used for the Ohmoworld email module) via a small backend endpoint or serverless function
  - Or a simple `mailto:` / form service (Formspree, etc.) if no backend is planned
- Real logo/favicon — currently text-only wordmark (`JOONS-ME`), no favicon set.

## Confirmed real content (already in the file, don't regenerate)
- Address: `10, Osemwengie Street, off Akugbe Road, Benin City`
- Phone: `0903 428 6339`
- Email: `hello@joons-me.com` (placeholder — confirm if real)

## What I need you to do next
1. Review `index.html` as-is and confirm you understand the design system above before changing anything.
2. Wire up the contact form to [Resend / your chosen provider — fill in before handing to Claude Code].
3. Replace placeholder portfolio and testimonial content with real data (ask me for it if you don't have it).
4. Add a real favicon and social share meta tags (Open Graph / Twitter card) using the JOONS-ME wordmark/colors.
5. Do a pass for accessibility: verify color contrast on the terminal panel's muted text, confirm all interactive elements are keyboard-reachable, and confirm the `prefers-reduced-motion` fallback (already partially handled) fully disables the typing animation and hover-lift transitions.
6. [Optional] If this needs to move from a single static file to a framework (Next.js, plain multi-page HTML, etc.), ask me which before restructuring — don't assume.

Keep every future change consistent with the token system and signature elements above — this is a distinctive design direction, not a generic template, and should stay that way.
