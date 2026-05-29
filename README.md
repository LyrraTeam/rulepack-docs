# rulepack-docs

The documentation source-of-truth for **[rulepack](https://rulepack.lyrra.net)** —
the npm-style registry and CLI for AI coding-agent rule files (Claude Code,
Cursor, Cline, Windsurf, AGENTS.md).

These MDX files are rendered at **https://rulepack.lyrra.net/docs** by the
rulepack web app, which consumes this repository directly. Improving the public
documentation happens **here**, via pull requests and issues — so anyone can
propose changes and discuss wording, structure, and the `rulepack.json` standard
in the open.

## Layout

Docs are organized into one folder per language (fumadocs `parser: "dir"`), so
adding a new language is just adding a folder:

```text
en/                     # English (default language)
  index.mdx             # → /docs
  quickstart.mdx        # → /docs/quickstart
  rulepack-json.mdx     # → /docs/rulepack-json
  cli.mdx               # → /docs/cli
  publishing.mdx        # → /docs/publishing
ja/                     # 日本語 — same filenames as en/
  index.mdx
  …
```

The site shows the folder matching the visitor's language; anything missing in a
language falls back to `en/`. To add a language, create a new folder (e.g.
`fr/`) with the same filenames and translate — then wire the locale into the web
app's `lib/i18n.ts`.

Pages use [fumadocs](https://fumadocs.dev) frontmatter:

```mdx
---
title: Page title
description: One-line summary, shown in nav + metadata.
---
```

A `<Callout>` component is available in MDX (no import needed).

## Contributing

1. Edit the matching file under the language folder (`en/…`, `ja/…`). Keep one
   topic per file and match the existing frontmatter. Translations should mirror
   the English filenames so they line up.
2. Open a pull request. Substantive wording / structure discussion belongs in
   issues so it stays public.
3. Be precise about behaviour — if something isn't shipped yet, say so. The
   docs double as the de-facto spec for `rulepack.json`.

## How the site consumes this repo

The rulepack web app clones this repository into `apps/rulepack-web/content/docs`
at dev/build time (its production Docker build clones it directly), so the
published site always has the latest docs without any extra wiring.
