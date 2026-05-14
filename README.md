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

## Pricing

JubJub uses two unrelated pricing models — which one applies depends on who is calling.

**Humans signed in at studio.jubjubapp.com** pay an AUD subscription via Stripe: Free ($0), Creator ($39/mo, or $31/mo on annual at 20% off), or Studio ($199/mo, or $159/mo on annual at 20% off). All plans include unlimited multi-platform publishing, on-chain records, and unmetered tool access. Plans differ in workspace permanence (7 days on Free, permanent on Creator and Studio), storage permanence, and collections.

**Autonomous agents** without a human session pay per action in USDC via x402 (Base) or MPP (Tempo): `contents_create` and `launches_create` are $0.25 each, `get_publish_recommendations` is $0.002, and `get_content_analytics`, `get_platform_comparison`, `get_content_ownership`, `get_content_revenue`, and `get_creator_intelligence` are $0.005 each. Both Creator and Studio subscribers are exempt from per-action charges.

**On-chain gas** is paid by the JubJub treasury — users and agents never pay gas for contract deploys, token mints, publish-ledger writes, or streaming settlement. Streaming revenue is split 97/3 inside the smart contract: 97% to rights holders, 3% to JubJub treasury. This split is immutable on-chain.

## Requirements

- An active JubJub account ([free signup](https://studio.jubjubapp.com/auth?tab=signup); paid plans optional)
- Social platform accounts connected in JubJub before publishing (Profile → Platforms)
- OpenClaw with any supported LLM (Claude, GPT, DeepSeek)

## Support

- **Docs:** [jubjubapp.com](https://jubjubapp.com)
- **Issues:** Open a GitHub issue in this repo

## License

MIT
