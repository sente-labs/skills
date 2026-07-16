# Sente Skills

Official agent skills for [Sente](https://sente.run) — managed email identities and real,
durable accounts for AI agents.

This is the **only official source** for Sente skills. Verify provenance: this repo is
`github.com/sente-labs/skills`, linked from [sente.run](https://sente.run). Our published packages
are [`@sente-labs/cli`](https://www.npmjs.com/package/@sente-labs/cli) /
[`@sente-labs/sdk`](https://www.npmjs.com/package/@sente-labs/sdk) on npm and
[`sente-sdk`](https://pypi.org/project/sente-sdk/) on PyPI. Anything else using the Sente name is
not ours — see [SECURITY.md](SECURITY.md).

## Skills

| Skill | What it does |
|---|---|
| [`sente`](skills/sente/SKILL.md) | Give an agent its own email identity; wait on OTPs/magic links; register new accounts at web apps; connect accounts the user already owns. |

## Install

The skill follows the [AgentSkills](https://agentskills.io) open standard (SKILL.md), so it works
across compatible agents:

```bash
# skills.sh (Claude Code, Cursor, Codex, and 70+ agents)
npx skills add sente-labs/skills

# OpenClaw
openclaw skills install <clawhub slug>        # or: clone and copy skills/sente to ~/.openclaw/skills

# Hermes
hermes skills install https://raw.githubusercontent.com/sente-labs/skills/main/skills/sente/SKILL.md

# Anything else that reads SKILL.md directories
git clone https://github.com/sente-labs/skills && cp -r skills/skills/sente <your agent's skills dir>
```

Or point a coding agent at the hosted variant for wiring email into a service's codebase:
paste `https://sente.run/skill.md` into it.

## What is Sente?

Most of the web needs an account, and an agent has no way to get or keep one. Sente gives the agent
a real email address it owns, extracts verification codes and magic links server-side, drives a
real browser to register accounts (autonomous, or confirm-before-submit so a human clicks the final
button), and can connect accounts the user already owns — credentials vaulted write-only,
authenticator (TOTP) re-login, revocable at any time.

Acceptable use in one line: accounts your org is accountable for, at targets that permit it — no
account farming, no CAPTCHA circumvention, no spam.

## License

MIT
