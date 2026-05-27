# career-jd-analyzer · make sense of a job posting

[简体中文](README.md) · English

> **JDs are vague, long, and full of jargon. Understand it first, then decide whether to apply.**

Translates a job posting into plain language: what it really wants, whether you should apply, and it even sees through the "subtext".

## What it does for you

- Separates the hard gates (don't bother if you don't meet them) from the nice-to-haves
- Sees through recruiting jargon — e.g. "can handle high intensity" often means lots of overtime; "salary negotiable" often means a wide range
- Judges whether you should apply given your situation, what you're missing, and gives you questions to ask HR

## A quick example

Send it a link to a data-analysis internship → it tells you: the core asks are SQL and Excel, the hard gate is the degree; "fast-paced" in the JD may mean overtime — ask about workload in the interview.

## How to use

Install it:

```bash
npx skills add agentsope/career-skills/skills/career-jd-analyzer
```

Then just tell Claude, e.g.:

> Help me see what this role really wants and whether I can apply: (paste the posting link or text)

## Its bottom line

It only reads the real posting you give it; if you don't give one, it says so — it never makes up a JD from the job title to bluff you.

— part of the **career-skills** pack
