# Engineering Mentor Skills

> [English](./README.md) | 한국어

[![skills.sh](https://skills.sh/b/JeYeongR/engineering-mentor-skills)](https://skills.sh/JeYeongR/engineering-mentor-skills)

백엔드, 프론트엔드, 인프라 영역의 기술 학습과 설계·디버깅·코드 리뷰를 돕는 엔지니어링 멘토 Agent Skills 모음입니다.

단순히 정답을 알려주는 대신, 사용자가 이미 알고 있는 내용을 먼저 설명하도록 유도하고 그 설명에서 중요한 빈틈을 찾아 질문을 확장합니다. 선행 지식이 부족한 경우에는 필요한 개념을 먼저 설명합니다.

## 포함된 스킬

- `/mentor` — 질문의 주제와 관점을 파악해 적절한 멘토를 선택하거나 여러 관점을 조합
- `/be-mentor` — Backend
- `/fe-mentor` — Frontend
- `/infra-mentor` — Infrastructure

`/mentor`는 기술 키워드만으로 라우팅하지 않고, 사용자가 명시한 엔지니어링 관점을 우선합니다.

예:

```text
/mentor 백엔드 개발자 관점에서 CI/CD를 공부하고 싶어
```

→ `be-mentor`를 주 관점으로 사용하고, 필요한 인프라 내용만 `infra-mentor` 관점으로 보완합니다.

```text
/mentor Spring 서버를 Kubernetes에 배포했는데 502가 간헐적으로 나
```

→ 주로 Backend + Infra 관점에서 분석합니다.

```text
/mentor 웹 페이지가 느린데 API도 느린 것 같아
```

→ 문제 경계에 따라 Frontend + Backend + Infra를 함께 사용할 수 있습니다.

## skills.sh로 설치

이 저장소의 스킬을 한 번에 설치:

```bash
npx skills add JeYeongR/engineering-mentor-skills
```

특정 스킬만 설치:

```bash
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill mentor
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill be-mentor
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill fe-mentor
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill infra-mentor
```

설치된 스킬 업데이트:

```bash
npx skills update
```

공개 GitHub 저장소의 스킬을 사용자가 skills CLI로 설치하면 익명 설치 통계가 수집되어 skills.sh 생태계와 leaderboard에 자동으로 반영될 수 있습니다.

## 멘토링 방식

사용자가 이미 공부했거나 구현한 주제라면 자신의 말로 먼저 설명하게 하고, 설명에서 중요한 빈틈이나 모호한 표현을 찾습니다.

기본 흐름:

1. 무엇을 공부하거나 경험했는지 파악
2. 알고 있는 내용은 먼저 설명하도록 유도
3. 중요한 빈틈이나 모호한 표현 하나를 선택
4. 정확한 의미와 이유 확인
5. 조건을 하나 바꿔 다시 생각
6. 운영 환경으로 확장
7. Trade-off 확인
8. 부족한 부분만 설명
9. 필요하면 구현과 테스트로 검증

모든 질문을 퀴즈처럼 되묻지는 않습니다. 선행 지식이 부족하면 먼저 설명합니다.

## 중요하게 보는 관점

- 왜 이렇게 동작하는가?
- 범위는 어디까지인가?
- 조건이 바뀌면 어떻게 되는가?
- 동시 요청이 들어오면?
- 일부만 실패하면?
- Timeout / Retry가 발생하면?
- 여러 서버에서 실행되면?
- 중복 요청은 안전한가?
- 장애를 어떻게 관측하고 복구할 것인가?
- 다른 선택과 비교했을 때 Trade-off는 무엇인가?
- 어떻게 테스트하고 검증할 것인가?

## AI로 생성한 코드

AI로 코드를 작성하는 것 자체를 문제로 보지 않습니다.

대신 프로젝트에 들어간 코드는 최소한 다음을 설명할 수 있어야 합니다.

- 왜 필요한가
- 주요 흐름은 어떻게 동작하는가
- 어떤 기술이나 라이브러리에 의존하는가
- 어떤 상황에서 실패할 수 있는가
- 어떤 Trade-off가 있는가
- 어떻게 테스트하고 검증할 것인가

목표는 AI가 만든 코드를 사용자의 지식으로 전환하는 것입니다.

## 코드 리뷰

대체로 다음 순서로 검토합니다.

```text
Intent
→ Correctness
→ Concurrency
→ Transaction
→ Failure
→ Edge Cases
→ Maintainability
→ Performance
```

실제 문제와 관련 있는 항목에 집중하고, 모든 항목을 억지로 적용하지 않습니다.

## 깊이 조절

- **Essential** — 지금 이해하거나 구현하기 위해 필요한 내용
- **Useful** — 디버깅, 설계, 성능, 운영에 도움이 되는 내용
- **Deep Dive** — 내부 구현이나 깊은 원리가 실제로 필요할 때

깊게 아는 것 자체보다 왜 알아야 하는지를 중요하게 봅니다.

## Hooks와 MCP

자세한 내용은 `docs/HOOKS_MCP.md`를 참고하세요.

기본 Mentor Skill은 Hook이나 별도의 MCP 서버를 필수로 요구하지 않습니다.

- Skill — 멘토의 행동과 사고 방식
- Hook — lifecycle / safety 자동화
- MCP — 외부 시스템과 실제 데이터에 접근할 때 사용

## 저장소 구조

```text
engineering-mentor-skills/
├── README.md
├── README.ko.md
├── docs/
│   └── HOOKS_MCP.md
└── skills/
    ├── mentor/
    ├── be-mentor/
    ├── fe-mentor/
    └── infra-mentor/
```
