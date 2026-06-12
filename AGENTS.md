# Repository Guidelines

## Site Shape

- Keep `index.html` as a plain directory of links to public pages.
- Do not put a full report, redirect, or single-purpose landing page at `/`.
- Add each report as a separate top-level `.html` file unless a subdirectory is
  clearly warranted.
- When adding a new public page, add a link card to `index.html` with a short
  title and one-sentence description.
- Keep pages static and self-contained. Avoid build tooling unless the site
  grows past simple standalone HTML pages.
- If a previous homepage report is moved behind the index, preserve the report
  content at its explicit report URL instead of replacing it with a redirect to
  `/`.

## Editing Style

- Use restrained, report-oriented styling: readable type, simple cards or
  tables, and no marketing hero treatment.
- Keep page copy concise and factual.
- Do not publish private source text, gated corpus excerpts, credentials, or
  local-only artifact details.
- Verify top-level pages open directly from `file://` before committing.

## Publishing Rendered Artifacts

When a set of related pages is published together (e.g. a spec plus its
implementation plans), put them in a named subdirectory and add a single
link-card to `index.html` pointing at the directory (`href="<dir>/"`, which
GitHub Pages serves from `<dir>/index.html`).

- Each page must be fully self-contained: inline all CSS/JS, no external
  `<link rel="stylesheet">` or `<script src>`. Source pages authored elsewhere
  with a shared stylesheet must have that stylesheet inlined before publishing.
- Within the subdirectory, cross-link pages by relative filename so the set is
  portable.
- Publish the rendered HTML only. Do not copy the source Markdown (or other
  source files) into the repo; rewrite any in-page link to source as plain text
  naming the path in the source repo, so no dangling links ship.
- The subdirectory's own `index.html` is a sub-index of that set; this does not
  violate the "no report at `/`" rule, which applies only to the site root.

### Process used for `superpowers/`

1. Rendered the Markdown specs/plans from the source repo into self-contained
   HTML (one landing `index.html`, one spec page, one page per plan), inlining
   the shared CSS/JS into every file.
2. Copied only the HTML set into `superpowers/` — no source Markdown. Rewrote the
   one in-page "source markdown" link as plain text naming the source-repo path.
3. Added one link-card to the root `index.html`.
4. Verified no external asset references and no dangling `.md` links remain and
   every page opens from `file://`, then committed and pushed to `main`
   (GitHub Pages auto-deploys).
