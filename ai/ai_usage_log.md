# AI Usage Log — {{PROJECT_NAME}}

A project of the University of Scranton Amateur Radio Club (W3USR).

This log records every substantive AI-assisted session for "{{PROJECT_TITLE}}".

Required by the University of Scranton AI Policy, the HamSCI Generative AI Use Agreement,
NASA and NSF guidance on generative AI in funded research, and {{FUNDER}} expectations.
See `.claude/rules/ai-governance.md`.

**At instantiation:** replace the placeholders above and delete every entry below the
append marker, including the example and any entries inherited from the template repository.
This log records *this* project's sessions. Entries are appended newest at the bottom, and the
`/commit` command writes them for you.

---

## Entry format

```
## [YYYY-MM-DD HH:MM TZ]
- **Tool**: Claude (Anthropic), <exact-model-id>
- **Session Purpose**: What this session set out to do
- **Sections/Files Affected**: The specific files or documents touched
- **Nature of Contribution**: Draft / Edit / Analysis / Code generation / Research / Scaffolding
- **Human Review Status**: Reviewed and verified / Partially reviewed / Pending review
- **Git Hash**: Filled in after committing
```

Date and time come from the system clock via `date`, never from an estimate. The Tool field
carries the actual running model ID.

---

<!-- Append new entries below this line, newest at the bottom. -->

## [EXAMPLE — delete this entry] [2026-09-01 19:04 EDT]
- **Tool**: Claude (Anthropic), claude-opus-5
- **Session Purpose**: Draft the station setup page for the club website and verify the
  equipment list against the shack inventory sheet.
- **Sections/Files Affected**: `web/station.html`, `web/assets/station.css`
- **Nature of Contribution**: Draft and edit; equipment list verified against the inventory
  sheet by {{NAME, CALLSIGN}}
- **Human Review Status**: Reviewed and verified
- **Git Hash**: 0000000

## [2026-09-12 13:35 UTC]
- **Tool**: Claude (Anthropic), claude-opus-5
- **Session Purpose**: Fork the W2NAF academic project template into a W3USR club template:
  rewrite the scaffold so it is directly applicable to University of Scranton Amateur Radio
  Club projects, add amateur-radio operating governance and a student-facing onboarding
  guide, and repoint the repository from `w2naf-academia` to `w3usr`.
- **Sections/Files Affected**: `CLAUDE.md` (rewritten), `README.md` (rewritten),
  `.gitignore` (secrets, Node/web, bulk-data sections added),
  `ai/ai_usage_log.md` (reset as a W3USR template with a format block and example entry),
  `.claude/commands/commit.md` (added a pre-commit sensitive-material check and submodule
  push-order verification), `.claude/rules/ai-governance.md` (rewritten: FCC, ARDC, FERPA,
  coursework conflict, disclosure table), `.claude/rules/latex-writing.md` and
  `.claude/rules/python-code.md` (reworked for club use),
  `.claude/rules/amateur-radio-operations.md` (new), `.claude/rules/web-development.md` (new),
  `docs/ONBOARDING.md` (new). Git remote repointed to `git@github.com:w3usr/ai_project_template.git`.
- **Nature of Contribution**: Draft and scaffolding; policy text drafted from the prior
  template and from the applicable institutional, funder, and FCC policies
- **Human Review Status**: Pending review — the Part 97 section citations in
  `.claude/rules/amateur-radio-operations.md`, and the club roles named in `CLAUDE.md`,
  need verification by the trustee or advisor before this template is used for a real project
- **Git Hash**: f745d39
