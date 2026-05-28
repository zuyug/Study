---
name: study-note-html-updater
description: Add the user's recently answered study topic into their categorized HTML study note. Use when the user says "노트추가", "정리노트 추가", "HTML에 추가", "방금 내용 노트에 넣어줘", or asks to save a prior answer into a study note, especially for stock/investing or coding questions.
---

# Study Note HTML Updater

## Goal

Update the user's study HTML so the latest answered topic becomes a durable, readable note.

Default target in this workspace:

```text
C:\Users\kjh\Desktop\coding 프로젝트\거시경제 기반 기술지표 단타 프로그램\학습_노트.html
```

If the file is not present, search the current workspace for `학습_노트.html` or ask for the target only if it cannot be found.

## Workflow

1. Identify the source answer to save. Prefer the assistant's immediately previous explanation unless the user points to a different topic.
2. Choose the category:
   - Use `stock` / `주식` for investing, finance, accounting, indicators, macro, trading, valuation, financial statements.
   - Use `code` / `코딩` for programming, tools, errors, APIs, automation, GitHub, HTML/CSS/JS/Python.
   - If both apply, choose the main learning intent and mention the assumption briefly.
3. Add one new note block to the matching category in `학습_노트.html`.
4. Preserve the existing visual system, CSS, sidebar, search behavior, responsive behavior, and source footer.
5. Update sidebar links and category counts.
6. Keep the article beginner-friendly:
   - title
   - category badges
   - one-line summary box
   - 2-4 core concept cards or short sections
   - examples when useful
   - "주의할 점" or "다시 기억할 문장" details when useful
7. Validate with an HTML parser or a browser/headless screenshot when feasible.
8. If the user also asks to publish, push the updated HTML to the requested GitHub repository.

## Editing Rules

- Use the existing IDs and naming style. Create stable IDs like `stock-per-pbr-roe` or `code-python-function-variable`.
- Do not replace the whole document unless the file is badly malformed.
- Do not add a new framework or external dependency.
- Keep Korean copy natural and concise.
- For mobile readability, avoid oversized headings inside articles.
- When using sources from web search, cite them in the footer or in the final response.

## GitHub Publishing

When the user asks to upload this note to GitHub, prefer the repository they named. For the user's current study repo, use:

```text
zuyug/Study
```

Publish only the study HTML and necessary preview assets unless the user asks for more. Use a clear commit message such as:

```text
Add categorized study note HTML
```
