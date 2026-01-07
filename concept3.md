# Concept 3: Multi-Domain Navigation Without Duplicating Prompt Files (Virtual Views)

## Goal
Allow a prompt to appear in **multiple domains/categories** (as in the current “Prompt’s classification”) while keeping **exactly one copy** of the prompt content on disk.

This avoids duplication, prevents drift, and still supports “browse by domain” navigation.

---

## GitHub-Specific Considerations (Impacts on Decisions)
This repository is hosted on GitHub, so the design optimizes for GitHub’s native browsing and Markdown rendering:
- **Prefer file-based links** over heading anchors in huge pages; GitHub renders per-file Markdown well and file links stay stable as content grows.
- **Avoid symlinks as a core mechanism**; symlink handling varies by OS/ZIP downloads and can confuse contributors. Keep everything as real files + relative links.
- **Add “index” READMEs in folders** to make GitHub folder navigation pleasant (GitHub surfaces `README.md` when you open a directory).
- **Keep paths slug-safe** (lowercase, hyphens) to minimize URL/encoding quirks and keep links readable.
- **Optional automation fits GitHub well**: if indexes/taxonomy become painful to maintain manually, a small GitHub Action can regenerate `prompts/README.md` and `docs/taxonomy/*.md` from canonical prompt metadata on PRs.

---

## Core Idea
- Store each prompt **once** in a canonical location.
- Create **domain index pages** (and taxonomy maps) that link to the canonical prompt file.
- Optionally create lightweight **alias files** that contain only a pointer, not the full body.

---

## Proposed Repository Structure

```
README.md
docs/
  techniques/
  taxonomy/
    README.md
    arts-and-humanities.md
    business-and-economics.md
    computer-science.md
    ...
  resources.md
prompts/
  README.md
  by-id/
    README.md
  by-id/
    032-analyze-and-improve-powershell-code.md
    078-life-event.md
    ...
  by-id/
    032-analyze-and-improve-powershell-code/
      v1.md
      v2.md
```

### What goes where
- `prompts/by-id/NNN-slug.md`: **single source of truth** for the latest prompt.
- `prompts/by-id/NNN-slug/vN.md`: historical versions.
- `docs/taxonomy/*.md`: domain pages that list prompts for that domain (links only).
- `prompts/README.md`: master index (by number/title/tags).
- `README.md`: hub landing page.

---

## Multi-Domain Classification (No Duplication)
A prompt can be referenced from multiple places by linking to the canonical file.

Example:
- `docs/taxonomy/computer-science.md` includes:
  - `[032 — Analyze and improve PowerShell code](../../prompts/by-id/032-analyze-and-improve-powershell-code.md)`
- `docs/taxonomy/cybersecurity.md` can include the *same* link to the same canonical file.

This produces “virtual duplication” in navigation (it appears in multiple domain lists) without duplicating content.

---

## Optional: Alias Files (If You Want Domain Folder Browsing)
If you strongly want `prompts/<domain>/` folders for browsing, keep them as **aliases**, not duplicates:

```
prompts/
  computer-science/
    032-analyze-and-improve-powershell-code.md   (alias stub)
```

Alias stub contains:
- a short note “This is an alias”
- a link to canonical `prompts/by-id/NNN-slug.md`

Pros:
- domain folder browsing works,
- still no duplicated bodies,
- minimal maintenance.

Cons:
- users click through one extra hop (unless you rely on taxonomy pages instead).

On GitHub, taxonomy pages (`docs/taxonomy/<domain>.md`) plus folder READMEs usually remove the need for alias stubs. Prefer alias stubs only if you observe users primarily navigating by clicking folders rather than indexes.

---

## Prompt File Format (Canonical)
Each `prompts/by-id/NNN-slug.md` contains:
1. `# NNN. Title`
2. Markdown metadata table (includes **all domains** it belongs to)
3. Prompt body in a fenced block

Version files live under `prompts/by-id/NNN-slug/vN.md` and follow the same format.

---

## Navigation Pages

### `prompts/README.md` (library index)
Provide:
- by number
- by title
- by tags
- by domain (links to `docs/taxonomy/<domain>.md`)

### `docs/taxonomy/<domain>.md` (domain pages)
Each domain page lists prompts that belong to that domain (links only), sourced from the current taxonomy.

---

## Maintenance Workflow

### Adding a prompt
1. Add `prompts/by-id/NNN-slug.md`
2. Add its domains in the metadata table
3. Add links to it in relevant `docs/taxonomy/*.md` pages (or generate these later)
4. Add one row to `prompts/README.md` (or generate later)

### Updating a prompt (preserve history)
1. Move current latest to `prompts/by-id/NNN-slug/vN.md`
2. Update `prompts/by-id/NNN-slug.md`
3. No domain link changes needed unless domains changed

---

## When to Choose This Concept
Pick Concept 3 if:
- prompts belong to multiple domains and you want them listed everywhere,
- you want **zero content duplication**,
- you prefer navigation through index pages (taxonomy) over folder browsing,
- you want the simplest long-term maintenance model (one file to edit per prompt).

---

## Backup Before Migration (GitHub-Friendly)
Before changing the root `README.md`, preserve the current state in-repo so it remains accessible on GitHub:
- Copy current `README.md` to `docs/archive/README.md` (treat this as an immutable snapshot).
- Optionally add a short header at the top of `docs/archive/README.md` stating it is an archive snapshot and should not be edited.
