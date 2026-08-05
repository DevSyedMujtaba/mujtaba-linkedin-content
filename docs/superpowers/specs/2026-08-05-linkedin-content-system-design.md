# LinkedIn Content System — Design

**Date:** 2026-08-05  
**Creator:** Syed Mujtaba Bukhari  
**Positioning:** How real production systems work (senior-friendly; keep select high-leverage basics)  
**Approach:** Template library + daily fill (Approach 2)  
**Calendar:** `docs/90-day-content-calendar.md` (v3 — system design / production pillars)

## Goal

Build authority as a full-stack / SaaS engineer first; surface hire/freelance opportunities second. Daily LinkedIn posts. Voice: builder journal + teacher.

## Daily deliverable

Each day the content creator sends a **post pack**:

1. Ready-to-post LinkedIn caption (hook, body, CTA, hashtags)
2. One polished square graphic filled into a locked template
3. Which template was used + series name

Mujtaba posts it the same day.

## Platforms

- **Primary:** LinkedIn only (v1)
- Instagram deferred until LinkedIn rhythm is stable

## Audience mix

- Mostly other developers (engagement, follows, shares)
- Occasional posts aimed at recruiters / founders

## Content pillars (weekly mix)

Driven by the **90-day calendar** in `docs/90-day-content-calendar.md`.

Core series: System Design Simplified · Production Lessons · Backend Deep Dives · Database Mastery · Building SaaS at Scale  
Supporting: Security Engineering · Distributed Systems · AI for Backend · Engineering Mindset · Frontend for Backend Engineers

| Voice mix | Cadence | Templates |
|-----------|---------|-----------|
| Teacher (production depth) | most days | Compare, How-it-works, Mistake vs Fix, Code tip |
| Builder journal / case study | ~1–2 / week | Builder journal |
| Soft opportunity | Days 87–90 | Builder journal |

## Visual brand (locked from Salt vs Pepper example)

- Clean educational infographic, dark blue + white base
- Accent colors per concept (e.g. blue vs red for comparisons)
- Top-left series pill/tag
- Bold title; short subtitle
- Structured teach zones (columns, flow, or code block)
- Footer: headshot optional; **Mujtaba Bukhari** · Backend Focused Full Stack Developer · `Node.js • Koa.js • TypeScript • MySQL • APIs`
- Soft CTA: “Save this post for later!”
- Square 1:1 for LinkedIn

## Template library (5 layouts)

See `templates/README.md` for fill rules.

1. **Compare** — X vs Y (two columns + optional “how they work together”)
2. **How-it-works** — numbered horizontal/vertical flow
3. **Mistake vs Fix** — wrong pattern left, correct pattern right
4. **Code tip** — one idea + code block + takeaway
5. **Builder journal** — what shipped / broke / fixed + one lesson

## Series names

Use calendar series labels on the graphic pill (e.g. SYSTEM DESIGN SIMPLIFIED, DATABASE MASTERY).

## Constraints

- No confidential Occy / client data — sanitize product details
- Prefer accurate technical claims; include small code only when correct
- Frame posts as production systems / architecture / failure modes; keep select high-leverage basics
- Daily quality over complexity: use simpler template fills when needed
## Success signals (4–6 weeks)

- Consistent daily posting
- Saves + comments from developers
- Profile visits / connection requests from relevant people
- Clear visual recognition of the template family
