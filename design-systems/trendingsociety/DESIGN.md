# Trending Society

> Category: Media & Publishing
> AI-powered content platform. Dark editorial aesthetic with orange accents — authoritative, trend-forward, premium.

## 1. Visual Theme & Atmosphere (Multi-Variant Brand System)

Trending Society uses two distinct visual variants (themes) depending on the content type and storytelling mode. Both variants maintain the core brand identity while shifting the background, readability, and content density to match the format.

### Variant A: Dark Editorial (Default)
- **Vibe:** Urgent, technical, premium, commanding. Inspired by high-end dark dashboards and editorial publications.
- **Canvas:** Near-black background (`#0A0A0A`) with stark white primary text and brand orange (`#F97316`) as a sharp accent color.
- **Content Style:** Billboard-style headlines (3-5 words), low text density, high visual impact.
- **Key Elements:** Solid orange square badges for indices (e.g., "01"), accent bars above titles, hand-drawn vector arrow doodles, and "Save this post" CTAs.
- **Best For:** Hard news, SaaS metrics, infrastructure deep dives, product releases.

### Variant B: Warm Cream Blueprint (Educational)
- **Vibe:** Academic, structured, trustworthy, highly legible. Inspired by YC Blueprints and expert case studies.
- **Canvas:** Warm cream/linen background (`#F5F0EB`) with dark charcoal primary text (`#1C1917`) and brand orange (`#F97316`) for labels and accents.
- **Content Style:** Paragraph-heavy editorial layout, structured bullets, bold text for scannability, and high density.
- **Key Elements:** Huge faded watermark index numbers behind headlines (`rgba(0,0,0,0.04)`), italicized orange thesis statements below headlines, bullet lists starting with `→`, "KEY TAKEAWAY" zones, and rounded outline pills at the bottom.
- **Best For:** Frameworks, guides, YC analysis, step-by-step blueprints, checklists.

---

## 2. Color Palette & Roles

### Variant A (Dark Editorial) Colors
- **Canvas Background:** `#0A0A0A` (Near Black)
- **Primary Text:** `#FFFFFF` (White)
- **Secondary Text:** `rgba(255, 255, 255, 0.7)`
- **Muted/Social Handle:** `rgba(255, 255, 255, 0.35)`
- **Accent Indicator:** `#F97316` (Brand Orange)
- **Pills/Badges:** `#F97316` background with white text, or solid white outline
- **Callout boxes:** Solid brand orange (`#F97316`) or dark orange outline

### Variant B (Warm Cream Blueprint) Colors
- **Canvas Background:** `#F5F0EB` (Warm Cream / Linen)
- **Primary Text/Headline:** `#1C1917` (Dark Charcoal)
- **Body Text:** `rgba(28, 25, 23, 0.8)` (Charcoal at 80% opacity)
- **Italic Thesis Statement:** `#F97316` (Brand Orange)
- **Muted/Social Handle:** `rgba(28, 25, 23, 0.4)` (Charcoal at 40% opacity)
- **Ghost Number Background:** `rgba(28, 25, 23, 0.04)` (Very faint charcoal)
- **Outline Pills:** Transparent background with `1.5px solid rgba(28, 25, 23, 0.15)` border and `rgba(28, 25, 23, 0.65)` text
- **Takeaway Label:** `rgba(28, 25, 23, 0.35)` uppercase

---

## 3. Typography Rules

### Font Family
- **Universal Typeface:** `Inter`, fallback: `-apple-system, BlinkMacSystemFont, sans-serif`
- **No secondary fonts** — hierarchy is created entirely through variations in weight (400 to 900), size, color, and italics.

### Typographic Hierarchy

| Role | Size | Weight | Line Height | Case & Style | Variant Usage |
|------|------|--------|-------------|--------------|---------------|
| Hook Headline | 76px | 800 | 1.06 | Mixed, bold | Both (Variant A: White / Variant B: Charcoal) |
| Slide Headline | 68px | 800 | 1.06 | Mixed, bold | Both (Variant A: White / Variant B: Charcoal) |
| Section Category | 17px | 800 | Normal | Uppercase, +3px spacing | Both (Orange) |
| Secondary Label | 15px | 600 | Normal | Uppercase, +2px spacing | Both (Muted color) |
| Thesis Statement | 22px | 500 | 1.50 | Italic, orange | Variant B (Cream) |
| Body Text | 24px | 400 | 1.65 | Left-aligned | Both (Variant A: 70% White / Variant B: 80% Charcoal) |
| Bullet Items | 23px | 400 | 1.55 | Left-aligned | Both |
| Takeaway Label | 14px | 700 | Normal | Uppercase, +2px spacing | Variant B |
| Takeaway Text | 22px | 700 | 1.40 | Bold, dark | Variant B |
| Outline Pills | 17px | 500 | Normal | Mixed | Variant B |
| Ghost Watermark | 360px | 900 | 1.00 | Giant number | Variant B (`rgba(28,25,23,0.04)`) |

---

## 4. Component Stylings & Layout Elements

### Index Badges (Variant A)
- **Style:** Solid orange square (`#F97316`), `64px × 64px`, containing index (e.g. "01", "02").
- **Positioning:** Placed at the top-left or top-right, aligned with guidelines.

### Ghost Numbers (Variant B)
- **Style:** Giant font (`360px`), color `rgba(28,25,23,0.04)`, absolute positioned in the top-right quadrant, sliding behind the headline.

### Thesis Line (Variant B)
- **Style:** Italicized orange text (`#F97316`) positioned directly below the headline. Introduces the core slide concept in 10-15 words.

### Bullet Points
- **Variant B Style:** Prefixed with a muted arrow character `→` (color `rgba(28,25,23,0.35)`). List items left-aligned with `padding-left: 28px`.

### Key Takeaway Box (Variant B)
- **Style:** Clean spacing, labeled `KEY TAKEAWAY →` in muted uppercase text. Below it, the takeaway sentence is in bold primary text. Below that, a flex row of rounded outline pill tags containing keyword themes.

### Brand Footer & Social Handle
- **Variant A Footer:** Subtle strip at the bottom containing dark/white handle (`@trendingsociety`) and URL.
- **Variant B Footer:** Bottom centered text `Give your AI as much context as you'd give a new employee.` (in thin italic light grey) or context-specific teaser.
- **Social Handle:** Positioned at the top-left or bottom-left depending on page layout, opacity set to 40%.

### Swipe Cues
- **Text:** `SWIPE →` or `SWIPE` with a bold arrow in accent orange.
- **Slide Counters:** `3/10` or `2/7` in a pill container. Variant A uses a white circle/pill on dark; Variant B uses a black circle/pill on cream.

---

## 5. Layout & Grid Systems

### Canvas Specs
- **Dimensions:** Exactly `1080px × 1350px` (Instagram 4:5 portrait frame).
- **Margins:** Outer margins are `64px` on left/right and `80px` on top/bottom to ensure safety from UI overlays.

### Alignment Philosophy
- **Alignments:** Left-align all headlines and body text blocks (never center-align paragraphs).
- **Vertical Centering:** Content sections are grouped and vertically centered in the safe zone of the slide.
- **Visual Rhythm:** Use alternating slide structures. Do not repeat the exact same layout (e.g., bullet list, paragraph list, quote, stat) on consecutive slides.

---

## 6. Depth & Elevation
- **Variant A:** Subtle dark gradients behind text (`linear-gradient(160deg, #080808 0%, #0D0B0C 50%, #0A0808 100%)`) to prevent the background from feeling sterile.
- **Variant B:** Warm solid backdrop (`#F5F0EB`) with absolute-positioned elements (faint ghost number at z-index 1, text content at z-index 2) creating physical layers.

---

## 7. Do's and Don'ts

### Do
- Left-align all text content blocks.
- Bold key insights within body text paragraphs to enable rapid reading scan.
- Maintain the designated color boundaries (never introduce blue, green, etc.).
- Ensure every slide has the top-left handle (`@trendingsociety`) and top-right counter (e.g. `2/7`).
- Tease the next slide's question or topic at the very bottom of content slides.

### Don't
- Don't mix Variant A (dark) and Variant B (cream) content slides in the same deck. Keep the deck cohesive (either all Variant A or a structured sequence: Dark Hook → Cream Content → Dark CTA).
- Don't write more than 40 words of body text on a single slide.
- Don't use generic bullet circles; use the customized arrow `→` bullets.
- Don't use drop shadows on text unless it's a headline overlaying an image.
- Don't use emojis in body copy. Emojis can only be used as single icon highlights in dedicated pill badges.

---

## 8. Responsive Behavior
- **Fixed Frame:** All outputs are rendered at exactly `1080px × 1350px` layout templates. No resizing is required.
- **Export Formats:** PNG files must be screenshotted at 1x or 2x resolution (`2160px × 2700px` for high-density displays).

## 9. Agent Prompt Guide

### Quick Color Reference
- Primary text: `#FFFFFF`
- Brand accent: `#F97316` (orange)
- Body text: `rgba(255,255,255,0.7)`
- Muted text: `rgba(255,255,255,0.3)`

### Slide Construction Pattern
Every slide in a carousel follows this skeleton:
```html
<div style="width:1080px; height:1350px; background:#0A0A0A; position:relative; overflow:hidden; padding:64px;">
  <!-- Logo badge: top-left -->
  <!-- Slide counter: top-right -->
  <!-- Optional: faded index number (300px, 6% opacity) -->
  <!-- Content: headline + body, vertically positioned -->
  <!-- Optional: accent bar above headline -->
</div>
```

### Example Slide Prompts
- "Create a hook slide: full-bleed background image with bottom gradient overlay. Headline at 64px Inter weight 800, white, anchored to lower third. Logo top-left, counter top-right. Orange accent bar above headline."
- "Create a key point slide: warm gradient background. Faded '02' at 300px behind content. Headline at 52px weight 700, body at 30px weight 400 rgba(255,255,255,0.7). Content centered vertically."
- "Create a stat slide: centered stat number at 120px weight 800 with orange glow. Label at 32px weight 500 below. Minimal — number is the hero."
- "Create a CTA slide: 'Follow @trendingsociety' at 48px weight 700. Three benefit bullets with checkmarks. White pill button at bottom. Logo and counter as usual."

### Iteration Guide
1. Start with the darkest possible background — slides should feel like they emerge from darkness
2. One idea per slide — if you're writing more than 2 sentences, split into multiple slides
3. The accent bar is the only splash of color — use it to mark the start of content
4. Stat numbers should feel like they take over the slide — 120px is not too big
5. The faded index numbers are a signature detail — use them on point slides for depth
6. CTA slides should feel like an invitation, not a command — white button, not orange
