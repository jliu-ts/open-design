# Variant B: Warm Cream Blueprint

> Vibe: Educational, editorial, structured, academic, trustworthy.
> Best for: Case studies, frameworks, checklists, guidebooks, step-by-step blueprints.

This style features a warm cream background, high-readability charcoal body text, giant ghost watermarks behind headlines, orange italicized thesis taglines, bullet points with `→`, and takeaway blocks.

---

## 1. Palette & Theme Tokens

- **Backdrop Canvas:** `#F5F0EB` (Warm Cream / Linen)
- **Primary Text/Header:** `#1C1917` (Dark Charcoal)
- **Body Text:** `rgba(28, 25, 23, 0.8)` (Charcoal at 80% opacity)
- **Thesis Highlight:** `#F97316` (Brand Orange)
- **Muted Text:** `rgba(28, 25, 23, 0.4)` (Charcoal at 40% opacity)
- **Ghost Number Background:** `rgba(28, 25, 23, 0.04)` (Charcoal at 4% opacity)

---

## 2. Key Components & CSS Implementations

### A. Ghost Index Watermarks
Giant index numbers positioned absolute, sitting behind and slightly offset from the main headline text.
```css
.ghost-num {
  position: absolute;
  font-size: 360px;
  font-weight: 900;
  line-height: 1;
  color: rgba(28, 25, 23, 0.04);
  z-index: 1;
  user-select: none;
  pointer-events: none;
  top: 40px;
  right: -10px;
}
```

### B. Orange Thesis Statement
An italicized sentence positioned directly below the headline summarizing the key concept.
```css
.thesis {
  font-size: 22px;
  font-weight: 500;
  color: #F97316;
  font-style: italic;
  line-height: 1.5;
  margin-bottom: 36px;
  max-width: 780px;
}
```

### C. Custom Bullet Pointers
Clean list elements using an arrow character.
```css
.bullet-list {
  list-style: none;
  max-width: 780px;
}
.bullet-list li {
  font-size: 23px;
  font-weight: 400;
  color: rgba(28, 25, 23, 0.8);
  line-height: 1.55;
  padding: 8px 0 8px 28px;
  position: relative;
}
.bullet-list li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: rgba(28, 25, 23, 0.35);
  font-weight: 500;
}
```

### D. Key Takeaway Blocks
A footer-anchored block wrapping up the core slide message, flanked by tag pills.
```css
.key-takeaway {
  margin-top: 32px;
}
.kt-label {
  font-size: 14px;
  font-weight: 700;
  color: rgba(28, 25, 23, 0.35);
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-bottom: 6px;
}
.kt-text {
  font-size: 22px;
  font-weight: 700;
  color: #1C1917;
  line-height: 1.4;
}
.pills {
  display: flex;
  gap: 10px;
  margin-top: 20px;
}
.pill {
  font-size: 17px;
  font-weight: 500;
  color: rgba(28, 25, 23, 0.65);
  padding: 10px 20px;
  border: 1.5px solid rgba(28, 25, 23, 0.15);
  border-radius: 100px;
  background: transparent;
}
```

---

## 3. Recommended Slide Layouts

### 1. Hook Slide (Dark Cover)
- Keep cover slide dark (Variant A style) for high visual stop-rate in feed, e.g. dark slate overlay over a relevant product screenshot.

### 2. Editorial Point Slide
- Top metadata: `@trendingsociety` handle, `2/7` counter badge.
- Giant ghost watermarked number (e.g. `01`).
- Orange principle label (`PRINCIPLE 01 / PROPRIETARY AI MODELS`).
- Clean charcoal headline.
- Orange italic thesis tagline.
- Paragraphs with bold keywords for scannability.
- Dedicated Takeaway container + outline pills.

### 3. FAQ / Breakdown Slide
- Large headline asking a reader-facing question.
- Orange divider line.
- Bullet points starting with `→` explaining the details.
- Footer teaser line: `How does PostHog handle your privacy?` (italic light grey) guiding to the next slide.

---

## 4. Anti-Patterns to Avoid

- ❌ **No Mixed Slide Themes:** Do not interleave dark content slides and cream content slides. Use a consistent canvas across all content slides.
- ❌ **No Centered Paragraphs:** Bullet points and text must be left-aligned.
- ❌ **No Text Overcrowding:** Keep body copy to a maximum of 40 words. Bold key phrases.
