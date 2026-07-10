# DONE: Fix Broken TOC Anchor Links

**Section:** `intro/`, `fundamentalAI/`, `medicalImaging/`, `contouring/`, `treatmentPlanning/`
**Priority:** High
**Owner:** Codex
**Opened:** 2026-07-10
**Completed:** 2026-07-10

## Original Gap

Five chapters opened with hand-written GitHub-style Markdown tables of contents. MyST/Sphinx did not resolve those generated slugs. The original build reported 145 warnings: 144 from the manual TOC links and one additional stale Introduction link to a nonexistent glossary page.

| File | Original warnings |
|---|---:|
| `fundamentalAI/index.md` | 55 |
| `medicalImaging/medicalImaging.md` | 25 |
| `intro/intro.md` | 24 |
| `contouring/contouring.md` | 23 |
| `treatmentPlanning/treatmentPlanning.md` | 18 |

## What Was Done

1. Removed the hand-written TOC bullet-link blocks from all five affected chapters.
2. Retained the chapters' actual headings and body content, allowing `sphinx_book_theme` to provide navigation from the document structure.
3. Did not add replacement manual links or a redundant in-page TOC.
4. Confirmed `GUIDE.md` already prohibits hand-written chapter TOCs and updated its reference to point to this completed record.
5. Corrected the remaining stale glossary link to point to the existing glossary in `fundamentalAI/index.md`.
6. Ran a clean strict Sphinx build and confirmed all 145 baseline warnings were eliminated.

## Acceptance Criteria

- [x] Zero `myst.xref_missing` warnings reference hand-written anchor links in a clean Sphinx build
- [x] No chapter contains a hand-written `- [Text](#slug)` navigation block
- [x] The local documentation build completes with a visibly lower warning count
- [x] The same Sphinx command used by the GitHub Actions docs workflow completes locally with zero warnings; the remote run will execute after push

## Verification

- `rg` found no hand-written `- [Text](#slug)` navigation entries in `docs/`.
- `git diff --check` passed.
- Clean strict Sphinx build: completed with zero warnings.
