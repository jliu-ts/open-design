# Variant C: Skeuomorphic Board (Pinboard & UI Mockup Style)

> Vibe: Hand-crafted, tactile, skeuomorphic, highly creative, clean.
> Best for: Design showcases, tutorials, visual guides, interactive frameworks, "how-to" articles.

This style features a warm cream pinboard backdrop, high-contrast hand-drawn borders, tilted elements, physical sticky notes, floating mockups, and infographic panels.

---

## 1. Palette & Theme Tokens

- **Backdrop Canvas:** `#FAF6F0` (warm soft cream)
- **Primary Text:** `#2C2C2A` (Charcoal) — never pure black
- **Brand Accent 1 (Coral):** `#D85A30` (warm coral red) — used for hooks, highlighted words
- **Brand Accent 2 (Peach):** `#F0997B` (softer orange-peach) — used for accents, badges, sticky notes
- **Grid Pattern:** A subtle graph paper mesh overlay
  ```css
  background-color: #FAF6F0;
  background-image: 
    linear-gradient(rgba(44, 42, 40, 0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(44, 42, 40, 0.03) 1px, transparent 1px);
  background-size: 40px 40px;
  ```

---

## 2. Key Components & CSS Implementations

### A. Hand-Drawn Borders & Outlines
Title cards, frames, and badges are wrapped in thick, slightly irregular borders that look hand-sketched.
```css
.hand-drawn-box {
  border: 3px solid #2C2C2A;
  border-radius: 16px 12px 18px 15px; /* Irregular border radius creates a hand-drawn feel */
  background: #FFFFFF;
  box-shadow: 4px 6px 0px rgba(44, 42, 42, 0.08); /* Solid offset shadow */
  padding: 24px;
}
```

### B. Pinboard Sticky Notes
Tilted sticky notes with pin points representing annotations or highlights.
```css
.sticky-note {
  background: #FFF9E6; /* Light yellow sticky note */
  border: 2px solid #2C2C2A;
  box-shadow: 3px 5px 12px rgba(44, 42, 42, 0.08);
  padding: 20px;
  width: 240px;
  position: relative;
  transform: rotate(-3deg);
}
.sticky-note.peach { background: #FFE8E0; transform: rotate(2deg); }
.sticky-note.white { background: #FFFFFF; transform: rotate(-1deg); }

/* Pushpin at top center */
.sticky-note::before {
  content: '';
  position: absolute;
  top: -8px; left: 50%;
  transform: translateX(-50%);
  width: 14px; height: 14px;
  border-radius: 50%;
  background: #D85A30;
  border: 2px solid #2C2C2A;
  box-shadow: 0 2px 4px rgba(0,0,0,0.15);
}
```

### C. Floating UI Cards
Clean overlay cards layered on top of each other at angles to simulate a stack of visual mockups.
```css
.card-stack {
  position: relative;
  height: 400px;
  width: 100%;
}
.card-mockup {
  position: absolute;
  width: 320px;
  height: 420px;
  background: #FFFFFF;
  border: 2px solid #2C2C2A;
  border-radius: 12px;
  padding: 28px;
  box-shadow: 4px 8px 24px rgba(44, 42, 40, 0.08);
  transition: transform 0.3s ease;
}
/* Visual offsets in stack */
.card-mockup:nth-child(1) { transform: rotate(-6deg) translate(-40px, 0); z-index: 3; }
.card-mockup:nth-child(2) { transform: rotate(1deg) translate(20px, 10px); z-index: 2; background: #2C2C2A; color: #FFFFFF; }
.card-mockup:nth-child(3) { transform: rotate(5deg) translate(80px, 20px); z-index: 1; }
```

### D. Tactile Pill Badges
Used for categories, tags, or word clouds.
```css
.tactile-pill {
  display: inline-block;
  font-size: 16px;
  font-weight: 700;
  text-transform: uppercase;
  color: #2C2C2A;
  background: #FAF6F0;
  border: 2px solid #2C2C2A;
  border-radius: 50px;
  padding: 8px 18px;
  box-shadow: 2px 3px 0px rgba(44, 42, 42, 0.1);
  margin: 4px;
}
.tactile-pill.active {
  background: #D85A30;
  color: #FFFFFF;
}
```

### E. Perfectly Aligned Brand Footers
Footers use flex alignment to ensure decorative stars do not overlap or sit awkwardly below the text baseline. Includes custom micro-interactions on hover.
```css
.slide-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 10;
}
.footer-text {
  font-size: 18px;
  font-weight: 700;
  color: #73706B; /* Premium soft charcoal with 4.5:1+ contrast against cream */
  display: inline-flex;
  align-items: center;
  gap: 8px;
  cursor: pointer;
  user-select: none;
}
.footer-star {
  font-size: 24px;
  color: #F0997B;
  line-height: 1;
  margin-top: -2px; /* Optical adjustment to center the star vertically */
  transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275), color 0.3s ease;
  display: inline-block;
}
.footer-text:hover .footer-star {
  transform: scale(1.25) rotate(72deg);
  color: #BE3E14; /* Accent color change on hover */
}
```

### F. Skeuomorphic Lift Transitions
Adding interactive hover transformations to floating elements (cards and sticky notes) to make the canvas feel alive when hovered.
```css
.card-mockup, .sticky-note {
  transition: transform 0.3s cubic-bezier(0.165, 0.84, 0.44, 1), box-shadow 0.3s ease;
}
.card-mockup:hover {
  transform: scale(1.05) translateY(-15px) rotate(0deg) !important;
  z-index: 15;
  box-shadow: 12px 24px 48px rgba(44, 44, 42, 0.16);
}
.sticky-note:hover {
  transform: scale(1.04) translateY(-8px) rotate(0deg) !important;
  z-index: 20;
  box-shadow: 8px 16px 32px rgba(44, 44, 42, 0.15);
}
```

---

## 3. Recommended Slide Types & Layouts

### 1. The Skeuomorphic Hook (Cover)
- **Layout:** High-contrast hand-drawn frame at the top: `HOW TO USE POSTHOG FOR CUSTOM AI` with coral text. A large subtitle below it.
- **Centerpiece:** A stacked card-mockup stack (`.card-stack`) sitting in the center third, showing 3 tilted cards stacked.
- **Background:** Graph paper grid with orange-red accent dots/stars.

### 2. The Moodboard Slide
- **Layout:** A grid showing 4–6 small styled modules representing content blocks (sticky notes, solid color blocks, screenshot outlines, word clouds).
- **Instruction:** Keep text minimal inside each block, mimicking index cards on a wall.

### 3. The "Correct vs Incorrect" Slide
- **Layout:** Split-screen layout.
  - Left/Top (Incorrect): A red border frame with a red `X` badge, showing messy, verbose text.
  - Right/Bottom (Correct): A green border frame with a green checkmark badge, showing structured, beautifully styled outline text alongside a moodboard illustration.
- **Vibe:** Highly instructional, actionable.

---

## 4. Anti-Patterns to Avoid

- ❌ **No Flat Digital Gradients:** Avoid standard UI gradients. Use solid warm overlays or textured-feeling backdrops.
- ❌ **No Sharp Digital Cards:** Avoid clean, borderless cards. Cards must have a thin, dark outline (`#2C2C2A`) and physical drop-shadow offsets.
- ❌ **No Centered Paragraphs:** Keep body text left-aligned inside sticky notes and card modules.
- ❌ **No Dense Copy:** Keep text blocks extremely brief (15-20 words max per block). Let the visual layout (sticky notes, stacked cards) do the storytelling.
- ❌ **No Competitor/Platform Branding:** Never output "Claude Design", "Claw Design", "Claude", or "Made with Claude Design" as header handles, footer tags, or signatures. All slides must use the current brand handle (e.g., `@trendingsociety`) as specified in DESIGN.md.
