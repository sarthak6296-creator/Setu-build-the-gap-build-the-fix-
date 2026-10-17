# OpportunityKit

**Turn requirements into a checklist, then see how a student profile measures up.**

Built for SETU 2026 (Forge Realm), Problem Statement PS-03.
Team: **Ai coder** | Sarthak Anil Jadhav

- Live demo: `PASTE-YOUR-VERCEL-LINK-HERE`
- Demo video: `PASTE-YOUR-VIDEO-LINK-HERE`

## The problem
Internships, scholarships and competitions list requirements in different places and formats. Students struggle to know if they qualify and what to prepare.

## What it does
1. **Organize** - paste an opportunity's text. Visible rules detect year, branch, CGPA or marks, skills, documents, portfolio link, weeks, income limit, team size and deadline, and highlight them in the pasted text. Every field is editable.
2. **Compare** - each requirement is checked against the student profile.
3. **Explain** - every item gets a status (MATCH, MISMATCH or MISSING INFO), a short reason and a fix. A summary shows a readiness bar and ordered next steps.

3a. **Interactive flow** - 3 steps (Opportunity, Profile, Result). The profile uses tap and slide controls: year and branch buttons, a CGPA slider, skill tags with one-tap suggestions from the requirements, document cards (unknown, ready, not ready) and weeks shortcuts. A live meter at the bottom updates the result as you change anything.
3b. **What-if simulator and fix plan** - tick "What if I fix this?" on any gap and the readiness ring and verdict update live. The fix plan lists next steps quickest first, with an effort label for each.
4. **Compare** - add up to 3 results and see them ranked (fewest mismatches first, then fewest missing details). A **Copy summary** button copies the result as text.

Unknown is not a fail: if the profile has no answer, the item is MISSING INFO and the app asks for it.

## Example (from the problem statement)
Internship asks: 2nd or 3rd year, CGPA 7.5+, HTML + CSS + JavaScript, resume, portfolio/GitHub link, 8 weeks.
Profile: 2nd year CSE, CGPA 8.2, HTML + CSS + Python, resume ready, link and availability not provided.

Result: **3 matches, 1 mismatch, 2 missing details. Not ready to apply yet.**
Click **Try the example** on the page to see it.

## Rules used
| Requirement | Rule |
|---|---|
| Year | profile year within the allowed range |
| Branch | profile branch is in the accepted list |
| CGPA / Marks | profile value is at or above the cut-off |
| Skills | every required skill is listed (JS = JavaScript, etc.) |
| Documents | marked Ready (Not ready = mismatch, not answered = missing) |
| Portfolio / GitHub | a valid-looking link is provided |
| Availability | weeks available is at least the weeks needed |
| Family income | at or below the limit |
| Team size | within the allowed range |
| Deadline | not passed (warns when 7 days or less remain) |

A blank profile answer is always MISSING INFO.

## Monetization
- **Free plan** for students: unlimited checks.
- **Student Plus** (paid extras): deadline reminders, saved profiles and history, curated opportunity lists.
- **College license** for placement cells: batch readiness dashboard, common gaps, custom checklists.
- Running cost is very low: rules run in the browser, no server and no AI calls.
- Pilot prices (Rs 99 per student per year for colleges, Rs 49 per month for Student Plus) are assumptions to test.

## Tech
Plain HTML, CSS and JavaScript in a single file. No backend, no API keys, no build step. The profile is saved only in the browser (localStorage).

## Run locally
Open `index.html` in any browser. No install needed.

## Deploy
Import this repo in Vercel (Framework Preset: Other, no build command). See `docs/` for the Round 2 submission notes.
