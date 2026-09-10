# Hooks and MCP Strategy

## Recommendation

Use Skills for mentoring behavior and routing.

Do not require Hooks or MCP for the mentor to work.

### Why

- Skills are the reusable behavioral layer.
- Hooks are lifecycle/tool-use automation and policy.
- MCP is for connecting external tools and data.

Keeping these responsibilities separate avoids hidden behavior and unnecessary context.

## Claude Code Hooks

Good uses:
- protect dangerous infrastructure commands
- run lightweight validation before/after specific tool operations
- enforce project safety policies
- optionally emit a small session-start reminder

Avoid:
- injecting the full mentor prompt every session
- duplicating SKILL.md in hooks
- automatically blocking normal coding just because mentoring is enabled

A particularly useful future hook for `infra-mentor` is a `PreToolUse` policy that requires explicit confirmation for destructive commands such as production Terraform apply/destroy or Kubernetes deletion.

Claude Code supports hook-based runtime permission decisions and `PreToolUse` can participate before the normal permission system.

## MCP

Do not build a custom mentor MCP merely to store the mentoring prompt.

MCP becomes valuable when mentoring needs live evidence, for example:
- GitHub/issues/PR context
- monitoring/incident data
- cloud/Kubernetes state
- internal documentation
- design sources
- databases or operational tools

Then the pattern is:

Skill = how to reason
MCP = what real-world evidence/tools are available

For example:
`/mentor API가 느려`
→ BE: inspect request/DB behavior
→ Infra: inspect metrics/traces/deployment
→ MCP: retrieve actual monitoring or repository evidence if connected

## Codex

Keep portable behavior in Skills and AGENTS.md.

Codex includes skill metadata in its assembled context when skills are configured. Use MCP/plugins/apps for external tools where supported instead of trying to reproduce Claude-specific hooks.

## Current recommendation

Start with:
- mentor
- be-mentor
- fe-mentor
- infra-mentor

No mandatory hook.
No custom MCP server.

Add integrations only when you have an actual data source or safety policy that needs them.
