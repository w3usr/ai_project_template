---
paths:
  - "**/*.html"
  - "**/*.htm"
  - "**/*.css"
  - "**/*.scss"
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.php"
  - "**/*.twig"
  - "**/*.njk"
  - "**/*.liquid"
  - "**/_config.yml"
  - "**/package.json"
---

# Web Development Rules
*Delete this file if the project includes no web work.*

Covers the club website, event and outreach pages, dashboards, and any web front end.

## Content Accuracy
- **Never invent club facts.** Founding dates, officer names, meeting times, event
  attendance, award history, grant totals, and equipment lists are verified with the advisor
  or an officer before they are published. A plausible-sounding placeholder on a live page is
  worse than an obvious `{{TBD}}`.
- Callsigns are published with the member's knowledge. Personal contact details are not
  published at all; route inquiries to a club address.
- Photographs of identifiable people are published only with their permission. Photographs of
  minors at outreach events require the additional permission the event organizers collected.
- Content that speaks for the club or the University needs the advisor's sign-off before it
  goes live.

## University Identity
- The University of Scranton's name, seal, and logos are the University's marks. Follow
  University brand and web guidelines, and check with the advisor before using a University
  mark on a club page or in club material.
- Where club content is hosted on University infrastructure, University IT policy governs it.

## Accessibility
The site is a university club's public face; accessibility is a requirement, not a polish step.
- Every image carries meaningful `alt` text; decorative images carry `alt=""`
- Semantic HTML (headings in order, real `<button>` and `<a>` elements, labeled form fields)
- Text contrast meets WCAG AA; color is never the only way information is conveyed
- The page works by keyboard alone, and the focus outline stays visible
- Video and audio carry captions or a transcript

## Security and Secrets
- Never commit API keys, database credentials, SMTP passwords, CMS admin logins, or analytics
  tokens. Use environment variables and a gitignored `.env`.
- Never commit a database dump that contains member data.
- Keep dependencies current, and treat a published advisory in a dependency as work to do.
- Validate and escape anything a visitor submits. A club contact form is still a public input.

## Workflow
- If the site lives in its own repository as a submodule, commit inside the submodule first,
  then bump the pointer here, then push the submodule before the parent.
- Build a page locally and look at it before committing, including at phone width.
- Preserve the existing theme, template, and CSS conventions of the site being edited.
- Check that internal links resolve and that no `{{PLACEHOLDER}}` survives to production.
