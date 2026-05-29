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

Each `*.mdx` file at the repository root is one docs page, mounted at
`/docs/<filename>`:

| File | Page |
| --- | --- |
| `index.mdx` | `/docs` |
| `quickstart.mdx` | `/docs/quickstart` |
| `rulepack-json.mdx` | `/docs/rulepack-json` |
| `cli.mdx` | `/docs/cli` |
| `publishing.mdx` | `/docs/publishing` |

Pages use [fumadocs](https://fumadocs.dev) frontmatter:

```mdx
---
title: Page title
description: One-line summary, shown in nav + metadata.
---
```

A `<Callout>` component is available in MDX (no import needed).

## Contributing

1. Edit or add an `.mdx` file at the repo root. Keep one topic per file and
   match the existing frontmatter.
2. Open a pull request. Substantive wording / structure discussion belongs in
   issues so it stays public.
3. Be precise about behaviour — if something isn't shipped yet, say so. The
   docs double as the de-facto spec for `rulepack.json`.

## How the site consumes this repo

The rulepack web app pins this repository as a **git submodule** at
`apps/rulepack-web/content/docs`, and its production Docker build also falls
back to cloning this repo's default branch when the submodule isn't present —
so the published site always has the latest docs without any extra wiring.
