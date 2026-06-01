---
name: carousel-article
zh_name: "文章轮播 Carousel"
en_name: "Article Carousel"
emoji: "📱"
description: "Turn article content into a premium social media carousel. Supports dark-editorial, cream-blueprint, skeuomorphic-board, cinematic-editorial, and minimalist-editorial styles."
triggers:
  - "carousel"
  - "instagram carousel"
  - "linkedin carousel"
  - "social slides"
  - "article slides"
  - "social carousel"
category: marketing
scenario: social-media
aspect_hint: "4:5 portrait (1080×1350)"
tags: ["carousel", "social", "instagram", "linkedin", "article", "dark", "editorial", "blueprint", "board", "cinematic", "minimalist"]
od:
  mode: deck
  surface: web
  scenario: marketing
  design_system:
    requires: true
  preview:
    type: html
    entry: index.html
    reload: debounce-100
  example_prompt: "Create a carousel from this article in the minimalist-editorial style: thin inset frame stone-grey typographic cover transitioning to deep dark sage green content slides with typewriter Lora list copy, thin Sage loop SVGs, and bottom-right interactive SHARE buttons."
---

# Article Carousel Generator

Create a single-file HTML carousel from article content. Each slide is exactly **1080×1350px** (Instagram 4:5 portrait) safe zone. Output a keyboard-navigable deck optimized for screenshot export.

## Visual Design Variants

The generator supports five distinct styling variants. Select the variant requested in the prompt or choose the one best suited to the topic:

### 1. Dark Editorial (`dark-editorial`)
- **Vibe:** Technical, dashboard-style, dark mode, high impact.
- **Reference details:** See [style-dark-editorial.md](file:///Users/jeff/Documents/GitHub/trendingsociety/apps/open-design/skills/carousel-article/references/style-dark-editorial.md)
- **Use case:** Hard tech news, infrastructure metrics, data releases.

### 2. Warm Cream Blueprint (`cream-blueprint`)
- **Vibe:** Educational playbook, structured academic guide, highly readable.
- **Reference details:** See [style-cream-blueprint.md](file:///Users/jeff/Documents/GitHub/trendingsociety/apps/open-design/skills/carousel-article/references/style-cream-blueprint.md)
- **Use case:** Step-by-step guides, startup blueprints, checklists.

### 3. Skeuomorphic Board (`skeuomorphic-board`)
- **Vibe:** Skeuomorphic, tactile, creative, designer-handcrafted.
- **Reference details:** See [style-skeuomorphic-board.md](file:///Users/jeff/Documents/GitHub/trendingsociety/apps/open-design/skills/carousel-article/references/style-skeuomorphic-board.md)
- **Use case:** Design tutorials, creative brainstorming, moodboards, tool breakdowns.

### 4. Cinematic Editorial (`cinematic-editorial`)
- **Vibe:** High-end visual editorial, dramatic imagery, centered step takeaways.
- **Reference details:** See [style-cinematic-editorial.md](file:///Users/jeff/Documents/GitHub/trendingsociety/apps/open-design/skills/carousel-article/references/style-cinematic-editorial.md)
- **Use case:** AI workflows, step-by-step product visuals, branding narratives.

### 5. Minimalist Editorial (`minimalist-editorial`)
- **Vibe:** Quiet, intellectual, professional, minimalist, highly structured.
- **Reference details:** See [style-minimalist-editorial.md](file:///Users/jeff/Documents/GitHub/trendingsociety/apps/open-design/skills/carousel-article/references/style-minimalist-editorial.md)
- **Use case:** Marketing playbooks, industry trends, opinion editorials, growth frameworks.

---

## Content Structure & Layout

Regardless of the variant selected, build a logical narrative structure of 6-8 slides:
1. **Hook (Slide 1):** Provocative title (max 5-8 words). Accent colors, high contrast.
2. **Body Insights (Slides 2-5):** Alternating content layouts (Bullet list, Quote, Stat, Paragraph key point).
3. **takeaways (Slide 6/7):** Consolidated checklist or key takeaways section.
4. **CTA (Final Slide):** Conversion pill button, follow invite, save-post cue.

## Implementation Details

- **Responsive constraints:** Set a fixed canvas of `width: 1080px; height: 1350px; overflow: hidden; position: relative;` for all slides.
- **Margins:** Place content within a `64px` left/right and `80px` top/bottom safe zone.
- **Interactive Navigation:** Include keyboard event listeners for arrow keys (`ArrowLeft`/`ArrowRight`) to scroll between slides smoothly.
- **Fonts:** Embed `Inter` from Google Fonts.

## Anti-Patterns

- ❌ **No Mixed Slide Themes:** Do not interleave dark content slides and cream content slides. Decks must be visually uniform.
- ❌ **No Overcrowding:** Maximum 40 words of readable text per content slide.
- ❌ **No Placeholders:** Use styled CSS shapes and gradients instead of broken external images.
- ❌ **No Centered Copy:** Always left-align paragraphs, bullet lists, and descriptions (except under-card step subtitles in Variant D).
- ❌ **No Generic Emojis:** Do not place emojis inside paragraphs. Use them only as isolated badges in tag pills.
- ❌ **No Competitor/Platform Branding:** Never output "Claude Design", "Claw Design", "Claude", or "Made with Claude Design" as header handles, footer tags, or signatures. All slides must use the current brand handle (e.g., `@trendingsociety`) as specified in DESIGN.md.
