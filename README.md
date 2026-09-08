# sn-slides-public-artifacts

Public image hosting for the `sn-create-slides` skill's Google Slides backend.

The Google Slides API's `createImage` request only accepts a `url` — it fetches
the image anonymously, server-side, with no way to authenticate as a Drive
user. That means any image inserted into a Slides deck via the API (logos,
backgrounds, icons) needs a genuinely public URL. This repo exists to be that:
plain static image files, referenced by their `raw.githubusercontent.com`
URL, nothing else.

## Layout

- `sambanova/` — the `sn-create-slides` skill's default SambaNova brand assets
  (logos, background photos, brand-neutral outline icons).
- `sambaacademy/` — a custom-brand image set used by one team's decks.

Each additional custom brand a team wants to use with the Google Slides
backend gets its own top-level folder here, mirroring this pattern.

## Nothing sensitive belongs here

Every file in this repo is served with no authentication to anyone on the
internet who has the URL. Only commit images that are already meant to be
public-facing (brand logos, marketing photography) — never anything
confidential.
