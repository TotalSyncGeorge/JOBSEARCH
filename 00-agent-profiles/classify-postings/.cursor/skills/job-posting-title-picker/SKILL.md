---
name: job-posting-title-picker
description: >-
  Choose the best resume job title for a target role by classifying a job
  description as architect-track or lead-IC-track. Use when the user shares a
  job posting, asks which title to use, or asks to tailor the resume for a
  specific role.
---

# Resume Title Picker

## Context

The user held a sole-software-person role at a small startup. Two honest titles
are available depending on the target role:

| Title                      | Best for                                        |
|----------------------------|-------------------------------------------------|
| **Software Architect**     | Architect, staff, principal, or director roles   |
| **Lead Software Engineer** | Senior or lead individual-contributor roles      |

## Decision Algorithm

Scan the job description for signal words. Classify, then recommend.

### Step 1 — Collect signals

**Architect signals** (design & influence):
- "design systems," "define architecture," "technical vision/strategy"
- "cross-team," "influence," "stakeholders," "alignment"
- "trade-offs," "scalability," "technical decisions"
- "mentor," "guide," "set standards"
- Less emphasis on sprint work, PRs, or shipping features directly

**Lead/Senior IC signals** (build & ship):
- "build," "implement," "ship," "deliver"
- "own a component/service/feature end-to-end"
- "code reviews," "pull requests," "hands-on"
- "collaborate with your team," "agile/scrum"
- Specific tech-stack requirements with depth expectations

### Step 2 — Apply the one-line test

> Does the job description spend more words on **what you'll decide** or
> **what you'll build**?
>
> - Decide → **Software Architect**
> - Build  → **Lead Software Engineer**

### Step 3 — Break ties

When the signal is mixed, use these tiebreakers in order:

1. **Posted title / level** — If the posting says "Staff," "Principal," or
   "Architect," recommend Software Architect. If it says "Senior," "Lead," or
   "Engineer," recommend Lead Software Engineer.
2. **Team size** — Large team or multiple teams → Architect. Small team or
   "small, scrappy" → Lead.

### Step 4 — Output

State the recommended title and a one-sentence justification citing the
strongest signals found. Example:

> **Recommend: Software Architect** — the posting emphasizes "define technical
> direction across teams" and "drive architectural decisions," with no mention
> of sprint-level delivery.
