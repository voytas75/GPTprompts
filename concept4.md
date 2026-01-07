# Concept 4: Flat Prompt Library + Classification In Root README (No Domain Folders)

## Goal
Restructure the repo for GitHub so:
- every prompt is a single file located at `prompt/<number>-<prompt-name>.md`,
- classification/taxonomy stays in the root `README.md` (as link lists, not folders),
- navigation is primarily via `README.md` + indexes + search.

This avoids folder-based category structures entirely.

---

## Proposed Structure

```
README.md
docs/
  techniques/
    cot.md
    lot.md
    few-shot.md
    self-consistency.md
    meta.md
    rag.md
  resources.md
  archive/
    README.md
prompt/
  README.md
  032-analyze-and-improve-powershell-code.md
  078-life-event.md
  ...
prompt-versions/
  032-analyze-and-improve-powershell-code-v1.md
  032-analyze-and-improve-powershell-code-v2.md
  ...
```

### What goes where
- `README.md`: hub landing page + **classification tree** (from current “Prompt’s classification”) linking to `prompt/*.md`.
- `prompt/*.md`: **latest** version of each prompt (one prompt per file).
- `prompt/README.md`: master prompt index (by number, title, tags; optional featured list).
- `prompt-versions/*`: historical versions (optional, but recommended for preserving provenance).
- `docs/archive/README.md`: snapshot of the original mega-README before migration.

---

## File Naming Rules (Stable Permalinks)
- Use a numeric ID prefix as the canonical identifier:
  - `prompt/032-analyze-and-improve-powershell-code.md`
- ID is **immutable** (never renumber).
- Slug is lowercase with hyphens; keep it stable when possible.
- All links are file-based (`prompt/...md`), not anchors into a large page.

If a slug must change, prefer keeping the old file as a stub that links to the new file (to preserve old GitHub links), and treat that stub as an “alias”.

---

## Prompt File Format (Recommended)
Each file in `prompt/*.md` uses:
1. H1 title: `# 032. Analyze and improve PowerShell code`
2. Markdown metadata table (machine-friendly by convention)
3. Prompt body in a fenced block for copy/paste

Recommended metadata keys (fixed order):
- `Domains` (can be multiple; reflects classification membership)
- `Tags`
- `Audience`
- `Inputs`
- `Output`
- `Source`

---

## Classification Design (Single File)
The root `README.md` becomes the canonical “Prompt’s classification” map:
- replicate the current hierarchy (including nested subcategories) as headings/lists,
- each prompt entry is a link to its file in `prompt/`.

Example link format:
- `[032 — Analyze and improve PowerShell code](../prompt/032-analyze-and-improve-powershell-code.md)`

This supports prompts belonging to multiple categories without duplication: the same prompt file can be linked from multiple places in the classification tree.

---

## Indexes (GitHub Navigation)

### `prompt/README.md`
Primary “library index”, optimized for scanning:
- table sorted by ID
- optional sections for “Featured”, “Recently updated”, “By tag” (manual or generated later)

### Root `README.md`
Stays relatively short at the top (hub links), and then includes classification. It points users to:
- prompt library index (`prompt/README.md`)
- technique guides (`docs/techniques/`)
- resources (`docs/resources.md`)
- archived original README (`docs/archive/README.md`)

---

## Versions / History (Optional but Clean)
To keep `prompt/*.md` as “latest only” while preserving older revisions:
- store older revisions in `prompt-versions/` with a clear suffix:
  - `prompt-versions/032-analyze-and-improve-powershell-code-v1.md`

Rules:
- never edit version files after creation,
- latest lives only in `prompt/`.

---

## Migration Steps (From Current Mega-README)
1. Back up current `README.md` to `docs/archive/README.md`.
2. Create `docs/techniques/*.md` for sections like CoT/LoT/Few-shot/etc.
3. Extract each prompt into `prompt/NNN-slug.md` (latest).
4. If preserving history, copy original text into `prompt-versions/*-v1.md` and treat extracted file as curated “latest”.
5. Replace the root `README.md` with:
   - a short hub section (links to `prompt/README.md`, `docs/techniques/`, etc.)
   - the “Prompt’s classification” section converted into file-based links to `prompt/*.md`
6. Create `prompt/README.md` index.

---

## When to Choose This Concept
Pick Concept 4 if you want:
- the simplest “where do prompts live?” answer (`prompt/` flat),
- categories that can change over time without moving files,
- multi-category prompts with no duplication,
- GitHub-friendly navigation via indexes rather than folders.
