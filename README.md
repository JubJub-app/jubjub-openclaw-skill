# JubJub Skill for OpenClaw

Publish content across multiple platforms, collaborate with your team, and maintain verified publish history — all through your OpenClaw agent.

## What JubJub Does

[JubJub](https://jubjubapp.com) is a content publishing and team collaboration platform for creators and media teams. With this skill, your OpenClaw agent can:

- **Publish content** to TikTok, Instagram, YouTube, LinkedIn, and Vimeo
- **Manage content workflows** — create, update, schedule, and track content items
- **Collaborate with your team** — send messages, manage workspaces and teams
- **Track publish history** — every publish action creates a verified record, giving you immutable proof of ownership and distribution

## Setup

1. Go to [jubjubapp.com](https://jubjubapp.com) and create an account
2. Navigate to **Profile → Agents**
3. Click **New Agent** and give it a name (e.g. "OpenClaw")
4. Copy your API key — it starts with `jjagent_`
5. Add it to your OpenClaw config:

```yaml
skills:
  entries:
    - skill: jubjub
      apiKey: jjagent_YOUR_KEY_HERE
```

Or pass it as an environment variable:

```bash
JUBJUB_API_KEY=jjagent_YOUR_KEY_HERE
```

## Installation

### Via ClawHub CLI
```bash
clawhub install jubjub
```

### Direct from GitHub
Paste this URL into your OpenClaw agent chat:
```
https://github.com/jubjubapp/jubjub-openclaw-skill
```

## Example Prompts

Once installed, try saying to your agent:

- *"Publish my latest video to Instagram and TikTok"*
- *"Show me all content in my workspace"*
- *"Message my team that the edit is ready for review"*
- *"What's the publish history for my last YouTube upload?"*
- *"Create a new content item called 'March Campaign'"*
- *"List all my connected platforms"*

## Requirements

- An active JubJub account ([Creator](https://jubjubapp.com) $25/mo or [Studio](https://jubjubapp.com) $129/mo)
- Social platform accounts connected in JubJub before publishing (Profile → Platforms)
- OpenClaw with any supported LLM (Claude, GPT, DeepSeek)

## Support

- **Docs:** [jubjubapp.com](https://jubjubapp.com)
- **Issues:** Open a GitHub issue in this repo

## License

MIT
