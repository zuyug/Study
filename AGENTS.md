# Study Notes Agent Rules

This repository is the user's personal study note site.

## Primary Goal

When the user says `노트추가`, `정리노트 추가`, `HTML에 추가`, or asks to save the latest answer, convert the most recent assistant explanation into a beginner-friendly Markdown note and publish it through this MkDocs site.

## Categories

Use one primary category:

- `economy`: economics, stocks, finance, accounting, investing, macro, trading
- `coding`: programming, errors, automation, GitHub, HTML/CSS/JS/Python
- `ai`: Codex, Claude, prompts, AI tools, AI workflows
- `life`: practical life knowledge, work habits, decisions, other topics

Use tags for detailed classification. Keep categories broad and tags specific.

## Note Format

Create notes with this shape:

1. YAML frontmatter with `title` and `tags`
2. H1 title
3. `.note-meta` block with category, beginner level, and core question
4. One-line summary admonition
5. Beginner-friendly explanation
6. Easy example
7. Common pitfalls or cautions
8. "다시 기억할 문장"
9. Review cards table

Use `docs/templates/note-template.md` as the source pattern.

## Required Updates

For every new note:

- Add the Markdown file under the matching `docs/<category>/` folder.
- Add a link to the category `index.md`.
- Add the page to `mkdocs.yml` navigation when it should be visible in the left nav.
- Add at least one card to `docs/review/anki-cards.md`.
- Add the same card rows to `docs/review/anki-cards.csv`.
- Run `mkdocs build --strict`.
- If the user requested publishing, commit and push to GitHub.

## Validation

Use RITL for requested build work:

1. Build with `mkdocs build --strict`.
2. If it fails, fix the smallest relevant issue.
3. Rebuild until it passes or a real blocker is found.
4. Verify important pages exist in `site/`.

Do not replace the whole site or change unrelated notes unless the user asks.
