# Amateur Radio Operating Rules

**This file applies to every project in this repository.** It has no `paths:` scope because
the license obligations it describes do not depend on which file you have open.

W3USR is a licensed amateur station. The rules below come from the FCC, not from the club, and
the club cannot waive them.

## The One Rule That Governs All the Others

**A licensed human control operator is responsible for every transmission.** An amateur
station may transmit only when a control operator is designated and present at a control
point (47 CFR 97.7, 97.103, 97.105). AI tools hold no license, no privileges, and no
responsibility. They assist with writing, analysis, code, and design. They do not operate the
station.

In practice, for this repository:

- AI may draft a net script, a contest strategy, a message template, a beacon text, or a
  digital-mode payload. A control operator reads it, approves it, and sends it.
- AI may write software that formats, queues, or decodes transmissions. A control operator
  supervises the station while that software runs, under a control method Part 97 permits.
- AI output goes on the air only after a licensed human has read it.

Do not build anything that transmits on its own schedule without first working out, with the
trustee or advisor, which control method under 97.109 applies and who the responsible station
licensee is.

## Rules That Come Up in Club Projects

Cited to 47 CFR Part 97. The regulation is the authority; confirm the current text at
[ecfr.gov](https://www.ecfr.gov/current/title-47/chapter-I/subchapter-D/part-97) before
relying on a summary here, including this one.

| Topic | Section | What it means for us |
|---|---|---|
| Control operator required | 97.7, 97.103, 97.105 | Someone licensed is responsible, always. The station licensee is responsible even when another member is the control operator. |
| Station control methods | 97.109 | Local, remote, and automatic control each carry conditions. Remote control (telecommand) adds 97.213; automatically controlled digital stations add 97.221. Pick the method deliberately and document it. |
| Station identification | 97.119 | Identify with the callsign at least every 10 minutes during a communication and at the end of it. Any software that transmits must handle this. |
| No obscured messages | 97.113(a)(4) | Never write code, or ask AI to write code, that encodes transmitted messages to hide their meaning. Standard published digital modes and open protocols are fine; encryption for privacy is not. Authentication of a control link is a separate matter; ask before building one. |
| No broadcasting | 97.113(b) | One-way transmissions to the general public are prohibited, with narrow exceptions. A "club radio station" that streams programming is not one of them. |
| No communications for pay or pecuniary interest | 97.113(a)(2), 97.113(a)(3) | The club may not use the station on behalf of a business, and members may not be paid to operate. Publicizing a club fundraiser on the air needs a check with the advisor first. |
| Third-party communications | 97.115 | An unlicensed visitor may speak through the station while the control operator is present and at the control point. This is the rule that makes demo days legal; read it before running one. |
| RF exposure | 97.13(c) | Antenna and amplifier projects require an RF exposure evaluation. Do this before the antenna goes up, and record the result in the repository. |

## Logging and Operating Integrity

Log data is a record of what actually happened on the air. Treat it like data.

- **Never fabricate a QSO, a log entry, a contest score, a QSL, or an award credit**, and
  never let AI generate one. Synthetic records for testing are fine when they live in a file
  named for what they are (`test_fixtures/`, `sample_log.adi`) and can never be uploaded.
- **Never upload a synthetic or AI-generated log** to LoTW, eQSL, Club Log, a contest sponsor,
  POTA, SOTA, or any other aggregator. Uploads are one-way and hard to retract.
- Before writing anything that touches a real log file, make a copy. Work on the copy.
- Contest, POTA, SOTA, and award programs have their own rules. They are the authority for
  their own events, and AI is a poor source for what they currently say. Check the sponsor's
  published rules.
- When AI assists with log analysis or a score claim, say so in `ai/ai_usage_log.md` and have
  a licensed member verify the numbers before submission.

## Using the Club Callsign

- W3USR transmits under the authority of its license trustee. Get the trustee's authorization
  before operating under the club call, before entering a contest as W3USR, and before
  publishing anything on the air or online as an official club activity.
- Personal callsigns are used for personal operating. Do not log personal contacts under the
  club call.
- Club social media, QRZ, and website content that speaks for W3USR needs the advisor's or
  trustee's sign-off, whether or not AI helped write it.

## Station and Equipment Safety

- Antenna work, tower work, and rooftop access happen with the advisor's knowledge and with
  another person present. AI cannot assess a site.
- Do not publish building access procedures, alarm codes, rooftop routes, or remote-station
  credentials in this repository at any visibility level.
- Treat AI guidance on RF exposure, grounding, lightning protection, electrical work, and
  tower rigging as a starting point for research, and confirm it against ARRL publications,
  manufacturer documentation, the National Electrical Code, and a person who has done the job.

## Where to Take a Question

If a project raises a licensing or operating question this file does not answer, stop and ask
the trustee or the faculty advisor before proceeding. "The AI said it was fine" is not a
defense to the FCC, and it is not how this club operates.
