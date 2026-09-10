# Engineering Mentor Skills

> [English](./README.md) | 한국어

[![skills.sh](https://skills.sh/b/JeYeongR/engineering-mentor-skills)](https://skills.sh/JeYeongR/engineering-mentor-skills)

백엔드, 프론트엔드, 인프라 문제를 함께 고민하고 방향을 잡아주는 엔지니어링 멘토 스킬 모음입니다.

## 스킬

- `/mentor` — 문제의 성격을 판단해 백엔드, 프론트엔드, 인프라 관점을 하나 이상 조합하는 진입점입니다. 아키텍처, 장애 분석, 성능, 설계 판단처럼 경계가 섞인 질문에 적합합니다.
- `/be-mentor` — Java, Spring, JPA, 데이터베이스, 동시성, 트랜잭션, 메시징, 분산 시스템을 다룹니다. 정확성, 장애 복구, 운영 영향까지 포함해 백엔드 의사결정을 함께 검토합니다.
- `/fe-mentor` — JavaScript/TypeScript, 브라우저, React, Next.js, 렌더링, 상태, 데이터 패칭을 다룹니다. 사용자 경험, 접근성, 보안, 성능 관점에서 프론트엔드 문제를 살핍니다.
- `/infra-mentor` — Linux, 네트워크, Docker, Kubernetes, 클라우드, CI/CD, 관측성을 다룹니다. 배포 환경의 실패 지점, 복구, 확장성, 보안, 비용을 함께 고려합니다.

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
