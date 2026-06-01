# Variant E: Minimalist Editorial (Dark Sage & Editorial Typography Style)

> Vibe: Quiet, intellectual, professional, minimalist, highly structured.
> Best for: Marketing playbooks, industry trends, opinion editorials, growth frameworks, minimalist text guides.

This style features a clean light stone cover slide with thin inset borders and a speech-bubble curve motif, followed by deep dark sage green content slides with typewriter-esque serif body copy, thin SVG process diagrams, and faint background line watermarks.

---

## 1. Palette & Theme Tokens

- **Cover Backdrop:** `#EAE8E4` (light stone / grey-cream)
- **Cover Text:** `#0C0C0B` (dark charcoal)
- **Content Backdrop:** `#131A17` (deep forest/sage black)
- **Primary Text:** `#FAF6F0` (warm off-white) on dark slides
- **Secondary Accent:** `#689A8F` (soft sage teal) — used for headers and step numbers
- **Muted text:** `rgba(250, 246, 240, 0.4)`
- **Border Frame:** `rgba(12, 12, 11, 0.15)` on light; `rgba(250, 246, 240, 0.1)` on dark
- **Primary Font:** `Lora` (Serif) — used for display headings, typewriter lists, and body copy
- **Secondary Font:** `Inter` (Sans-Serif) — used for labels, metadata, and diagram annotations

---

## 2. Key Components & CSS Implementations

### A. Inset Border Frame
An outer container border inset by `32px` with a decorative speech-bubble circle subtraction in the top-right corner.
```css
.inset-frame {
  position: absolute;
  top: 32px; bottom: 32px;
  left: 32px; right: 32px;
  border: 1px solid #2C2C2A;
  pointer-events: none;
  z-index: 5;
}
/* Speech bubble curve in top-right corner */
.corner-curve {
  position: absolute;
  top: 0; right: 0;
  width: 140px; height: 140px;
  border-left: 1px solid #2C2C2A;
  border-bottom: 1px solid #2C2C2A;
  border-bottom-left-radius: 140px;
  background: #EAE8E4;
}
```

### B. Typewriter Serif Lists
List elements styled like classic typewritten manuscripts using hyphens instead of traditional bullets.
```css
.typewriter-list {
  list-style: none;
  font-family: 'Lora', serif;
  font-size: 22px;
  color: #FAF6F0;
  line-height: 1.6;
}
.typewriter-list li {
  padding-left: 24px;
  position: relative;
  margin-bottom: 16px;
}
.typewriter-list li::before {
  content: '-';
  position: absolute;
  left: 0;
  color: rgba(250, 246, 240, 0.6);
}
```

### C. Clean Loop Diagrams
Process loops built with thin SVG arrows and minimal rectangular container boxes.
```css
.loop-container {
  position: relative;
  width: 100%;
  height: 380px;
  margin-top: 40px;
}
.loop-box {
  border: 1.5px solid #689A8F;
  background: transparent;
  padding: 16px 24px;
  border-radius: 4px;
  color: #FAF6F0;
}
.loop-box .label {
  font-family: 'Inter', sans-serif;
  font-size: 14px;
  font-weight: 700;
  color: #689A8F;
  text-transform: uppercase;
}
```

### D. Interactive Share Button
A dark grey rectangular button positioned at the bottom right of text-heavy slides to invite engagement.
```css
.share-action-button {
  background: #2C2C2A;
  border: 1.5px solid rgba(250, 246, 240, 0.15);
  border-radius: 4px;
  padding: 14px 28px;
  color: #FAF6F0;
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 1px;
  display: inline-flex;
  align-items: center;
  gap: 12px;
  cursor: pointer;
  transition: all 0.2s ease;
}
.share-action-button:hover {
  background: #689A8F;
  color: #131A17;
}
```

---

## 3. Recommended Slide Types & Layouts

### 1. Minimalist Cover (Slide 1)
- **Background:** Light stone grey (`#EAE8E4`).
- **Border Frame:** Thin inset border with a top-right speech-bubble cutout.
- **Typography:** Giant centered serif heading (e.g. `5 Marketing Trends that is Dominating 2026`) using Lora serif.
- **Accents:** Faint thin lines at the top-left and bottom-left, with a solid black dot `●` at the bottom-right corner inside the frame.

### 2. Typewriter Step Slide (Slides 2-5)
- **Background:** Deep sage black (`#131A17`).
- **Header:** Author name on the left, handle on the right.
- **Headline:** Bold Sage Green title (e.g. `1. COMMUNITY FOCUS`).
- **Visual Content:** Typewriter list explaining the concepts, followed by a minimal process diagram (Figma/writecream mockup or SVG cycle diagram).
- **Accents:** Faint feather quill pen watermark line art in the background.

### 3. Shareable Quote Slide (Slide 6)
- **Background:** Deep sage black.
- **Visual Center:** A centered, italicized serif quote in larger font size.
- **Interactive Element:** Bottom-right `SHARE` button.

---

## 4. Anti-Patterns to Avoid

- ❌ **No Heavy Graphics on Cover:** The cover slide must remain strictly typographic. Avoid adding visual screenshots or large colored tags here.
- ❌ **No Overuse of Color:** Limit colors to Stone Grey, Sage Black, Sage Teal, and Off-White. Do not introduce standard orange or coral accents into this variant.
- ❌ **No Centered Lists:** Keep typewriter lists left-aligned to mimic the layout of a real manuscript.
