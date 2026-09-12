---
paths:
  - "**/*.py"
  - "pyproject.toml"
  - "requirements.txt"
  - "requirements*.txt"
---

# Python Code Rules
*Delete this file if the project includes no Python.*

Common club uses: log parsing and ADIF handling, propagation and WSPR/PSKReporter analysis,
satellite pass prediction, rig or rotator control, dashboards, data plotting.

## Code Standards
- Follow the existing structure; introduce a new abstraction only with a reason you can state
- Keep `requirements.txt` or `pyproject.toml` current when adding a dependency
- Never commit credentials, API keys, or station passwords; use environment variables and a
  gitignored `.env`
- Write code a club member who joins next semester can read. Name things plainly, and comment
  the parts that are non-obvious rather than the parts that are obvious.

## Code That Touches the Radio
Anything that controls a rig, a rotator, an amplifier, or a transmit path is covered by
`.claude/rules/amateur-radio-operations.md`. In short: a licensed control operator supervises
it, it identifies per 97.119, and it does not transmit on a schedule of its own until the
control method has been worked out with the trustee.

- Default to receive-only and to dry-run modes. Make transmitting an explicit opt-in, never
  the default behavior of a script someone runs to see what it does.
- Guard destructive or irreversible actions (uploading a log, sending a spot, keying a
  transmitter) behind a confirmation.

## Data Handling
- Copy a real log before operating on it; never edit the original in place
- Keep test fixtures clearly named as fixtures so no one mistakes them for real contacts
- Bulk data stays out of git; fetch it from its archive or regenerate it from a committed
  script, and record where it came from

## Commit Workflow
- Code in a submodule: commit in the submodule first, then bump the pointer here, then push
  the submodule before the parent
- `[AI-assisted]` prefix on AI-assisted commits
- Reference the tracking issue (`refs #N`, or `closes #N` when finishing the work is yours to
  declare)
- Ask the project lead before pushing to any remote

## Open Source
- Keep commit history clean and suitable for public visibility from the first commit
- Document design decisions in comments or `docs/`, not only in commit messages
- Apply the project's license consistently, with a `LICENSE` at the repository root
