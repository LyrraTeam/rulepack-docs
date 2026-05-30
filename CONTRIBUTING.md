# Contributing to rulepack docs

Thanks for helping improve the rulepack documentation! This repo is the
source-of-truth for **https://rulepack.lyrra.net/docs** — anyone can propose
changes to the wording, structure, and the `rulepack.json` standard in the
open. (The rulepack app and registry live in a separate repo; this one is the
public docs + community home.)

By participating you agree to our
[Code of Conduct](https://rulepack.lyrra.net/docs/legal/code-of-conduct).

## Ways to contribute

- **Spotted a mistake or something unclear?** Open an issue using the
  **Documentation fix** template.
- **Have an idea** (new page, restructure, a missing agent)? Open an issue using
  the **Suggestion** template so we can discuss it in the open first.
- **Ready to write?** Open a pull request (see below).

## Editing the docs

1. Docs are one folder per language (`en/`, `ja/`) — see the
   [README](./README.md) for the layout. Edit the matching file in each
   language; keep the page list in `meta.json` mirrored across languages.
2. Keep **one topic per file** and match the existing frontmatter
   (`title` + `description`). A `<Callout>` component is available in MDX.
3. Be precise about behaviour. If something isn't shipped yet, say so — the docs
   double as the de-facto spec for `rulepack.json`.
4. Preview locally if you can (the app clones this repo into
   `apps/rulepack-web/content/docs`), or describe your change clearly so a
   maintainer can verify it.

### Translations

`en/` is the reference language. If you can only update one language, do it and
note in the PR which others still need the change — a maintainer or another
contributor can follow up. Untranslated pages fall back to English.

### The `legal/` pages

`legal/` holds official policies (Terms, Privacy, Acceptable Use, Code of
Conduct). Typo and clarity fixes are welcome via PR, but **substantive changes
to policy meaning are made by the maintainers** — open an issue to discuss
rather than rewriting them.

## Pull requests

- Keep PRs focused; one topic per PR is easiest to review.
- Reference any related issue.
- By submitting a contribution, you certify you have the right to submit it and
  you license it to the project under the same terms as the surrounding docs,
  so it can be published on the site.

## Questions

Open an issue, or email **contact@rulepack.lyrra.net**.
