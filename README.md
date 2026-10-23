# CTF Library

Reference writeup data for CTF prep. This is the knowledge base — the
grinder's `queue/` is where unsolved challenges go, `done/` is where
solved ones land. This folder is what gets consulted *before* solving.

## Layout

```
library/
  README.md            this file
  CATALOG.md           technique/tool index — search this first
  <ctf>/
    <season-or-event>/
      <category>/
        <challenge>/
          challenge.md   description + questions (no solutions)
          guide.md       official walkthrough / writeup
          files/         challenge artifacts
      <category>.md      flat notes file (community writeups like Fall 2025)
  community/
    README.md          links to public writeups worth reading
```

## Adding a new CTF

1. Create `<ctf>/<event>/`.
2. One folder per challenge: `challenge.md` (prompt), `guide.md`
   (writeup once it exists), `files/` for artifacts.
3. Or drop a flat `<category>.md` for note-style sources.
4. Add entries to `CATALOG.md` under the right technique headings.

## Rules

- Writeup data only. Never put live competition challenges or flags here.
- `guide.md` files are reference material, not to be submitted anywhere.
- Keep the CATALOG current: every new ingestion adds its techniques.
- **PDFs become Markdown on ingest.** Extract text (pdftotext), transcribe any
  content-bearing screenshots into the relevant category file, then delete the
  PDF. The library stays text-only: greppable, tiny, AI-friendly.
