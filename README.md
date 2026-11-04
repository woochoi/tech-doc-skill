# tech-doc 스킬

기술 주제를 블로그 스타일의 한국어 입문자용 기술 문서로 작성하는 Claude Code 스킬입니다.

## 폴더 구성

```
tech-doc-skill/
  SKILL.md                        # 진입점: 작성 순서, 핵심 규칙, 자주 하는 실수
  references/
    style-guide.md                # 톤·문장 패턴·시각 장치 세부 규칙
    publish-checklist.md          # 발행 전 점검 항목
    stack-glossary.md             # 스택별 용어 풀이·비유 모음 (Java/Spring/Kafka/Redis 등)
  templates/
    article-outline.md            # 글 뼈대 템플릿
    example-article.md            # 스타일 적용 견본 (Kafka Consumer Group)
```

## 설치

스킬 폴더를 아래 위치 중 하나에 복사하면 됩니다.

| 위치 | 의미 | 경로 |
| --- | --- | --- |
| 개인 스킬 | 모든 프로젝트에서 사용 | `~/.claude/skills/tech-doc-skill/` |
| 프로젝트 스킬 | 이 저장소에서만 사용(팀 공유) | `.claude/skills/tech-doc-skill/` |

예시:

```bash
cp -r tech-doc-skill ~/.claude/skills/
```

## 사용

직접 호출:

```
/tech-doc-skill
Redis 분산 락을 입문자용 기술 블로그로 정리해줘.
```

또는 자연어로 (description이 신호가 되어 자동 호출):

```
Spring Batch의 Chunk 처리 원리를 기술 스타일 입문 글로 써줘.
```

## 개선하는 법

기술 블로그 글이 알려준 방식 그대로입니다.

1. 글을 한 편 써본다.
2. 마음에 안 드는 지점을 찾는다. (용어 풀이 누락, 비유 남발, 원리 생략 등)
3. `SKILL.md`의 `자주 하는 실수(gotchas)`에 한 줄 추가한다.
4. 다시 써보고 비교한다.

처음부터 완벽할 필요는 없습니다. 실제 작업에서 나온 실수를 하나씩 적어가며 좋아집니다.
