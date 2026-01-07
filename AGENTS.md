# Repository Guidelines

## Project Structure & Content Organization
- `README.md`: main entry point and **only index** (technique notes + prompt classification with links).
- `prompt/`: one prompt per file, **latest only**, named `NNN-slug.md` (e.g. `prompt/032-analyze-and-improve-powershell-code.md`).
- `docs/archive/README.md`: snapshot of the pre-migration mega-README (do not edit except for archival notes).
- `data/`: supporting text files used as source/reference material.
- `images/`: images referenced by `README.md`.

## Development Commands
This repo is Markdown-first (no build system).
- Search content: `rg "vector database" README.md prompt/`
- Find a prompt by ID: `ls prompt/032-*.md`
- Quick link sanity (prompt files exist): `python - <<'PY'\nimport re\nfrom pathlib import Path\ntext=Path('README.md').read_text('utf-8')\nmissing=[]\nfor rel in re.findall(r'\\(prompt/([^)]+\\.md)\\)', text):\n  if not (Path('prompt')/rel).exists(): missing.append(rel)\nprint('missing', len(missing)); print(*missing[:20], sep='\\n')\nPY`

## Writing Style & Naming Conventions
- Prompt filenames: `NNN-<kebab-case-title>.md` where `NNN` is zero-padded (immutable ID).
- Prompt file format: start with `# NNN. Title`, then include the prompt body in fenced code blocks (```text/```markdown/```powershell as appropriate).
- Keep Markdown clean: wrap long lines in prose when readability suffers; preserve code block formatting exactly.

## Testing Guidelines
No automated tests. Validate changes by:
- ensuring `README.md` links resolve to files in `prompt/`,
- opening `README.md` on GitHub and checking rendering of lists, code blocks, and `<details>` sections.

## Commit & Pull Request Guidelines
- Commits in history often use short, descriptive messages (sometimes with emojis). Follow that style and mention the prompt ID when relevant (e.g. “Add prompt 155 …”).
- PRs should include: what changed, which prompt IDs/files were touched, and any link/rendering checks performed. If you modify `README.md`, verify the classification links still point to the right `prompt/NNN-*.md` files.

