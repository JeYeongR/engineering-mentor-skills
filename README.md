# Engineering Mentor Skills

> English | [한국어](./README.ko.md)

[![skills.sh](https://skills.sh/b/JeYeongR/engineering-mentor-skills)](https://skills.sh/JeYeongR/engineering-mentor-skills)

A shared engineering mentor pack for Claude Code and Codex.

## Skills

- `/mentor` — automatic cross-domain router
- `/be-mentor` — backend
- `/fe-mentor` — frontend
- `/infra-mentor` — infrastructure

`/mentor` may combine multiple perspectives when the problem crosses boundaries, while prioritizing the engineering perspective explicitly requested by the user.

Examples:

```text
/mentor Next.js에서 Spring API 호출이 느린데 어디부터 봐야 해?
```

Routes to FE + BE, and may add Infra if the deployment/network boundary matters.

```text
/mentor Spring 서버를 Kubernetes에 배포했는데 502가 간헐적으로 나
```

Routes mainly to BE + Infra.

```text
/mentor 백엔드 개발자 관점에서 CI/CD를 공부하고 싶어
```

Uses BE as the primary perspective and Infra as a supporting perspective.

## Install with skills.sh

Install all skills from this repository:

```bash
npx skills add JeYeongR/engineering-mentor-skills
```

Install an individual skill:

```bash
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill mentor
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill be-mentor
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill fe-mentor
npx skills add https://github.com/JeYeongR/engineering-mentor-skills --skill infra-mentor
```

Update installed skills:

```bash
npx skills update
```
