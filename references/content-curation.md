# Image-Grounded Literature and Music Curation

## Separate research from image generation

Do research before creating the image. The agent selects and verifies all copy, then passes only the final exact strings to image generation. An image model must not be instructed to browse, search, or fabricate a source.

## Research workflow

1. Describe the photo internally in five dimensions: visible subject, light/time, spatial feeling, emotional tone, and dominant color.
2. Search reliable sources for a real book, short quotation, and song that fit at least two dimensions. Prefer official author/publisher/lyrics/cultural institution pages, or a reputable music catalogue.
3. Verify the work title, attribution, quotation wording, artist, and song title.
4. Keep the literary quotation or original caption short enough for the narrow column: normally no more than 20 Chinese characters or a short English sentence.
5. Use a short original photo caption only when a suitable, verifiable quotation cannot be found. Label it internally as original rather than attributing it to a book.
6. If no suitably verified song is found, leave the music text blank. Never invent a song, an artist, a book, a quotation, or an attribution.

## Matching standard

Match the book/title, line, and song to at least two of these dimensions:

- subject or setting
- light, weather, or time
- motion or stillness
- emotional direction
- color and temperature
- scale, solitude, intimacy, or openness

Avoid literal keyword matching that misses the image's actual feeling.

## Text payload sent to layout

Pass only this resolved content to the generator:

```text
month_number: 08
english_month: August
book_title: 《…》
quote_or_original_caption: …
artist: …
song_title: …
handwritten_line: Keep loving, run to mountains and seas.
author: MIXIAN
date: 2026.08.10
closing_line: Free to sway and thrive.
```

When music is blank, keep the headphone/music area visually quiet rather than filling it with unrelated decoration.
