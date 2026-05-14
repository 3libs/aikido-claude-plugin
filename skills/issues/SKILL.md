---
name: issues
description: Fetches Aikido security issues from the Aikido feed. Use when the user asks to list, show, count, summarize, triage, or fix feed issues, or scopes by cloud, repo, VM, domain, or container.
---

When listing Aikido feed issues:

1. Use **aikido-mcp:aikido_issues_list**
2. Call it when the user wants to list, show, count, or summarize Aikido feed issues; when they scope by cloud, repo, VM, domain, or container; or when you need the current issue set before triage or fixes.
3. Pass scope fields only when the user (or workspace context) supplies them: `cloud_name`, `repo_name`, `vm_name`, `domain_name`, `container_name`. For “this repo”.
4. Optional `issue_types` (array): `open_source`, `leaked_secret`, `cloud`, `sast`, `iac`, `surface_monitoring`, `malware`, `eol`, `mobile`, `docker_container`, `cloud_instance`, `scm_security`, `license`, `ai_pentest` — e.g. include `leaked_secret` for secrets. Omit when no category filter is needed.
5. Pagination: use numeric `page` only when the user needs more than the first page of results.
6. Present each issue exactly in this form (increment `#`):
   ```
   Issue #1: <issue_title>
    - Issue type: <issue_type>
    - Severity: <issue_severity>
    - Remediation: <issue_remediation>
   ```
7. Report how many issues are on this page; note if more pages may exist.
8. Keep `issue_remediation` verbatim for any follow-up fix steps.

If the Aikido MCP server is not available or fails, inform the user:

> The Aikido MCP server is required for Aikido feed issues but is not available.
> Install it following the setup guide at [reference.md](../scan/reference.md), or run `/aikido:setup`, then retry.
