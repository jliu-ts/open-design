# Variant D: Cinematic Editorial (Image Card & High-Impact Typography Style)

> Vibe: Immersive, dramatic, high-end editorial, visual-first, cinematic.
> Best for: AI agent workflows, software tutorials, visually rich stories, case studies, product breakdowns.

This style features rich color blocks per slide, rounded image/graphic cards with overlapping label pills, giant overlapping serif/sans-serif typography, and centered actionable takeaways beneath each visual block.

---

## 1. Palette & Theme Tokens

Each slide uses a specific, rich monochromatic or themed backdrop to separate sections:
- **Slide 1 (Cover):** Dark chocolate or crimson landscape background.
- **Slide 2 (Point 1):** Soft slate grey (`#D2D7D5`) with dark charcoal text.
- **Slide 3 (Point 2):** Warm olive-green (`#D1D4C2`) with dark charcoal text.
- **Slide 4 (Point 3):** Deep canyon brown (`#1E0C06`) with light cream text.
- **Primary Serif Font:** `Lora` (or Playfair Display) — used for key nouns and display italics.
- **Primary Sans-Serif:** `Inter` (weights 700–900) — used for secondary headlines and bold assertions.

---

## 2. Key Components & CSS Implementations

### A. Rounded Card Frames
A prominent centered image or graphic container with rounded edges, a thick border, and a solid shadow.
```css
.image-card-container {
  width: 100%;
  height: 520px;
  position: relative;
  margin-top: 40px;
}
.image-card {
  width: 100%;
  height: 100%;
  border: 3px solid #2C2C2A;
  border-radius: 32px;
  overflow: hidden;
  position: relative;
  box-shadow: 6px 8px 0px rgba(44, 44, 42, 0.15);
}
.image-card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```

### B. Overlapping Label Pills
A pill badge positioned absolutely at the top center of the card, bisecting the top border.
```css
.card-label-pill {
  position: absolute;
  top: -18px;
  left: 50%;
  transform: translateX(-50%);
  background: #FAF6F0;
  border: 3px solid #2C2C2A;
  border-radius: 100px;
  padding: 6px 20px;
  font-family: 'Inter', sans-serif;
  font-size: 14px;
  font-weight: 800;
  color: #2C2C2A;
  text-transform: uppercase;
  letter-spacing: 2px;
  z-index: 10;
}
```

### C. Large Overlay Display Typography
Typography layered directly inside the card over the image, using contrasting font weights and styles.
```css
.card-overlay-title {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 90%;
  text-align: center;
  z-index: 5;
  color: #FFFFFF;
}
.card-overlay-title .serif-word {
  font-family: 'Lora', serif;
  font-size: 72px;
  font-weight: 500;
  font-style: italic;
  display: block;
}
.card-overlay-title .sans-word {
  font-family: 'Inter', sans-serif;
  font-size: 80px;
  font-weight: 900;
  text-transform: uppercase;
  line-height: 0.9;
  letter-spacing: -2px;
}
```

### D. Tilted Handwritten Accent
A small cursive or script element rotated slightly to add a hand-designed annotation touch.
```css
.tilted-annotation {
  position: absolute;
  font-family: 'Lora', serif;
  font-style: italic;
  font-size: 28px;
  color: #FFFFFF;
  transform: rotate(-8deg);
  opacity: 0.9;
}
```

### E. Centered Under-Card Copy
Structured scannable paragraphs aligned centrally beneath the main card visual.
```css
.under-card-content {
  margin-top: 36px;
  text-align: center;
}
.under-card-headline {
  font-family: 'Inter', sans-serif;
  font-size: 34px;
  font-weight: 800;
  color: #2C2C2A;
  line-height: 1.25;
  margin-bottom: 12px;
}
.under-card-body {
  font-family: 'Inter', sans-serif;
  font-size: 20px;
  font-weight: 500;
  color: rgba(44, 44, 42, 0.7);
  line-height: 1.5;
  max-width: 820px;
  margin: 0 auto;
}
```

---

## 3. Recommended Slide Types & Layouts

### 1. The Cinematic Hook (Cover)
- **Background:** Full-bleed high-contrast photography or gradient artwork.
- **Top Header:** Brand logo and handle on the left, social destination checkmarks on the right.
- **Centerpiece Typography:** Large overlapping titles (`5 AI agents WE USE for our clients`) using a combination of Lora serif and Inter heavy sans-serif.
- **Actionable Tag:** Bottom-centered text banner inside a solid color block (e.g. `ACTUAL OPERATIONAL SYSTEMS` inside red `#BE3E14`).

### 2. Rounded Card Step Slide
- **Background:** Uniform solid color block (Slate, Olive, Chocolate) matching the slide theme.
- **Visual Center:** Card container with top-overlapping pill (`AGENT 02`). Inside the card, an evocative image overlaid with the step title.
- **Takeaway Text:** Centered bold headline + 2-sentence helper description beneath the card.

### 3. Integrated Process Summary (Slide 5)
- **Background:** Blurred gradient canvas.
- **Visual Layout:**
  - Large display headline: `How They Actually Work Together`
  - Two parallel sections comparing "Most people's workflow" with "Our workflow" using bullet pointers (`→`).
  - Solid takeaway box summarizing the connected system at the bottom.

### 4. The Brand CTA Slide (Final Slide)
- **Background:** Blurred gradient canvas.
- **Centerpiece Brand Logo:** A large solid red circle (`background: #BE3E14; border-radius: 50%; width: 220px; height: 220px;`) containing the white brand ribbon icon or stylized logo glyph, centered in the upper-middle third.
- **Main Heading:** "Curious how this actually looks in practice?" or "Save this post to your feed." (large bold white sans-serif, e.g. `font-size: 52px; font-weight: 800; margin: 32px 0 16px; text-align: center;`).
- **Centered Descriptive Call-to-Action:** Direct engagement prompt (e.g. `Share this with your team. Or drop a ⚡ if you want to see the agent prompts we use.`) in slightly smaller, clean white text (`font-size: 24px; font-weight: 500; opacity: 0.85; max-width: 760px; line-height: 1.5; margin: 0 auto;`).

---

## 4. Anti-Patterns to Avoid

- ❌ **No Overlapping Card Content:** Ensure overlapping title words inside the card have proper contrast against the background image. If the image is bright, add a subtle `background: rgba(0, 0, 0, 0.25)` overlay on the image.
- ❌ **No Multi-Color Grids:** Keep each slide's backdrop clean and monochromatic. Do not use noisy gradients under visual card steps.
- ❌ **No Small Text:** Body copy under cards should be easily readable at mobile scale (min 20px font size).
- ❌ **No Competitor/Platform Branding:** Never output "Claude Design", "Claw Design", "Claude", or "Made with Claude Design" as header handles, footer tags, or signatures. All slides must use the current brand handle (e.g., `@trendingsociety`) as specified in DESIGN.md.
