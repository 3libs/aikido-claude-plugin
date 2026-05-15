# Aikido Security — Claude Code Plugin

Brings [Aikido Security](https://aikido.dev) directly into Claude Code via the Aikido MCP server. Scan code you write or modify for vulnerabilities and secrets, request findings from your Aikido security feed.

## Skills

The plugin includes three skills that Claude uses automatically

| Skill | Command | What it does |
| --- | --- | --- |
| **Setup** | `/aikido:setup` | Configures your Aikido API key, checks Node.js (18.19+), and verifies the MCP server. Pass your key for one-step setup: `/aikido:setup <your-api-key>`. |
| **Scan** | `/aikido:scan` | Runs a full security scan on generated or modified files (SAST, secrets, IaC). |
| **Issues** | `/aikido:aikido-issues` | Lists, counts, and summarizes issues from your Aikido security feed — SAST, IaC, SCA, leaked secrets, cloud, containers, EOL, licenses, malware, and more. Filter by cloud, repo, VM, domain, or container. |

## Installation and setup

Check out the [installation and setup guide](https://help.aikido.dev/ai-and-dev-tools/aikido-mcp/anthropic-claude-code-mcp) for detailed guidance on how to setup the Aikido Claude Code Plugin.

## More information

- [Aikido MCP documentation](https://help.aikido.dev/mcp/anthropic-claude-code-mcp)
- [Aikido Security](https://aikido.dev)
