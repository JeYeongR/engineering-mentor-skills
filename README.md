# Engineering Mentor Skills

A shared engineering mentor pack for Claude Code and Codex.

## Skills

- `/mentor` — automatic cross-domain router
- `/be-mentor` — backend
- `/fe-mentor` — frontend
- `/infra-mentor` — infrastructure

`/mentor` may combine multiple perspectives when the problem crosses boundaries.

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
/mentor 웹 페이지가 느린데 API도 느린 것 같아
```

May use FE + BE + Infra for an end-to-end diagnosis.

## Install with skills CLI

Publish this repository to GitHub, then from a target project:

```bash
npx skills add <owner>/<repo>
```

Or install an individual skill:

```bash
npx skills add https://github.com/<owner>/<repo> --skill mentor
npx skills add https://github.com/<owner>/<repo> --skill be-mentor
npx skills add https://github.com/<owner>/<repo> --skill fe-mentor
npx skills add https://github.com/<owner>/<repo> --skill infra-mentor
```

Update:

```bash
npx skills update
```

## Hooks and MCP

See `docs/HOOKS_MCP.md`.

The default design intentionally requires neither Hooks nor a custom MCP server.
Skills own mentoring behavior; Hooks are for lifecycle/safety automation; MCP is for external evidence and tools.
