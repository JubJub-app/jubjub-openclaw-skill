# JubJub OpenClaw Skill

## Overview

This repo contains the JubJub SKILL.md for the ClawHub/OpenClaw
agent runtime registry. The SKILL.md defines all JubJub MCP tools
for installation into any OpenClaw-compatible agent.

## Key Files

- SKILL.md — the skill definition (frontmatter + tool descriptions)
- README.md — installation instructions

## Deploy

Publish via ClawHub CLI — do not create PRs to clawhub directly.
The clawhub repo has a vendor copy at clawhub/jubjub/SKILL.md
that must be kept in sync.

## Rules

- SKILL.md frontmatter must be valid YAML
- All 79 MCP tools must be documented
- Tool descriptions are the most reliable signal for the MCP
  model — write them as decision-time instructions, not docs
- version field must be incremented on every publish
- Requires env: JUBJUB_API_KEY
- Auth header: X-JubJub-Agent-Key: jjagent_...
- Base URL: https://api.jubjubapp.com
