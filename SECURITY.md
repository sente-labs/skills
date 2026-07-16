# Security

This skill handles the most sensitive category there is — account credentials and verification
codes — so provenance matters.

## Official sources (the complete list)

- This repo: `github.com/sente-labs/skills`
- Website / hosted skill: `https://sente.run` / `https://sente.run/skill.md`
- npm: [`@sente-labs/cli`](https://www.npmjs.com/package/@sente-labs/cli),
  [`@sente-labs/sdk`](https://www.npmjs.com/package/@sente-labs/sdk)
- PyPI: [`sente-sdk`](https://pypi.org/project/sente-sdk/)
- API: `https://api.sente.run/v1`

Any skill, package, or registry entry using the Sente name outside this list is **not ours**.
Skill registries have had real typosquatting/malware campaigns — check the source repo before
installing anything that asks for an API key.

## What this skill does and doesn't do

- It wraps the published `@sente-labs/cli`. It does not embed credentials, does not send your data
  anywhere except `api.sente.run`, and instructs agents to never print the API key.
- Connected-account credentials are vaulted **write-only** server-side (they cannot be read back
  via the API) and are purged on `sente connection delete`.
- Email content is treated as untrusted input end-to-end (prompt-injection-hardened extraction).

## Reporting

Vulnerabilities, abuse, or impersonation: **support@sente.run**. If you operate a site and want
Sente to stop registering against it, tell us and we will honor it.
