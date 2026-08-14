# Monthly Zine Postcard Layout Specification

## Canvas and upper photo

- Create a portrait `3:4` card on warm ivory paper.
- Use `contain` for the upper source photo. Never crop, cover, stretch, repaint, replace, or remove any part of it.
- Preserve camera frames, EXIF, brand lettering, decorative frames, and existing photo-card designs as part of the complete source artifact unless the user explicitly requests the inner photo only.

Route the photo by `r = source width / source height`:

- `r >= 1.70`: centered horizontal strip, 29–32% card height, max 90% card width.
- `1.15 <= r < 1.70`: centered horizontal photo area, 31–34% card height, max 88–92% card width.
- `0.85 <= r < 1.15`: centered square photo card, 35–38% card height, fitted completely by height.
- `0.55 <= r < 0.85`: centered vertical ticket, 40–42% card height, fitted completely by height; margins must read as intentional editorial space.
- `r < 0.55`: stop automatic generation and ask whether to retain the whole image or only its photographic area.

## Lower monthly page

Make the lower section a miniature horizontal monthly photography page. It is never a large vertical illustration or a second photo.

- Wide and standard landscape source: lower page 66–69% of card height.
- Square source: 62–65%.
- Portrait source: 58–60%.
- For shorter lower pages, reduce vertical gaps by at most 15%. Never change the left/right width ratio, type hierarchy, or footer relationship.
- Put one watercolor-and-ink visual block in the lower page's upper-left, 66–70% of lower-page width and 50–54% of lower-page height.
- The visual block uses free, organic watercolor edges and extracts one complete source-specific relationship: subject + space + light. It must stay clear of the footer.
- Below the watercolor block, at lower-page height 58–62%, place the handwritten line. It remains left-aligned and does not enter the right column.

## Right bookmark column

Reserve the lower page's right 24–28% as uninterrupted warm paper: no border, divider, illustration, or photo.

Align all groups to one central vertical axis:

- 0–18%: month number then English month beneath it.
- 32–62%: literary vertical pair. Book or emotional title on the right; source-verified short quotation or original caption on the left. Use `0.35–0.5em` between them.
- 82–90%: tiny headphone icon, centered **above** the artist/song line.

The literature block and music block need the column's largest intentional blank interval. The pure blank band before the footer rule is only 8–12% of lower-page height.

## Typography and color

- Sample one muted dark, readable text color from the source photo. Use it for month, copy, icon, rule, and footer.
- Let handwritten line and short quotation equal `1.0`.
- Book/title equals `1.5` (allowed `1.45–1.55`) and uses an elegant medium-weight serif, never bold.
- Song equals `0.7–0.75`; footer equals `0.8–0.9`; English month equals `1.5`.
- Month number is the only largest display text, `4.0–4.5` times the short quotation.
- No right-column text except the month number may exceed the book/title.
- Use a light handwritten face for the line, restrained serif for English and footer, and clear Chinese vertical text when Chinese is used.

## Footer

At lower-page height 86–88%, draw a thin horizontal rule. Under it, set three independent aligned fields:

- left: `{author}`
- center: `{date}`
- right: `{closing_line}`

Keep the footer untouched by watercolor or any other visual element.

## Locked generation skeleton

```text
Create a portrait 3:4 monthly Zine postcard on warm ivory paper with a strict upper-photo / lower-monthly-page structure. Keep the complete supplied photo unchanged in the upper area using contain only. Do not crop, stretch, repaint, replace, or remove any source detail.

Below it, create one miniature horizontal monthly photography page, not a second poster. In the lower left, create one source-specific watercolor-and-ink visual block with free organic edges, showing only the scene, subject, light, and spatial relationship from the source. Never reproduce EXIF, frames, branding, UI, or other packaging in the watercolor.

Reserve an unbordered warm-paper bookmark column on the right. Place the exact month, selected literature pair, and headphone-above-song group on its vertical axis. Use the exact supplied strings. Type hierarchy: month number 4.0–4.5x quote; English month 1.5x; book title 1.5x; quote and handwritten line 1.0x; song 0.7–0.75x; footer 0.8–0.9x. Keep the footer compact under one thin line, separate from the watercolor.

Do not add date grids, swatches, collage panels, logos, badges, stickers, decorative waves, watermarks, or extra text.
```
