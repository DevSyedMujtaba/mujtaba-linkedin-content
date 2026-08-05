# Template Library

Fill one template per day. Do not invent new layouts unless adding a permanent sixth template.

## Brand constants (every graphic)

- Format: square 1:1 LinkedIn
- Colors: dark navy/white base; concept accents (blue/red/green as needed)
- Series pill: top-left, short ALL CAPS or Title Case
- Title: large, bold; color-code compared terms when using Compare
- Subtitle: 1–2 lines max
- Footer left: **Mujtaba Bukhari** · Backend Focused Full Stack Developer  
  Stack line: `Node.js • Koa.js • TypeScript • MySQL • APIs`
- Footer right: Save this post for later!
- No clutter: max one main diagram idea

---

## 1. Compare

**Use for:** Salt vs Pepper, JWT vs Session, Index vs Full scan, etc.

**Zones:**
1. Series pill + title (`A` vs `B`) + subtitle
2. Left column (accent A): definition bullets + mini example
3. Right column (accent B): definition bullets + mini example / code
4. Optional bottom: “How they work together” or “Why both?”
5. Takeaway box + footer

**Fill fields:** series, titleA, titleB, subtitle, leftHeader, leftBullets[4], leftExample, rightHeader, rightBullets[4], rightExample, togetherSteps?, takeaway

---

## 2. How-it-works

**Use for:** request lifecycle, auth flow, deploy pipeline.

**Zones:**
1. Series + title + subtitle
2. 4–5 numbered steps in a flow
3. One “gotcha” callout
4. Footer

**Fill fields:** series, title, subtitle, steps[{label, detail}], gotcha, takeaway

---

## 3. Mistake vs Fix

**Use for:** anti-patterns from real backend/frontend work.

**Zones:**
1. Series + title
2. Left “Mistake” (red): code or bullets
3. Right “Fix” (green): code or bullets
4. Why it matters (1 line)
5. Footer

**Fill fields:** series, title, mistakeTitle, mistakeBody, fixTitle, fixBody, whyItMatters

---

## 4. Code tip

**Use for:** one sharp tip with a short snippet.

**Zones:**
1. Series + title + subtitle
2. Large code block (8–12 lines max)
3. 3 bullet “why this helps”
4. Takeaway + footer

**Fill fields:** series, title, subtitle, code, bullets[3], takeaway

---

## 5. Builder journal

**Use for:** shipped / broke / fixed from real work (sanitized).

**Zones:**
1. Series pill: BUILDER LOG
2. Title = outcome in plain language
3. Three blocks: Context → Problem → Fix
4. Lesson (1 line)
5. Footer

**Fill fields:** title, context, problem, fix, lesson

---

## Weekly rotation (default)

| Day | Template bias |
|-----|----------------|
| Mon | Compare or How-it-works |
| Tue | Code tip |
| Wed | Builder journal |
| Thu | Mistake vs Fix |
| Fri | Compare or How-it-works |
| Sat | Code tip (lighter) |
| Sun | Builder journal or soft opportunity |
