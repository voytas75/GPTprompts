# Concept 1: Hub README + Structured Docs + One-Prompt-Per-File Library

## Goal
Split a very large `README.md` into a navigable documentation set that:
- keeps the root `README.md` fast to scan,
- provides stable deep links to each prompt,
- supports both “browse by topic” and “jump to a specific prompt number” navigation,
- reduces merge conflicts by making edits local to one prompt file.

This concept combines “Hub + Section Docs” with “One prompt per file”.

---

## Design Principles
1. **Root README stays small**: landing page + links only (no giant lists).
2. **Stable permalinks**: prompt links should not change when categories/taxonomy evolve.
3. **Multiple navigation paths**: browse by domain, browse by technique, search by number/title/tag.
4. **Single source of truth**: prompt bodies live only in `prompts/**`. Taxonomy and indexes link to them.
5. **Scales without rework**: adding prompts is “add one file + update index” (or auto-generate index).

---

## Proposed Repository Structure

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
  prompt-taxonomy.md
  resources.md
prompts/
  README.md
  computer-science/
    032-analyze-and-improve-powershell-code.md
    032-analyze-and-improve-powershell-code/
      v1.md
    039-secure-powershell-code-analysis-and-improvement.md
    039-secure-powershell-code-analysis-and-improvement/
      v1.md
  business-and-economics/
    018-personal-financial-advisor.md
    018-personal-financial-advisor/
      v1.md
  arts-and-humanities/
    078-life-event.md
    078-life-event/
      v1.md
  ...
```

### What goes where
- `README.md`: landing page, “start here”, minimal TOC to `docs/` and `prompts/`.
- `docs/techniques/*.md`: technique explanations and reusable meta-prompts (CoT/LoT/etc).
- `prompts/**`: the full library, **one prompt per file**.
- `prompts/README.md`: master index to prompts (by number, title, tags, category).
- `docs/prompt-taxonomy.md`: classification tree / map linking to prompt files (no prompt bodies).
- `docs/resources.md`: useful links.

---

## Prompt File Naming and Paths

### File name convention (stable + sortable)
Use a **3-digit numeric prefix** (or 4-digit if you exceed 999 prompts) plus a slug:
- `032-analyze-and-improve-powershell-code.md`
- `145-executive-summary-synthesis.md`

Rules:
- Always keep the numeric ID in the filename.
- Slug is lowercase, dash-separated, no punctuation.
- ID is the “primary key” for permalinks; slug can be changed if needed (but avoid churn).

### Path designs (choose one)

**Chosen scheme: by domain (from current `README.md` taxonomy)**
- `prompts/computer-science/032-...md`
- `prompts/business-and-economics/018-...md`

Domains are taken from the existing “Prompt’s classification” section and treated as the canonical categorization source. Each prompt has exactly one “home” domain folder; cross-domain relevance is handled via tags and/or extra taxonomy links (without duplicating the prompt body).

---

## Versions and History
Keep the **latest** prompt in the top-level file:
- `prompts/<domain>/032-analyze-and-improve-powershell-code.md`

Move older versions into a sibling folder named after the prompt file (stable + human-readable):
- `prompts/<domain>/032-analyze-and-improve-powershell-code/v1.md`
- `prompts/<domain>/032-analyze-and-improve-powershell-code/v2.md`

Guidelines:
- Latest file stays clean (no “old versions” block).
- Version files contain the full prompt text for that historical revision.
- If you need a change log, keep it minimal and local (e.g., a short “Changes” section at top of each `vN.md`).

---

## Prompt File Content Template (Recommended)
Each prompt file should be easy to read and easy to index.

Suggested structure:
1. **Title**: `# 032. Analyze and improve PowerShell code`
2. **Metadata table** (preferred):
   - category/domain
   - tags
   - intended audience
   - inputs/variables
   - output format expectations
   - source link (if adapted)
3. **Prompt body** in a fenced block for copy/paste:
   - ```text or ```markdown or ```powershell
4. **Notes / variants** (optional):
   - brief usage notes, example invocation, or “related prompts” links

Keeping prompt body in a code fence makes it:
- consistent to copy,
- consistent to render,
- easier to extract programmatically later.

---

## Navigation and Indexes

### 1) Root landing (`README.md`)
Keep only:
- what the repo is,
- how to use it,
- links:
  - “Technique guides” → `docs/techniques/`
  - “Prompt library” → `prompts/README.md`
  - “Prompt taxonomy” → `docs/prompt-taxonomy.md`
  - “Resources” → `docs/resources.md`

### 2) Master index (`prompts/README.md`)
Provide multiple views:
- **By number** (sorted ascending)
- **By domain folder**
- **By tags** (optional)
- **Featured prompts** (optional top 10–20)

Format recommendation: a table with `ID`, `Title`, `Tags`, `Link`.

### 3) Taxonomy map (`docs/prompt-taxonomy.md`)
This file becomes a navigational “map”:
- keep the classification headings,
- under each, link to prompt files:
  - `[032 — Analyze and improve PowerShell code](../prompts/computer-science/032-analyze-and-improve-powershell-code.md)`

Do not duplicate prompt bodies here.

---

## Migration Strategy (From Current Mega-README)
1. **Freeze IDs**: treat existing prompt numbers as canonical identifiers.
2. **Extract technique sections** (`## 2`–`## 7`) into `docs/techniques/*.md`.
3. **Extract taxonomy list** into `docs/prompt-taxonomy.md` and convert links to file paths.
4. **Extract prompts** into `prompts/<domain>/NNN-slug.md` (domain from current taxonomy).
5. **Build `prompts/README.md`** as the new master index.
6. **Shrink `README.md`** to landing + links.

Optional (recommended for UX): keep a short “Where did everything go?” section in `README.md` with the new links.

---

## Link Stability Guidance
To minimize broken links:
- Always include the numeric ID in the prompt filename and the H1.
- Use file-based links throughout (`prompts/.../NNN-...md`), not anchors into a mega document.
- If you need anchors inside a prompt file (sections like “Old versions”), they are local and won’t affect other prompts.

---

## Maintenance Workflow (How it stays clean)
Adding a new prompt should be:
1. Create `prompts/<category>/NNN-slug.md`
2. Add one row/link to `prompts/README.md`
3. Add one link in `docs/prompt-taxonomy.md`

Updating a prompt should be:
1. If preserving history, move current latest to `prompts/<category>/NNN-slug/vN.md`
2. Update `prompts/<category>/NNN-slug.md` with the new latest
3. Ensure index + taxonomy links still point to the latest file

If desired, automate index maintenance later by parsing the metadata tables in prompt files.
