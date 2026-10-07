# KNX-MCP Skills

This directory is the public home for **reusable AI skills, prompts and workflows** built around KNX-MCP.

A skill should help an MCP-capable assistant perform a repeatable KNX/ETS task while keeping the user in control.

## What belongs here

Examples:

- project review and handover checks
- group-address quality checks
- room or floor inventory workflows
- troubleshooting workflows
- documentation and reporting prompts
- safe commissioning checklists

Skills must be generic enough to work across projects. Do not include customer-specific addresses, project names, credentials or keys.

## Recommended structure for each skill

Each skill should state:

1. **Purpose** — what problem it solves.
2. **Prerequisites** — ETS version, KNX-MCP version or project assumptions.
3. **Safety level** — read-only, project changes, bus access, or device programming.
4. **Required permissions** — which KNX-MCP tool groups need to be allowed or confirmed.
5. **Workflow** — the steps the assistant should follow.
6. **Confirmation points** — where the user must make a decision.
7. **Example request** — a realistic user prompt.
8. **Expected result** — what a successful run should produce.

## Safety rules

A public skill should never instruct an assistant to bypass KNX-MCP confirmations, disable safeguards, expose access keys or program devices without explicit user approval.

For write operations, prefer a workflow that first inspects the existing project, explains the planned change and then uses the configured KNX-MCP permission model.
