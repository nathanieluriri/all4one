# Design profile: all4one (working name)

## Product
- One line: a local-first reader that opens ebooks, comics, PDFs and audiobooks in one library, with on-device narration. Books never leave the device; only small progress records sync (Pro).
- Audience: people with DRM-free files (EPUB, comics, PDFs, M4B/MP3) who want one app instead of four.
- Market / locale: global; payments via Google Play / Apple in apps, Paystack or Flutterwave on web. Nigerian English, Yoruba, Igbo and Hausa voices are a possible later differentiator.

## What is built (source of truth)
- Codebase: none yet (design first). Source of truth is `Architecture_plan.docx` (shared 2026-10-13).
- Planned, phase-labelled in designs: read-listen switching (Phase 3), on-device Kokoro narration (Phase 4), skip silence and volume boost (after MVP), cloud voices (Phase 4).
- Proposed, not in the plan: Open Library metadata lookup (owner asked for AI-written metadata; Open Library is free and needs no server AI).

## Sanctioned dataset
- Path: `design/demo-library.md`. Every number on screen comes from it. All values are illustrative sample data for public-domain titles.

## Domain vocabulary
- Item types: ebook, comic, pdf, audio. Status: want, reading, finished.
- Shelves = the plan's "collections" (user-made tabs in the Library). Tags = chips on the item.
- Pair = an ebook and an audiobook linked as one title.
- Position model: CFI for reflowable ebooks, page for PDFs and comics, track + seconds for audio. Every item also has a percent.
- Narration moves by sentence (the pipeline splits text into sentences), so its skip buttons are previous/next sentence.
- Banned: "upload your books", "cloud library", anything implying DRM removal.

## Reference bar
- Mihon/Tachiyomi (owner's screenshots): library grid with count badges and shelf tabs, reader chrome with page slider and four tools, settings list. Take the structure, not the skin.
- Pocket Casts / Apple Books player: one big control row, chapter scrubber, sleep timer and speed as chips.
- Pass rules: Reddit Sans text styles only; every colour bound to a variable; violet only for reading, amber only for listening; badges show the real file extension; no feature shown as live if the plan marks it later.

## Brand
- Variables: collections `Primitives`, `Color` (Dark, Light), `Dimension`.
- Type: Reddit Sans text styles (Display, Headline, Title, Body, Label, Reader, Numeric), Reddit Sans Condensed for badges.
- Colour rules: violet = reading, amber = listening, red only for errors, green only for "finished".
- Logos: none yet. The wordmark is plain Reddit Sans text until a name is chosen.
- Domain visual idea: the reading buddy, a small creature that walks the line being narrated and leaves footprints on the words it touches (from the owner's reference video).

## Figma
- Working file: `VVCsO55kIkLasjBGTEv9Ei` (ALL IN ONE reader (Copy)).
- Pages owned by this work: 01 Foundations, 02 Components, 03 Screens, 04 Mascot Climb.
- No-touch: `Page 1` (owner's reference board and screenshots, nodes 5:12 and 7:2 to 7:9).

## Proof
- No customer proof yet. Sample titles are public domain.
