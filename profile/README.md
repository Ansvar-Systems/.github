# Ansvar Systems

Legal, compliance, and security sources for AI agents — every answer cited to the official source.

## Connect your agent

The [Ansvar Gateway](https://gateway.ansvar.eu) serves the full corpus fleet through one MCP endpoint. The free tier gives 100 queries per day, no card required.

Claude Code (one line):

```bash
claude mcp add ansvar --transport http https://gateway.ansvar.eu/mcp
```

Claude Desktop / Cursor — add to `claude_desktop_config.json` (or `mcp.json`):

```json
{
  "mcpServers": {
    "ansvar": {
      "type": "url",
      "url": "https://gateway.ansvar.eu/mcp"
    }
  }
}
```

Claude.ai — Settings → Connectors → Add custom connector → paste `https://gateway.ansvar.eu/mcp`

First request opens an OAuth signup flow. Setup guide: [ansvar.eu/docs/quickstart](https://ansvar.eu/docs/quickstart)

## What's inside

- Statute-level law corpora across dozens of audited jurisdictions, EU/EFTA/UK and international — see the [coverage map](https://ansvar.eu/coverage)
- Sector regulators: financial, cybersecurity, data protection, competition
- Security intelligence: CVE/KEV/EPSS, MITRE ATT&CK, CWE/CAPEC, OWASP
- Compliance workflows: threat modeling, DPIA, gap analysis — see [tiers](https://ansvar.eu/pricing)

Every served row carries a citation with source URL, publisher, and license.

## Open source

- [agent-affect-skills](https://github.com/Ansvar-Systems/agent-affect-skills) — skills that let coding agents report friction, embarrassment, and load-bearing weirdness at the end of a task ([docs](https://ansvar.eu/docs/agent-skills))
- [ansvar-compliance-skills](https://github.com/Ansvar-Systems/ansvar-compliance-skills) — Claude skills for CRA vulnerability obligations, regulatory threat modeling, and incident-reporting navigation

## Why the databases aren't in the repos

The public law-MCP repos ship the schema and ingestion code. Pre-built databases stay on Ansvar infrastructure because TDM and standards-licensing constraints on the upstream sources keep us from redistributing the corpus as a public artifact. Each repo's README explains its self-host path.
