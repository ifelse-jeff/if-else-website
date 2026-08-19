# If Else Data Solutions Website
# Master Project Context Document
# For Claude Code

Version: 1.0
Audience: Claude Code (VS Code) sessions, and any successor AI assistant
Prepared For: Ongoing website content, design, and code work
Last Updated: 2026-08-19

---

# PURPOSE OF THIS DOCUMENT

This document lets a new Claude Code session pick up work on the If Else
Data Solutions website immediately, without re-discovering project history
from scratch.

It contains:

- Project goals
- Infrastructure
- Completed work / current site state
- Known open issues
- Failed approaches (do not repeat)
- User preferences and working style
- Do's and Don'ts
- Best practices
- Reference data (IDs, keys, customer names, etc.)
- Recommended next steps
- A running session log (append-only, newest at the bottom)

This doc is the CLAUDE.md-style counterpart to a separate Claude Project
("If Else Data Website Design") used for content/strategy conversations.
This file is what Claude Code actually reads when working in the repo.
Keep the two in sync when something durable changes in either place.

**Two open items marked below need Jeff's confirmation/correction — see
"NEEDS CONFIRMATION" tags throughout.** Everything else is drawn directly
from the live site (fetched 2026-08-19) or the consolidated ChatGPT
migration record.

---

# INFRASTRUCTURE

Hosting: GitHub Pages (static hosting, no server-side runtime)
Domain: ifelsedata.com (custom domain via CNAME file in repo root)
Repo (local folder name seen in VS Code): IF-ELSE-WEBSITE — NEEDS CONFIRMATION
(exact GitHub repo owner/URL not yet confirmed in this doc)

Stack:

- HTML5, CSS3, vanilla JavaScript
- No framework (no React/Vue/Angular)
- No build process, no package manager, no bundler
- No CMS, no database, no backend application code

Known repo structure (from VS Code Explorer, 2026-08-19):

```
/
├── CNAME
├── index.html
├── README.md
├── images/
└── insights/
    ├── cloud-migration-pitfalls.html
    ├── data-quality-improvement.html
    ├── fractional-cio-growth.html
    ├── fractional-cio.html
    └── reporting-mistakes.html
```

Third-party services:

- **Formspree** — contact/consultation form processing (see Data &
  Reference Tables for form ID and CAPTCHA key)
- **Google reCAPTCHA** — spam protection on forms

Deployment: pushing to the repo's default branch redeploys automatically
via GitHub Pages. No manual deploy step.

---

# PROJECT OVERVIEW

**If Else Data Solutions** is a small technology consulting company. The
website presents it as a boutique consulting firm serving small and
midsize organizations with enterprise-level technology expertise, at
**ifelsedata.com**.

Mission statement (live on site): *"If Else Data Solutions untangles your
IT headaches so you can focus on running your business."*

Core headline (live on site, deliberately preserved since it was
accidentally lost and restored once already — see FAILED
APPROACHES / DO'S AND DON'TS): *"Empowering Small Businesses with
Enterprise-Grade Solutions"*

The company's earlier ChatGPT-era iterations of this site read too much
like an individual's résumé/portfolio rather than a company. That was
identified as the single biggest strategic problem in August 2026 (see
the consolidated migration record in the Claude Project). **As of this
document's writing, the live site has already moved substantially past
that problem** — see CURRENT SITE STATE below. Whoever did that work
(Jeff or an earlier Claude Code session) is not documented anywhere yet;
this doc starts the record going forward.

---

# PRIMARY OBJECTIVE

Continue building out If Else Data Solutions as a credible, company-first
consulting website, while:

- Preserving the simple static HTML/CSS/JS architecture (no framework,
  no build step) unless a real requirement changes that.
- Leading with business problems and outcomes, not technology inventories.
- Keeping the enterprise/corporate-blue visual identity: stable, trusted,
  precise, not trendy or startup-like.
- Treating technology names (SQL, Power BI, VMware, etc.) as supporting
  evidence, never the headline.

The user explicitly does NOT want:

- React, Vue, Angular, or any SPA framework
- A CMS or build pipeline
- The site to look/read like a résumé, personal portfolio, freelancer
  page, creative agency, or trendy startup landing page

---

# USER WORKING STYLE

**NEEDS CONFIRMATION — the following is inferred from this session's
conversation, not yet explicitly confirmed by Jeff for Claude Code work
specifically. Please correct anything wrong here.**

Inferred preferences:

- Prefers to go step by step, with confirmation before moving to the next
  piece, rather than large batches of changes at once.
- Is learning as they go (said explicitly) — prefer plain explanations of
  *why*, not just *what*, especially for anything non-obvious.
- Values a durable written record (this doc, plus the ChatGPT migration
  doc) over relying on conversation memory.
- Based on the phpRecipeBook project's established pattern (a different
  project, same user): likely prefers complete file replacements over
  line-level diffs when a file is being substantially changed, exact code
  over theoretical discussion, and a session log appended at the end of
  each work session.

When providing updates, until told otherwise, follow the phpRecipeBook
convention:

Preferred: "Replace this entire file"
Less preferred: "Modify line 234"

---

# CURRENT SITE STATE (verified via live fetch, 2026-08-19)

The live site at ifelsedata.com currently has:

## Header & Navigation

Logo: If Else Data Solutions logo
Primary nav: Services | Schedule | About | Insights | Contact
Contact methods in header: email (mailto link, see Data & Reference
Tables) and phone

## Hero Section

Headline: "Empowering Small Businesses with Enterprise-Grade Solutions"
CTA: "View Our Services" button

## Services Section — already reorganized around business outcomes

Three core service areas (this matches the company-first direction the
ChatGPT strategy doc called for — this work appears already done):

1. **Disconnected Systems** — integration of legacy platforms, cloud
   tools, siloed data. Example results: connected POS/billing/financial
   systems for a wholesale food distributor; built automated ETL
   pipelines for a publishing company.
2. **Slow Reporting or Manual Work** — automation/streamlined processes
   to reduce spreadsheet time. Examples: dashboards for
   publishing/food-distribution clients; cut reporting prep from hours to
   minutes.
3. **Outdated Infrastructure** — cloud migrations, hybrid environments,
   secure remote workforce support. Examples: POS system upgrade (50%
   transaction-time reduction); financial system migration with minimal
   downtime.

## About Us Section

Mission statement: "If Else Data Solutions untangles your IT headaches so
you can focus on running your business."

Common problems addressed (as listed on site):
- Security & downtime issues
- Cloud migration uncertainty
- Disconnected systems and duplicate data
- Time-consuming reporting processes
- Vendor accountability gaps

How they work (as listed on site):
- Flexible engagement models (advice, augmentation, or full delivery)
- Transparent communication on progress and risks
- Strong knowledge transfer and documentation

Core values (as listed on site):
- Clarity Over Complexity
- Results Over Hype
- Respect for Client Time
- Honesty in Every Engagement

## Client References / Logos

313 Alpha, Crain Communications, Shammami & Kasgorgis CPA PC, AdAge,
D&B Grocers Wholesale, Automotive News

Note: AdAge and Automotive News are new additions not present in the
ChatGPT-era migration record (which only listed the first four). Logo
usage permission should be confirmed for these two if not already done —
same caution the migration doc flagged for the original four.

## Insights Section — 5 articles currently live

1. "Why Fractional CIOs Are Critical for Growing Businesses"
2. "What Most Mid-Market Firms Get Wrong About Reporting"
3. "How a Fractional CIO Accelerates Business Growth"
4. "Migrating From On-Prem to Cloud: Avoid These 3 Pitfalls"
5. "Top 5 Ways to Improve Data Quality in Your Organization"

**Known open issue: #1 and #3 are still duplicative** (same underlying
topic — Fractional CIO — under two different titles). This was flagged in
the ChatGPT migration doc and has not been resolved. See KNOWN OPEN
ISSUES below.

## Forms

**Consultation Request Form:**
- Fields: Name, Email, Category dropdown (9 options incl. IT Strategy,
  Data Integration, Reporting, etc.), Message
- Confirmation message: "Thank you! Your request has been submitted."

**Contact Form:**
- Fields: Name, Email, "What's top of mind" text area, Urgency selector
- Confirmation message: "Thanks! We'll review and get back to you with a
  clear next step."

## Footer

Contact: email + phone
Copyright: © 2026 If Else Data Solutions. All rights reserved. — now rendered
dynamically via `<span id="copyright-year">` + a one-line script
(`new Date().getFullYear()`) on every page, so this never needs a manual
bump again. Fixed 2026-08-19 — see SESSION LOG.

---

# KNOWN OPEN ISSUES

1. **Duplicate Fractional CIO Insights articles.** "Why Fractional CIOs
   Are Critical for Growing Businesses" and "How a Fractional CIO
   Accelerates Business Growth" cover essentially the same ground. Either
   consolidate into one article, or clearly differentiate their angles
   (e.g., one explains *what* a Fractional CIO is, the other explains
   *when/why* a growing company needs one).
2. **Customer logo permissions.** AdAge and Automotive News were added to
   the client-logo strip at some point after the ChatGPT-era record was
   written. Confirm public-display permission exists for these, same as
   the original four (313 Alpha, Crain Communications, Shammami &
   Kasgorgis CPA PC, D&B Grocers Wholesale).
3. ~~Footer copyright year shows 2025.~~ **RESOLVED 2026-08-19** — now
   dynamic on every page (index + all 5 Insights articles). See SESSION
   LOG.
3b. **Insights article template inconsistency (found 2026-08-19, not yet
   fixed).** While fixing the footer issue above, found that the 5
   Insights articles were each authored independently and use 4 different
   HTML/CSS templates: different fonts/spacing/color rules, some wrapped
   in a `.post`/`header` card layout and some not, and inconsistent
   "Back to Insights" link targets (`/#insights` root-relative on some,
   `../index.html#insights` relative on others). All 5 now at least share
   a consistent footer, but the rest of the template is not unified. This
   is a design/content decision (pick one template, migrate all 5) rather
   than a mechanical fix, so it's logged here rather than corrected
   automatically — flag for a future session alongside or after the
   duplicate-Fractional-CIO-articles decision.
4. **Logo/brand mark.** Per Jeff (2026-08-19 conversation): "resolved for
   now." No further action needed unless he raises it again. (Prior
   ChatGPT-era attempts all failed — see FAILED APPROACHES below, kept
   for historical context only.)
5. **SEO fundamentals** not yet confirmed as done: unique page titles,
   meta descriptions, Open Graph metadata, social cards, structured data,
   sitemap.xml, robots.txt, favicon review, Search Console verification.
6. **Accessibility audit** not yet confirmed as done: heading hierarchy,
   semantic navigation, form labels, keyboard nav, focus states, color
   contrast, alt text, mobile touch targets, CAPTCHA accessibility.
7. **Analytics** not yet confirmed as installed: Google Analytics, Search
   Console, Microsoft Clarity, or equivalent. Do not assume any of these
   are present without checking the actual page source.
8. **Performance audit** not yet confirmed as done: Lighthouse pass,
   image optimization, lazy loading where useful.

---

# FAILED APPROACHES — DO NOT REPEAT

(Historical record from the ChatGPT era. Jeff has indicated the logo is
"resolved for now" as of 2026-08-19, so this is background only — but if
logo work comes up again, do not blindly repeat these.)

## Logo generation — repeatedly failed to follow explicit composition instructions

Requirements that were given repeatedly and still not satisfied across
many iterations: icon on the left (blue, minimalist), "If Else" beside it
aligned top, "Data Solutions" on one line beneath "If Else," dark/black
text, transparent background, SVG export.

What went wrong, repeatedly:
- Icon did not match the user-supplied reference image.
- "Data Solutions" placement kept coming out wrong.
- New generations often looked like previously-rejected versions ("same
  logo regenerated").
- SVG file delivery failed multiple times (expired sessions, file-not-found
  errors) even when the design itself might have been acceptable.

Lesson: if logo work resumes, treat any composition requirement as a hard
constraint, not inspiration. Verify any generated file actually exists and
opens before telling the user it's ready.

## Headline accidentally removed during a CSS/layout revision

The homepage headline ("Empowering Small Businesses with
Enterprise-Grade Solutions") was lost during an earlier layout change and
had to be restored after the user caught it during a full-page review.

Lesson: after any structural/CSS change, verify important copy is still
present, not just that the layout looks fine.

---

# DO'S AND DON'TS

**DON'T**

- Don't make the site read like a personal résumé, freelancer profile, or
  portfolio. (This was the central strategic problem identified in the
  ChatGPT era — the current live site appears to have already addressed
  it; don't regress.)
- Don't use the owner's personal name as the site's identity. Present "If
  Else Data Solutions" as the business.
- Don't center content around lists of technologies/certifications/
  platforms without business context.
- Don't introduce a JS framework, CMS, or build tooling without a
  concrete, agreed-upon reason.
- Don't rewrite large working portions of the site when a smaller
  targeted change accomplishes the goal.
- Don't change the header/nav without checking mobile layout afterward.
- Don't change contact-form markup/JS without doing a real Formspree
  submission test afterward.
- Don't accidentally remove the headline "Empowering Small Businesses
  with Enterprise-Grade Solutions."
- Don't assume any previously-generated logo asset is approved.
- Don't guess at isolated CSS changes without checking the full page for
  side effects, when the full file is available.
- Don't add flashy animation, excessive gradients, or trendy visual
  effects — this should read as enterprise/corporate, not startup.

**DO**

- Do present If Else Data Solutions as a boutique technology consulting
  firm and long-term technology partner.
- Do lead with business problems and outcomes (the current three-card
  services section is a good model — keep this pattern).
- Do keep technology names as supporting evidence, not the headline.
- Do preserve the simple static HTML/CSS/JS architecture.
- Do keep HTML/CSS readable and manually editable.
- Do use minimal JavaScript.
- Do preserve the corporate/enterprise visual aesthetic (clean spacing,
  restrained styling, corporate blue).
- Do maintain responsive/mobile-friendly behavior, with comfortably-sized
  touch targets.
- Do preserve and test the working Formspree + CAPTCHA setup after any
  related change.
- Do use recognizable customer names/logos as credibility signals where
  permission exists.
- Do update Insights with original, business-problem-first content (the
  reporting-mistakes article was identified as the strongest example of
  this pattern in the ChatGPT era — use it as a model).

---

# BEST PRACTICES

**Messaging pattern.** For any new page or section, answer in order: (1)
what business problem does the visitor have, (2) what outcome do they
need, (3) how does If Else Data Solutions get them there, (4) why should
they trust the company, (5) what should they do next.

**Tone.** Professional, experienced, practical, direct, honest, confident
without arrogance, business-focused. Avoid buzzwords, empty superlatives
("world-class," "revolutionary"), dense jargon, self-congratulatory
language.

**Design.** Stability, trust, precision, simplicity, enterprise competence
without corporate heaviness. Should not resemble a SaaS startup, trendy
design studio, or personal developer portfolio.

**Forms.** Formspree is a working dependency — don't replace casually.
After changing form attributes, field names, CAPTCHA markup, or
submission JS: perform a real submission and verify both the email
receipt and the visitor-facing success experience.

**Responsive behavior.** Mobile is not an afterthought. Test any
navigation/header change at narrow widths. Navigation links need enough
padding to be comfortably tappable.

---

# DATA & REFERENCE TABLES

## Core site info

| Item | Value |
| --- | --- |
| Company | If Else Data Solutions |
| Website | ifelsedata.com |
| Hosting | GitHub Pages |
| Front end | HTML5, CSS3, vanilla JavaScript |
| Framework | None |
| Primary headline | "Empowering Small Businesses with Enterprise-Grade Solutions" |
| Mission statement | "If Else Data Solutions untangles your IT headaches so you can focus on running your business." |
| Primary CTA (hero) | "View Our Services" |
| Contact email (mailto, from hero button) | jeff@ifelsedata.com |
| Phone number shown on site | 313.555.6667 — NEEDS CONFIRMATION (this has the look of a placeholder number; please confirm it's real before treating it as ground truth) |
| Formspree Form ID | `xkgbpqgk` |
| CAPTCHA site key | `6LfcjW0rAAAAANnzxgImFynapjbHcubdXE_Rh-gE` |

## Current client references

- 313 Alpha
- Crain Communications
- Shammami & Kasgorgis CPA PC
- AdAge
- D&B Grocers Wholesale
- Automotive News

## Current core values (as displayed)

- Clarity Over Complexity
- Results Over Hype
- Respect for Client Time
- Honesty in Every Engagement

## Current Insights articles (live)

1. Why Fractional CIOs Are Critical for Growing Businesses
2. What Most Mid-Market Firms Get Wrong About Reporting
3. How a Fractional CIO Accelerates Business Growth
4. Migrating From On-Prem to Cloud: Avoid These 3 Pitfalls
5. Top 5 Ways to Improve Data Quality in Your Organization

---

# RECOMMENDED NEXT STEPS

1. ~~Update or dynamically generate the footer copyright year.~~ DONE
   2026-08-19.
2. Confirm the phone number displayed is real, not a placeholder.
3. Confirm whether analytics is installed; add if desired.
4. Confirm logo-usage permission for AdAge and Automotive News.
5. Do an SEO pass (titles, meta descriptions, Open Graph, sitemap.xml,
   robots.txt, Search Console).
6. Do an accessibility pass (headings, labels, contrast, keyboard nav,
   focus states).
7. Do a performance pass (image optimization, lazy loading).
8. Resolve the duplicate Fractional CIO Insights articles (consolidate or
   differentiate).
9. Decide on and migrate to one consistent Insights article template
   (see KNOWN OPEN ISSUES item 3b).
10. Confirm this doc's INFRASTRUCTURE and USER WORKING STYLE sections
    (marked NEEDS CONFIRMATION above) and correct anything wrong.

---

# HOW TO UPDATE THIS DOCUMENT

At the end of any Claude Code session that makes meaningful changes to
this site, append a new dated entry under SESSION LOG below, following
this shape (matching the pattern established on the phpRecipeBook
project):

```
# SESSION LOG — YYYY-MM-DD

## Summary
One or two sentences on what this session accomplished.

## What Was Done
Per-change detail: file(s) touched, root cause if fixing a bug, the fix
itself, and anything explicitly NOT done / left for later.

## Files Modified
List of files.

## Current State After This Session
Short status update — what works now, what's still open.
```

Keep entries append-only (newest at the bottom, like a changelog) so the
full history stays intact. Update the "Last Updated" date at the top of
this document, and update KNOWN OPEN ISSUES / RECOMMENDED NEXT STEPS if
this session closed or opened any.

---

# SESSION LOG

(No Claude Code sessions logged yet as of 2026-08-19. This document was
created in a Cowork/Claude session on that date, based on the consolidated
ChatGPT migration record and a live fetch of ifelsedata.com. The first
Claude Code session to make changes to this repo should add the first
entry below.)

---

# SESSION LOG — 2026-08-19

## Summary
First Claude Code session against this repo. Read this context doc in
full, reviewed the three NEEDS CONFIRMATION items with Jeff (answers
still pending — see below), agreed a step-by-step order for KNOWN OPEN
ISSUES / RECOMMENDED NEXT STEPS starting with lowest-risk items, and
fixed the footer copyright year across the whole site — including a
related issue found along the way (4 of 5 Insights articles had no
footer at all).

## What Was Done
- **Footer copyright year (KNOWN OPEN ISSUES #3):** Was hardcoded "2025"
  on the 2 pages that had a footer (`index.html`,
  `insights/fractional-cio.html`). Updated to 2026, then converted to a
  dynamic `<span id="copyright-year">` populated by
  `new Date().getFullYear()` on every page, so it will never need a
  manual bump again.
- **Missing footers on 4 Insights articles (found this session, not
  previously documented):** `cloud-migration-pitfalls.html`,
  `data-quality-improvement.html`, `fractional-cio-growth.html`, and
  `reporting-mistakes.html` had no `<footer>` element at all. Added a
  footer CSS rule (matching the existing style used on
  `fractional-cio.html`) and the same dynamic-year footer markup/script
  to all 4, so every page on the site now shows a consistent copyright
  line.
- **NOT done / left for later:** Did not unify the rest of the Insights
  article templates. Each of the 5 was authored independently with
  different fonts/spacing, some with a card-style wrapper and some
  without, and inconsistent "Back to Insights" link targets
  (`/#insights` vs `../index.html#insights`). Logged as new KNOWN OPEN
  ISSUES item 3b — flagged as a design/content decision for a future
  session, not corrected automatically, consistent with the "smallest
  changes first, content/design decisions last" ordering agreed at the
  start of this session.
- Reviewed NEEDS CONFIRMATION items with Jeff (repo identity, user
  working-style inference, phone number). Answers not yet received as of
  this log entry — still open, see RECOMMENDED NEXT STEPS.
- Agreed a working order for the remaining open issues (see
  RECOMMENDED NEXT STEPS, renumbered this session): phone number
  confirmation and analytics check next, then logo permissions, then
  SEO/accessibility/performance passes, then the two content/design
  decisions (duplicate Fractional CIO articles; Insights template
  consolidation) last.

## Files Modified
- `index.html`
- `insights/fractional-cio.html`
- `insights/cloud-migration-pitfalls.html`
- `insights/data-quality-improvement.html`
- `insights/fractional-cio-growth.html`
- `insights/reporting-mistakes.html`
- `docs/If_Else_Data_Solutions_Context.md` (this file)

## Environment note
The Edit tool and Bash's `sed` both failed with `ENOENT` trying to write
temp files directly inside the site root (`index.html`,
`insights/*.html`) — worked fine on `docs/` files. Likely OneDrive
Files-On-Demand/sync interference on that specific folder. Worked around
it by reading/writing files directly via PowerShell + .NET
(`System.IO.File]::ReadAllText/WriteAllText` with a no-BOM UTF8
encoding, verifying single-match-only before each replace). If this
recurs, that's the fallback — plain `Edit`/`sed` are not reliable in
`index.html`/`insights/` right now.

## Current State After This Session
Every page on the site (`index.html` + all 5 Insights articles) now
shows a self-updating copyright year in a consistent footer. Insights
template consistency, the duplicate Fractional CIO articles, and the
three NEEDS CONFIRMATION items remain open for the next session.