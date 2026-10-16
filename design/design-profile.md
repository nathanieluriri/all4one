# Design profile: all4one (working name)

## Product
- One line: a local-first reader that opens ebooks, comics, PDFs and audiobooks in one library, with on-device narration. Books never leave the device; only small records sync (Pro): progress, sessions, highlights and notes, tabs and settings.
- Audience: people with DRM-free files (EPUB, comics, PDFs, M4B/MP3) who want one app instead of four.
- Market / locale: global; payments via Google Play / Apple in apps, Paystack or Flutterwave on web. Nigerian English, Yoruba, Igbo and Hausa voices are a possible later differentiator.

## What is built (source of truth)
- Codebase: none yet (design first). Source of truth is `Architecture_plan.docx` (shared 2026-10-13).
- Planned, phase-labelled in designs: read-listen switching and the audiobook Read along mode (Phase 3), on-device Kokoro narration (Phase 4), skip silence and volume boost (after MVP), cloud voices (Phase 4).
- Proposed, not in the plan: Open Library metadata lookup (owner asked for AI-written metadata; Open Library is free and needs no server AI); transcribing an audiobook that has no linked ebook so it can use Read along.
- Owner decisions (15 Oct 2026): Library tabs default to All, Unsorted, Reading, Listening and are sorted by hand; imports land in Unsorted. Stats get an overall page (Kindle week view + Mihon overview + format ranking, no download stats) and a per-book page modelled on the Kindle book card. Audiobooks get a Read along text mode where the reading buddy walks the current line instead of a highlight. Three reading buddies are free, the rest need Pro.

## Sanctioned dataset
- Path: `design/demo-library.md`. Every number on screen comes from it. All values are illustrative sample data for public-domain titles.

## Domain vocabulary
- Item types: ebook, comic, pdf, audio. Status: want, reading, finished.
- Tabs = the plan's "collections" (across the top of the Library). All and Unsorted fill themselves; other tabs are placed by hand. Tags = chips on the item.
- Read along = audiobook text mode (lyrics style); narration = text-to-speech of an ebook.
- Pair = an ebook and an audiobook linked as one title.
- Position model: CFI for reflowable ebooks, page for PDFs and comics, track + seconds for audio. Every item also has a percent.
- Narration moves by sentence (the pipeline splits text into sentences), so its skip buttons are previous/next sentence.
- Banned: "upload your books", "cloud library", anything implying DRM removal.

## Reference bar
- Mihon/Tachiyomi (owner's screenshots): library grid with count badges and shelf tabs, reader chrome with page slider and four tools, settings list. Take the structure, not the skin.
- Pocket Casts / Apple Books player: one big control row, chapter scrubber, sleep timer and speed as chips.
- Kindle reading stats (owner's photos): "Last week" totals, per-day bars with dates and times, Session and Today blocks, and the per-book card (cover, percent, bar, reading time, page, pages left, time left, highlights, notes).
- Mihon statistics (owner's screenshot): overview card with three numbers and icons, grouped count cards. Download counts are excluded on purpose.
- Music-app lyrics view: text scrolls with the audio and the current line stays at a fixed height.
- Pass rules: Reddit Sans text styles only; every colour bound to a variable; amber only for listening; badges show the real file extension; planned features carry a phase label on the canvas or in an annotation, never inside the app UI.

## Brand
- Variables: collections `Primitives`, `Color` (Dark, Light), `Dimension`.
- Type: Reddit Sans text styles (Display, Headline, Title, Body, Label, Reader, Numeric), Reddit Sans Condensed for badges. Reader/Lyrics is the Read along text; Reader/Narration is narration text.
- Colour rules: violet is the app accent and the reading colour; amber is reserved for listening (audio, narration, the reading buddy); red only for errors; green only for "finished". Empty tracks and off toggles use border/track (3:1 on the canvas). The narration sentence band uses listen/band, an opaque token, so text halos can match it. Amber text and icons use listen/text (amber/700 in Light mode, 5.9:1 on white).
- Logos: none yet. The wordmark is plain Reddit Sans text until a name is chosen.
- Domain visual idea: the reading buddy, a small creature that walks the line being read, its feet stopping just short of the letters so every word stays readable (from the owner's reference video). In Read along it replaces the highlight; it leaves no footprints.

## Figma
- Working file: `VVCsO55kIkLasjBGTEv9Ei` (ALL IN ONE reader (Copy)).
- Pages owned by this work: 01 Foundations, 02 Components, 03 Screens, 04 Mascot Climb.
- No-touch: `Page 1` (owner's reference board and screenshots, nodes 5:12 and 7:2 to 7:9).

## Proof
- No customer proof yet. Sample titles are public domain.
