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
