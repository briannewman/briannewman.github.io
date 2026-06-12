# CLAUDE.md

This repo's agent guidance lives in @AGENTS.md — site shape, the page-index
convention, editing style, and the publishing process for rendered artifacts.
It is the single source of truth for both Claude Code and Codex.

## Claude Code notes

- `index.html` at `/` is a plain link directory. Never replace it with a report
  or a redirect. Add a link card; put the page itself at a named URL.
- Keep every page static and self-contained — inline all CSS/JS, no external
  `<link rel="stylesheet">` or `<script src>`, no build tooling.
- Verify a page opens from `file://` before committing.
- Do not publish credentials, gated corpus excerpts, raw claim packets, article
  IDs, or local-only artifact details.
