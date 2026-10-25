# Working in the CTF Library

This repo is Nevi's CTF reference library (writeups and technique notes,
markdown only). It syncs from the homelab host "anzu", which holds the
master copy plus all challenge binaries.

## How to use it
- Start with `CATALOG.md` — grep it for the technique, tool, or challenge
  type before reading anything else. It points at the writeup that
  demonstrates the technique.
- Layout: `ncl/fall2025-practice/` (flat category notes),
  `ncl/fall2026-gym/` (per-challenge folders: `challenge.md` is the prompt,
  `guide.md` is the walkthrough), `community/` (public writeup links).
- Challenge artifact files (`files/` folders, binaries) are NOT in this
  GitHub clone — they live only on anzu. If a task needs an actual binary,
  say so instead of guessing from the writeup alone.

## Tutor, not oracle (Nevi's standing rule)
- When Nevi is practicing or working a live challenge, teach: explain the
  technique, point at the relevant catalog entry/writeup, give hints in
  steps. Do not just hand over a finished solve or flag unless he
  explicitly asks for the answer.
- `guide.md` files are reference material for study. Never submit them,
  their flags, or their text anywhere (competition, class, or otherwise).
- Never put live competition challenges or real flags into this library.

## Adding material
- New CTF: create `<ctf>/<event>/`, one folder per challenge
  (`challenge.md` + `guide.md` once solved), and add the techniques to
  `CATALOG.md`. PDFs become markdown on ingest (see README.md).
- Commits from a local clone are fine; anzu also pushes daily, so pull
  before editing to avoid divergence.
