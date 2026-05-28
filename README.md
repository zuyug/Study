# Study Notes

질문하고 이해한 내용을 다시 읽기 쉽도록 쌓는 개인 학습 노트입니다.

## 구조

```text
docs/
  economy/   경제, 주식, 투자, 재무제표
  coding/    코딩, 자동화, GitHub
  ai/        Codex, Claude, 프롬프트, AI 도구
  life/      생활 지식과 기타 배움
  review/    Anki 복습 카드
```

## 로컬 미리보기

```bash
pip install -r requirements.txt
mkdocs serve
```

## 빌드 검증

```bash
mkdocs build --strict
```

## GitHub에서 보기

현재 저장소가 private이고 현재 GitHub 플랜에서 private repository Pages가 지원되지 않아 GitHub Pages 자동 배포는 비활성 템플릿으로 보관합니다.

- GitHub에서는 `docs/` 아래 Markdown 파일을 바로 볼 수 있습니다.
- 휴대폰에서도 GitHub 앱/모바일 웹에서 Markdown 노트를 볼 수 있습니다.
- 나중에 저장소를 public으로 바꾸거나 private Pages 지원 플랜을 쓰면 `.github/workflows/deploy-pages.yml.disabled`를 `.github/workflows/deploy.yml`로 바꾸고 Pages를 GitHub Actions로 켜면 됩니다.

## 노트 추가 규칙

Codex 또는 Claude에게 `노트추가`라고 말하면 `AGENTS.md`와 `CLAUDE.md`의 규칙에 따라 새 노트와 복습 카드를 추가합니다.
