# Engineering Mentor Skills

> [English](./README.md) | 한국어

[![skills.sh](https://skills.sh/b/JeYeongR/engineering-mentor-skills)](https://skills.sh/JeYeongR/engineering-mentor-skills)

Claude Code와 Codex에서 사용할 수 있는 엔지니어링 멘토 스킬 모음입니다.

## 스킬

- `/mentor` — 여러 엔지니어링 영역을 자동으로 판단하는 라우터
- `/be-mentor` — 백엔드
- `/fe-mentor` — 프론트엔드
- `/infra-mentor` — 인프라

`/mentor`는 문제가 여러 영역에 걸쳐 있을 경우 여러 관점을 조합할 수 있으며, 사용자가 명시적으로 요청한 엔지니어링 관점을 우선합니다.

예시:

```text
/mentor Next.js에서 Spring API 호출이 느린데 어디부터 봐야 해?
```

FE + BE 관점으로 라우팅하며, 배포나 네트워크 경계가 중요하면 Infra 관점을 추가할 수 있습니다.

```text
/mentor Spring 서버를 Kubernetes에 배포했는데 502가 간헐적으로 나
```

주로 BE + Infra 관점으로 라우팅합니다.

```text
/mentor 백엔드 개발자 관점에서 CI/CD를 공부하고 싶어
```

BE를 주 관점으로 사용하고 Infra를 보조 관점으로 사용합니다.

## skills.sh로 설치

이 저장소의 모든 스킬을 설치합니다:

```bash
npx skills add JeYeongR/engineering-mentor-skills
```

특정 스킬만 설치합니다:

```bash
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill mentor
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill be-mentor
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill fe-mentor
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill infra-mentor
```

설치된 스킬을 업데이트합니다:

```bash
npx skills update
```


## Hooks와 MCP

`docs/HOOKS_MCP.md`를 참고하세요.

기본 설계에서는 Hooks나 별도의 MCP 서버를 필수로 요구하지 않습니다.
Skill은 멘토링 동작을 담당하고, Hooks는 lifecycle/safety 자동화를 담당하며, MCP는 외부 근거와 도구를 사용할 때 활용합니다.
