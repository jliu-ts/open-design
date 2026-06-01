# Variant A: Dark Editorial

> Vibe: High-impact, technical, dark-mode, authoritative, clean.
> Best for: SaaS metrics, product infrastructure, business analytics, hard tech news.

This style features near-black backgrounds, high-contrast white headlines, orange highlights, hand-drawn vector arrows, solid orange index boxes, and a low text density.

---

## 1. Palette & Theme Tokens

- **Backdrop Canvas:** `#0A0A0A` (Near Black)
- **Primary Text:** `#FFFFFF` (White)
- **Accent Color:** `#F97316` (Brand Orange)
- **Secondary Text:** `rgba(255, 255, 255, 0.7)` (Muted white)
- **Handle/Metadata:** `rgba(255, 255, 255, 0.35)`
- **Warm Backdrop Gradient:** 
  ```css
  background: linear-gradient(160deg, #080808 0%, #0D0B0C 50%, #0A0808 100%);
  ```

---

## 2. Key Components & CSS Implementations

### A. Solid Index Badges
Used to demarcate slides chronologically.
```css
.badge {
  width: 64px;
  height: 64px;
  background: #F97316;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 26px;
  font-weight: 800;
  color: #FFFFFF;
  border-radius: 0px; /* Sharp edges */
}
```

### B. Billboard Headlines
Commanding, uppercase, and compact (max 5-6 words).
```css
.headline {
  font-size: 78px;
  font-weight: 900;
  color: #FFFFFF;
  line-height: 1.05;
  letter-spacing: -2px;
  text-transform: uppercase;
}
.headline .hl {
  color: #F97316; /* Highlight keyword in orange */
}
```

### C. Bold Takeaway Callouts
Contrast boxes to highlight actionable insights.
```css
.callout {
  background: #F97316;
  padding: 24px 32px;
  align-self: flex-start;
  max-width: 640px;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.5);
}
.callout.outline {
  background: transparent;
  border: 3px solid #F97316;
}
.callout-text {
  font-size: 24px;
  font-weight: 700;
  color: #FFFFFF;
  line-height: 1.3;
}
```

### D. Vector Doodle Arrows
Used to direct the eye to the callout box.
```html
<svg class="doodle-arrow" style="width: 120px; height: 100px;" viewBox="0 0 100 100" fill="none">
  <path d="M10,80 Q50,90 80,20 Q85,15 90,10 M75,15 L90,10 L88,28" stroke="#F97316" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
```

---

## 3. Recommended Slide Layouts

### 1. Hook (Cover) Slide
- Headline at 92px uppercase, centered or bottom-anchored.
- Orange tag above headline (e.g. `AI INFRASTRUCTURE`).
- Subtitle in muted white (`rgba(255,255,255,0.6)`) at 26px.
- Background uses a subtle grid overlay or floating UI frames.

### 2. Billboard Point Slide
- Top header with social handle (`@trendingsociety`) and counter (`2/6`).
- Solid orange index badge.
- Huge uppercase headline (e.g. `YOUR DATA BUILDS THEIR BRAIN`).
- Doodle arrow pointing to a solid orange callout block with a 1-line takeaway.

### 3. Stat Slide
- Giant centered number (`180px` weight 900) with a glow effect:
  `text-shadow: 0 0 60px rgba(249, 115, 22, 0.2);`
- Orange category label (`SOVEREIGN AI`).
- Brief caption (26px) underneath.

---

## 4. Anti-Patterns to Avoid

- ❌ **No Rounded Corners:** All container boxes and badges must have sharp edges (0px border-radius) except the accent line (3px).
- ❌ **No Centered Paragraphs:** Keep body text left-aligned.
- ❌ **No Text Overload:** Keep the copy extremely minimal. Slides should feel like billboards.
- ❌ **No Multiple Colors:** Only use white, orange `#F97316`, and black `#0A0A0A`.
