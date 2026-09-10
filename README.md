# Engineering Mentor Skills

> English | [한국어](./README.ko.md)

[![skills.sh](https://skills.sh/b/JeYeongR/engineering-mentor-skills)](https://skills.sh/JeYeongR/engineering-mentor-skills)

Engineering mentor skills that help users think through and find direction in backend, frontend, and infrastructure problems.

## Skills

- `/mentor` — The entry point for questions that span one or more domains. It combines backend, frontend, and infrastructure perspectives for architecture, debugging, performance, and design decisions.
- `/be-mentor` — Covers Java, Spring, JPA, databases, concurrency, transactions, messaging, and distributed systems. It weighs correctness, failure recovery, and operational consequences alongside implementation details.
- `/fe-mentor` — Covers JavaScript/TypeScript, browsers, React, Next.js, rendering, state, and data fetching. It examines frontend work through user experience, accessibility, security, and performance.
- `/infra-mentor` — Covers Linux, networking, Docker, Kubernetes, cloud, CI/CD, and observability. It considers failure modes, recovery, scalability, security, and cost in production environments.

`/mentor` may combine multiple perspectives when the problem crosses boundaries, while prioritizing the engineering perspective explicitly requested by the user.

Examples:

```text
/mentor Where should I start if calling a Spring API from Next.js is slow?
```

Routes to FE + BE, and may add Infra if the deployment/network boundary matters.

```text
/mentor My Spring server is running on Kubernetes, but I'm getting intermittent 502 errors.
```

Routes mainly to BE + Infra.

```text
/mentor I want to learn CI/CD from a backend developer's perspective.
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
