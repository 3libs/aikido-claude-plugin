# Changelog

All notable changes to the Aikido Security Claude Code plugin are documented here.

## [Unreleased]

### Added

- **Automatic scanning via a `PostToolUse` hook** (`hooks/hooks.json`). After
  Claude writes or edits a file (`Write`, `Edit`, or `MultiEdit`), the hook invokes
  the `scan` skill on first-party source changes to check for SAST vulnerabilities,
  exposed secrets, and IaC misconfigurations, then remediate and re-verify. Non-code
  changes (documentation, assets, lockfiles without source changes) are skipped.
  This brings the Claude Code plugin to parity with the Cursor plugin (always-apply
  rule) and the Kiro plugin (`postToolUse` hook), which already scan automatically
  after edits.
- **README banner** (`assets/banner.svg`), built from the official Aikido logo mark.

### Changed

- **`README.md`** — documented the automatic-scanning behavior under a new
  "Automatic scanning" section.
