---
name: resume-critique
description: >-
  Critique resumes for software architect, staff, principal, and lead
  engineering roles. Use only when the user explicitly asks to use the
  resume-critique skill by name for resume feedback, review, bullet rewrites,
  or tailoring to a job posting.
---

# Resume Critique

## When To Use

Use this skill only when the user explicitly asks to use `resume-critique` by
name.

Examples that should use this skill:

- "Use the resume-critique skill on my resume."
- "Run `resume-critique` against this job posting and resume."

Examples that should not automatically use this skill:

- "Critique my resume."
- "Review this resume for architect roles."
- "Help me rewrite these bullets."

Do not apply this skill proactively just because a resume file, PDF, or job
posting is present in the workspace or current context.

## Inputs

Collect as much of this as the user can provide:

- Resume text, source file, or PDF
- Target job posting or target role
- Preferred title, if the user has one
- Constraints such as page length, industry, or location

If no job posting is provided, critique against a generic
Senior/Principal/Software Architect bar.

## Critique Standard

Be harsh, specific, and useful. Optimize for interview conversion, not
politeness.

Judge whether the resume reads like someone who:

- sets technical direction
- designs systems and platforms
- makes trade-offs across scale, reliability, cost, and delivery
- influences other engineers and stakeholders
- delivers measurable business impact

## Review Areas

Evaluate all of the following:

1. Title and executive summary fit
2. Architectural leadership signals
3. System design, scale, reliability, security, and migration evidence
4. Cloud, platform, and infrastructure credibility
5. Business impact and metrics
6. ATS keyword coverage for the target role
7. Weak, vague, repetitive, or low-signal bullets
8. Missing evidence that could make a hiring manager reject the resume

## Output Format

Use this structure:

### Overall Verdict

- State whether the resume is strong, borderline, or mispositioned for the
  target role.
- Give a short explanation of the main reason.

### Biggest Problems

- List the highest-impact issues first.
- Focus on why each issue hurts this specific type of role.

### Detailed Critique

Cover:

- title and summary
- architecture and technical leadership signals
- experience bullets
- scale, reliability, and platform depth
- business impact and metrics
- ATS and keyword alignment

### Rewrite Recommendations

Rewrite the weakest parts, typically:

- the title if it weakens positioning
- the summary if it is generic or low-signal
- 3 to 6 weak bullets

Rules for rewrites:

- preserve the user's facts
- do not invent achievements or metrics
- if a metric is missing but would help, add a bracketed placeholder

### Rejection Risks

State what a hiring manager might conclude negatively after reading the resume.

### Missing Information

Call out missing facts that would materially improve the resume if added.

## Writing Rules

- Prefer direct language over praise
- Point to exact bullets or sections when possible
- Explain what is weak, not just that it is weak
- Prefer concrete rewrites over generic advice
- Penalize resumes that read like pure feature delivery when the target role is
  architect-track
- Reward evidence of technical direction, cross-team influence, standards,
  platform work, trade-offs, mentoring, and measurable outcomes

## Tailoring To A Job Posting

If a job posting is provided:

- calibrate the critique to that exact role
- mirror the posting's terminology when truthful
- identify missing or weak keywords
- explain which gaps are most likely to block an interview
- suggest a stronger honest title if the current one undercuts fit

## Default Prompt Behavior

When applying this skill, follow this instruction set:

> Critique this resume for a Senior, Principal, or Software Architect role. Be
> harsh and specific. Evaluate executive summary and title fit, architectural
> leadership signals, system design and scale evidence, cloud and platform
> credibility, business impact and metrics, ATS keyword coverage, weak or vague
> bullets, and what would make a hiring manager reject it. Then rewrite the
> weakest sections and suggest a stronger title or summary if needed.
