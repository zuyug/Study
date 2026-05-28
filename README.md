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

## 노트 추가 규칙

Codex 또는 Claude에게 `노트추가`라고 말하면 `AGENTS.md`와 `CLAUDE.md`의 규칙에 따라 새 노트와 복습 카드를 추가합니다.
