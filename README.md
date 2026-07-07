![Aikido Security — Claude Code Plugin](./assets/banner.svg)

# Aikido Security — Claude Code Plugin
All notable changes I made to the Aikido Security Claude Code plugin are documented here.

## Installation and setup

Check out the [installation and setup guide](https://help.aikido.dev/ai-and-dev-tools/aikido-mcp/anthropic-claude-code-mcp) for detailed guidance on how to setup the Aikido Claude Code Plugin.

## Automatic scanning

The plugin registers a `PostToolUse` hook (`hooks/hooks.json`) that fires after
Claude writes or edits a file. When first-party source code changes, it invokes the
`scan` skill to scan the modified files for SAST vulnerabilities, exposed secrets,
and IaC misconfigurations, then remediate and re-verify — so generated code is
checked before it ships, without you having to ask. Non-code changes (docs, assets)
are skipped. This brings the Claude Code plugin to parity with the Cursor and Kiro
plugins, which already scan automatically after edits.

## More information

- [Aikido MCP documentation](https://help.aikido.dev/mcp/anthropic-claude-code-mcp)
- [Aikido Security](https://aikido.dev)
