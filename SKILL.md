---
name: photo-to-monthly-zine-postcard
description: Turn one user-provided photograph into a portrait 3:4 monthly Zine postcard with an unchanged upper photo, a compact watercolor monthly page below, and image-grounded literature and music curation. Use when users ask for a photo postcard, 月历明信片, Zine 明信片, or a literary music-matched photo card.
---

# Photo to Monthly Zine Postcard

Create one finished front-side postcard. Treat the supplied photo and the monthly layout as equally important: preserve the photo faithfully, then create a compact editorial lower page that responds to the source.

## Required inputs

- Use the user's photo as the only photo source.
- Use the user's provided month, handwritten line, footer fields, or copy verbatim when supplied.
- If the user supplies no month, infer the current month only when that is clearly intended; otherwise ask one concise question.
- Read [layout specification](references/layout-spec.md) before composing any image.

## Workflow

1. Inspect the photo for subject, focal relationship, dominant color, light, mood, and aspect ratio `r = width / height`.
2. Route the unchanged source photo into the upper area using the ratio rules in [layout specification](references/layout-spec.md). Preserve the entire supplied photo with `contain`; do not crop, stretch, repaint, remove, or retype its built-in frame, EXIF, branding, or camera text.
3. Curate the right-column book, short text, and song using [content curation](references/content-curation.md). Research and verify them before image generation; never tell the image generator to browse or invent sources.
4. Build the lower half as one miniature **horizontal monthly photography page**, not a second poster or a full-page illustration. Follow every placement and type-scale requirement in [layout specification](references/layout-spec.md).
5. Generate the final 3:4 card using the locked prompt skeleton in the layout specification. Pass preselected, verified text as exact strings.
6. Check the result with [quality gate](references/quality-gate.md). Regenerate when a hard constraint fails.

## Visual anchors

- Use `assets/reference-beach-monthly.png` only as a private layout reference when a visual anchor helps. Do not include it in the user's output.
- Preserve the reference's hierarchy: photograph above; free-edge watercolor on the lower left; one unbordered, warm-paper right column; a compact footer at the bottom.

## Non-negotiable constraints

- Keep the outer card portrait `3:4`, warm ivory paper, subtle paper grain, and restrained single-color typography.
- Keep the upper photo as the actual complete source image. Do not turn it into watercolor.
- Never use the lower section as a full vertical poster, second large photo, date grid, swatch strip, collage, badge, logo, watermark, sticker, or generic decoration.
- Keep the lower watercolor source-specific, free-edged, and limited to the left visual block. It must not duplicate photo-card packaging such as EXIF, a device frame, or a UI.
- Keep the right column empty except for month, literature block, and music block. Do not add a divider line around it.
- Treat supplied copy as locked. Do not paraphrase, translate, alter punctuation, or silently replace dates.

## Default copy

Use these only when the user has not supplied replacements:

- Handwritten line: `Keep loving, run to mountains and seas.`
- Footer left: `MIXIAN`
- Footer center: `2026.08.10`
- Footer right: `Free to sway and thrive.`

## Output

Deliver the generated postcard image and briefly state the selected month, literature source/caption, and song. If the fallback was used, say so plainly.
