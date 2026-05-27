# role-matching.md — JD Alignment Reference
# Skill: career-experience-mapper · Step 3: Role Alignment（对齐岗位）
# Purpose: Executable rules for deciding how to foreground, reframe, downplay, or cut each experience entry against a target JD.
# Red line: All rules operate on facts already present in the experience. Never add skills, tools, or outcomes the candidate did not have. See → no-fabrication.md
# Language convention: Chinese reasoning, English output; NACE 8 competency vocabulary preferred.

---

## 1. Relevance Triage — Three-Tier Classification

### Tier Definitions

**FOREGROUND（强相关 · 前置完整展开）**
Criteria — must satisfy ≥ 2 of 4:
- Core tools / skills from this experience appear ≥ 2 times in JD Required section
- At least 1 bullet with quantified outcome (number / % / scale) can be written truthfully
- Primary job duties map directly to this experience's main activities (same verb category: analyze / develop / manage / coordinate)
- Industry or domain overlaps substantially with target role

Action: Place in Experience section first; first bullet must hit JD's highest-frequency required keyword.

**REFRAME（弱相关 · 侧写保留部分子弹）**
Criteria — any of:
- Only a subset of dimensions (partial tools, transferable soft skills) intersect with JD
- Experience is from a different industry but contains transferable competencies
- Outcomes are quantifiable but need re-framing in target-role language

Action: Extract only the dimensions that truly exist AND intersect with JD keywords. Rewrite with JD vocabulary as primary lens. Do not write bullets about dimensions that did not exist.

**DOWNPLAY（弱/无关 · 缩减为一行，移入次级区）**
Criteria — all of:
- No direct keyword intersection with JD
- Deleting would create a gap > 6 months OR the entry demonstrates career continuity

Action: One-line entry, no bullets, move to "Other Experience" or bottom of resume. Format: `[Title], [Organization], [Date Range]`

**CUT（无关 · 从本版本删除）**
Criteria — all of:
- No keyword intersection
- No gap risk (other entries cover the timeline)
- Resume already has ≥ 4 strongly relevant entries

Action: Remove from this JD-specific version. Retain in master resume bank.

### Gap Exception Rule（时间空白例外）
If cutting or downplaying an entry creates > 6 months of unexplained resume gap → override CUT to DOWNPLAY. Retain as one-line entry. Reason: unexplained gaps are a common human-reviewer filter trigger, independent of ATS logic.

### Enhancv 2/4 Retention Threshold
Before assigning REFRAME vs. DOWNPLAY/CUT, apply this checklist. If ≥ 2 answers are YES → retain (FOREGROUND or REFRAME):

| # | Question | Y / N |
|---|----------|-------|
| 1 | Does this experience demonstrate a skill the target role requires? | |
| 2 | Can I write at least one bullet with a quantified outcome (not just duties)? | |
| 3 | Does including this entry fill a meaningful time gap? | |
| 4 | Can this experience be linked to the target role without distorting facts? | |

Score < 2 YES → DOWNPLAY or CUT.

---

## 2. JD Keyword Extraction — Frequency × Position Matrix

### Step 1: Extract and Weight Keywords

| JD Location | Priority Weight |
|-------------|----------------|
| Job title / role name | Highest |
| First 50% of Requirements section | High |
| First 3 bullets of Responsibilities | High |
| Any term appearing ≥ 3 times across sections | Must-have keyword |
| Preferred / Nice-to-have section | Bonus keyword |
| Appears once in lower half of JD | Low priority |

Rule: A keyword appearing in ≥ 3 separate JD sections → treat as core required. A keyword appearing only once under "Preferred" → treat as bonus, not blocking.

### Step 2: Bucket into Three Categories

| Bucket | Examples | ATS Weight |
|--------|----------|-----------|
| Hard skills（硬技能）: tools, languages, certifications | Python, SQL, Figma, AWS, CPA, React.js | Highest — ATS hard filter |
| Methodology / process（方法论）| Agile, A/B testing, data pipeline, GAAP, Scrum | High |
| Soft skills（软技能）| communication, leadership, collaboration | Low in ATS; embed in bullets, do not list standalone |

### Step 3: Exact Terminology Matching（精确匹配）
Use the JD's exact phrasing — do not substitute synonyms:
- JD says "React.js" → write "React.js", not "ReactJS" or "React"
- JD says "machine learning" → write "machine learning", not "ML" (unless JD uses both)
- JD says "cross-functional collaboration" → mirror that phrase in at least one bullet

### Step 4: Qualification Threshold Check
Calculate coverage of Required keywords only:
- ≥ 80% coverage → proceed with tailoring
- 60–79% coverage → proceed, note gaps to user, suggest supplementary project framing
- < 60% coverage → flag to user: "Match rate insufficient. Consider adding a relevant project or selecting a better-fit role."

---

## 3. Natural Embedding vs. Keyword Stuffing

### Natural Embedding Rules（自然嵌入规则）
- Each core required keyword appears 2–3 times across the resume, distributed across sections:
  - Summary: 1 occurrence
  - Experience bullets: 1–2 occurrences
  - Skills section: 1 occurrence (hard skills only)
- No single paragraph contains the same keyword more than 2 times.
- Soft skills are never listed standalone in Skills section; embed in experience bullets.

### Sentence Template（句法模板）
```
[Action Verb] + [Keyword / Tool] + [Context / Scope] + [Quantified Result]
```
Examples:
- "Built an end-to-end data pipeline using Python and Airflow, reducing ETL runtime by 40%."
- "Conducted A/B testing on three UX variants using Optimizely, increasing conversion rate by 18%."
- "Coordinated cross-functional sprint planning across 4 teams using Jira, maintaining 95% on-time delivery over 6 months."

### Keyword Stuffing — Prohibited Patterns
- Listing keywords as comma-separated strings with no action verb or result.
- Repeating the same keyword 3+ times within one bullet or paragraph.
- Pasting JD sentences verbatim into the resume.
- Creating a hidden white-text keyword block (detectable and penalized).

Modern ATS semantic analysis can detect abnormal keyword density and reduce score. Human reviewers will reject stuffed resumes immediately.

---

## 4. Foreground / Reframe / Downplay / Cut Decision Checklist

```
INPUT: experience entry E, target JD

─── FOREGROUND ───────────────────────────────────────────────
  □ E's core tools/skills match ≥ 2 Required JD keywords
  □ E has at least 1 quantifiable outcome (truthful)
  □ E is recent (within 3 years) OR directly relevant regardless of date
  → Place first in Experience section
  → First bullet hits JD's top-priority required keyword
  → Reorder remaining bullets to mirror JD Responsibilities sequence

─── REFRAME ──────────────────────────────────────────────────
  □ E matches 1 Required JD keyword (partial intersection)
  □ E has transferable dimensions (coordinate / analyze / present / manage)
     that truly existed in this experience
  □ 2/4 threshold score ≥ 2
  → Extract only the intersecting dimensions
  → Rewrite first bullet using JD's vocabulary as primary lens
  → Omit dimensions that do not intersect (do not invent new ones)
  → Retain in main Experience section OR move after stronger entries

─── DOWNPLAY ─────────────────────────────────────────────────
  □ E has no direct keyword intersection
  □ Removing E creates gap > 6 months OR breaks continuity
  → One-line format, no bullets: [Title], [Organization], [Date Range]
  → Move to "Other Experience" section or resume bottom
  → Do not reference in Summary

─── CUT ──────────────────────────────────────────────────────
  □ E completely irrelevant to this JD
  □ No gap risk after removal
  □ Resume has ≥ 4 strongly relevant entries (space is saturated)
  → Delete from this JD-specific version
  → Keep in master resume bank for future versions
```

---

## 5. Same Experience, Multiple JD Profiles — Example Table

**Source experience (master draft):**
Student entrepreneurship project · Finance Team Lead · 6 months
- Built cost forecasting model in Excel covering 3 financing scenarios
- Coordinated resource allocation with marketing and product teams; joined 6 weekly cross-team meetings
- Presented monthly financial reports to 12 advisors

| Target Role | Tier | First Bullet（侧写首条子弹） | Omitted / Not Mentioned |
|-------------|------|---------------------------|------------------------|
| Data Analyst | FOREGROUND | "Built a 3-scenario cost forecasting model in Excel, projecting 6-month burn rate with < 10% deviation." | Cross-team coordination (secondary signal) |
| Business Analyst | FOREGROUND / REFRAME | "Delivered monthly financial reports to a 12-person advisory board, synthesizing cost variance data into actionable recommendations." | Financing scenario technical details (too domain-specific) |
| Project Manager | REFRAME | "Coordinated resource allocation across marketing and product teams through 6 weekly sync meetings, maintaining on-track delivery for 3 parallel workstreams." | Excel model (not a PM primary signal; move to Skills if JD mentions Excel) |
| Event / Program Operations | REFRAME | "Managed cross-team communication across 3 functional groups, ensuring timely decision-making and resource readiness for project milestones." | All finance / modeling content deleted; only coordination signal retained |
| SWE Intern | DOWNPLAY | *(No bullets.)* One line: "Finance Team Lead, [Project Name], [Dates]" | Almost everything; SWE JD has no intersecting keyword |

Principle: The underlying facts do not change across versions. Only the observation lens (which dimension leads, which verb, which result is foregrounded) shifts to match the target JD.

---

## 6. Bullet Ordering Rule Within Each Experience Entry

1. First bullet → hits JD's highest-frequency required keyword.
2. Remaining bullets → ordered to mirror the sequence of JD Responsibilities (match JD's priority order, not chronological order of tasks).
3. If a dimension in the experience does not intersect with any JD keyword → move to last bullet or omit entirely.

Example reorder (DA role JD prioritizes: data analysis > reporting > stakeholder communication):
- Before: "Led weekly team meeting → Built Excel model → Wrote monthly report"
- After: "Built Excel model (data analysis) → Wrote monthly report (reporting) → Led weekly meeting (stakeholder communication)"

---

## 7. ATS Reality Check（ATS 现实）

- ATS systems do not automatically reject resumes. They organize and surface relevant applications for human review. 90–95% of resumes still receive human review.
- The widely cited "75% rejected by ATS" statistic has no verifiable source and is considered a myth by recruiting professionals (see Sources: S01).
- ATS keyword scanning goal: surface relevant resumes for human reviewers, not make hiring decisions.
- True hard filters (configured by hiring managers, not ATS vendors): work authorization status, specific required certifications, minimum degree level.
- ATS keyword score is a reference signal, not a hiring decision. Optimize for human readability first; keyword coverage second.
- Keyword coverage < 60% of Required items → flag inadequate match to user before spending time tailoring.

---

## 8. Reframing Ethics — Hard Boundary（侧写道德边界）

These rules are non-negotiable. Cross-reference: → **no-fabrication.md**

| Permitted | Prohibited |
|-----------|-----------|
| Shift which dimension of a real experience leads the bullet | Write a bullet about a task never performed |
| Use JD's vocabulary to describe something that actually happened | Add a tool or technology not actually used |
| Emphasize a result that genuinely occurred | Inflate a number or invent a metric |
| Omit irrelevant details from a bullet | Claim a scope or responsibility not held |
| Translate a Chinese role title into a functional English equivalent | Upgrade a junior role to a senior-sounding title that misrepresents authority |
| Reorder bullets to prioritize JD-relevant content | Reorder to imply the JD-relevant work was primary when it was incidental |

Reframing is a change of camera angle on real events. It is not a change of events.

If a required skill is missing from the candidate's experience → do not write it in. Flag the gap to the user and suggest legitimate ways to acquire it (course project, certification, etc.).

---

## 9. Workflow Integration — Step 3 Sub-steps

This section maps directly to `career-experience-mapper` Step 3 "Role Alignment":

### 3.1 Inputs Required
- Target JD full text (English preferred; Chinese JD accepted with note)
- Experience entries (Chinese or English; will be translated to English output)
- Master experience bank (all entries with full detail; maintained across job applications)

### 3.2 JD Decode
- Extract all technical terms, tool names, methodologies; rank by frequency × position
- Separate Required vs. Preferred keywords into two lists
- Identify verb category of JD's first 3 Responsibilities: analytical / execution / leadership

### 3.3 Per-Entry Relevance Scoring
For each experience entry, independently assess:
- Hard skill keyword hits: 0 / 1 / 2+
- Quantified outcome present: Y / N
- Verb-category match with JD primary Responsibilities: high / medium / low
- Output classification: F (Foreground) / R (Reframe) / D (Downplay) / C (Cut)

### 3.4 Reframe Execution (R-class entries)
- Identify which dimensions of the experience truly intersect with JD keywords
- Rewrite first bullet using JD vocabulary as primary lens
- Omit non-intersecting dimensions
- Never add dimensions not present in original experience

### 3.5 Natural Keyword Verification
- Each Required keyword appears 2–3 times total across resume sections
- No Required keyword appears > 2 times within a single section
- Required keyword coverage ≥ 80% → proceed; 60–79% → note gap; < 60% → warn user

### 3.6 Output Artifacts
- Versioned bullet set per experience entry, tagged by target JD
- Keyword coverage report (Required: N/M matched)
- F/R/D/C decision log with rationale (for candidate review and transparency)

---

## Sources

| ID | Source | URL |
|----|--------|-----|
| S01 | The Interview Guys — ATS rejection myth debunked | https://blog.theinterviewguys.com/ats-resume-rejection-myth/ |
| S02 | Klaxos — How Applicant Tracking Systems Work | https://klaxos.com/career-advice/how-applicant-tracking-systems-work/ |
| S03 | Jobscan — Top Resume Keywords | https://www.jobscan.co/blog/top-resume-keywords-boost-resume/ |
| S04 | Resumly — Aligning Resume with JD Keywords (2026 Graduates) | https://www.resumly.ai/blog/aligning-resume-with-jd-keywords-for-recent-graduates-2026 |
| S05 | Teal HQ — How to Read a Job Description | https://www.tealhq.com/post/how-to-read-a-job-description |
| S06 | Scion Staffing — Mastering Resume Without Keyword Stuffing | https://scionstaffing.com/mastering-resume-without-keyword-stuffing/ |
| S07 | University of Arizona Career Readiness — Tailoring Your Resume | https://career.arizona.edu/resources/tailoring-your-resume/ |
| S08 | Enhancv — Should I Include Irrelevant Experience | https://enhancv.com/blog/should-i-include-irrelevant-experience-on-a-resume/ |
| S09 | The Muse — Spin 1 Resume for 5 Industries (before/after case study) | https://www.themuse.com/advice/this-is-how-you-spin-1-resume-for-5-different-industries |
| S10 | Resumly — Aligning Resume for Career Changers (2026) | https://www.resumly.ai/blog/aligning-resume-with-jd-keywords-for-career-changers-2026 |
| S11 | Harvard Business School & Accenture — Hidden Workers (2021) | https://www.hbs.edu/managing-the-future-of-work/research/Pages/hidden-workers.aspx |
| S12 | Indeed Career Advice — Tailoring Your Resume | https://www.indeed.com/career-advice/resumes-cover-letters/tailoring-resume |
| S13 | West Virginia University Career Services — Tailoring Your Resume | https://careerservices.wvu.edu/resources/how-to-tailor-your-resume-to-impress-employers/ |
| S14 | MokaHR — Is Keyword Stuffing Ruining ATS | https://www.mokahr.com/myblog/is-keyword-stuffing-ruining-ats/ |
| S15 | Columbia University Career Education — Creating Strong Bullet Points | https://www.careereducation.columbia.edu/resources/resumes-impact-creating-strong-bullet-points |
| S16 | Santa Monica College Career Services — Tailoring Your Resume | https://www.smc.edu/student-support/career-services/resume-writing/tailoring-your-resume.php |
| S17 | Resumly — Analyzing JD to Extract High-Value Keywords | https://www.resumly.ai/blog/analyzing-job-descriptions-to-extract-highvalue-keywords |
