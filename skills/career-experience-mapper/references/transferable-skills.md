# transferable-skills.md
# Reference: career-experience-mapper skill

**What this file is:** A runtime reference tool for the `career-experience-mapper` skill.
It maps raw candidate experiences to defensible competency language using NACE 8 as the
primary output vocabulary, with O*NET cross-functional sub-skills as secondary anchors.
**How the skill uses it:** (1) Classify the raw experience using the 5-type input classifier.
(2) Apply the evidence threshold test before assigning any label. (3) Look up the applicable
mapping table (CS/tech track or non-technical track). (4) Select scale-appropriate verbs.
(5) Check output against the over-reach red list. Red-line rule: see `no-fabrication.md`.

---

## 1. NACE 8 Competency Definitions + Employer Priority

Primary vocabulary for all competency output. 83%+ of US university career centers and
their employer partners use NACE language. Output competency labels in NACE terms first.

### 1.1 NACE 8 Definitions

| # | Competency (能力域) | Core Definition |
|---|---|---|
| 1 | Career & Self-Development (职业与自我发展) | Proactively develop oneself through continual personal and professional learning; awareness of strengths and weaknesses |
| 2 | Communication (沟通) | Clearly and effectively exchange information, ideas, facts, and perspectives within and outside organizations |
| 3 | Critical Thinking (批判性思维) | Identify and respond to needs based on situational context and logical analysis |
| 4 | Equity & Inclusion (公平与包容) | Demonstrate awareness, attitude, knowledge, and skills to equitably engage people from different cultures |
| 5 | Leadership (领导力) | Recognize and capitalize on personal and team strengths to achieve organizational goals |
| 6 | Professionalism (职业素养) | Understand and demonstrate effective work habits; act in the interest of the larger community |
| 7 | Teamwork (团队协作) | Build and maintain collaborative relationships to work effectively toward common goals |
| 8 | Technology (技术应用) | Understand and leverage technologies ethically to enhance efficiencies and accomplish goals |

### 1.2 Key Behavioral Indicators (abbreviated)

- **Communication:** active listening, clarifying questions, adapting to diverse audiences, written + verbal + non-verbal
- **Critical Thinking:** sound decision-making, data analysis, anticipating needs, recognizing personal bias
- **Leadership:** innovative thinking, motivating others, building trust, managing projects
- **Teamwork:** conflict management, accountability, complementing others' strengths, building positive relationships
- **Technology:** adapting to new technologies, selecting appropriate tools, embracing change
- **Professionalism:** maintaining personal brand, showing dedication, demonstrating dependability

### 1.3 Employer Priority Ranking (NACE Job Outlook 2025, n=237)

| Priority | Attribute | % Employers Seeking |
|---|---|---|
| 1 | Problem-solving skills (→ Critical Thinking) | ~90% |
| 2 | Teamwork skills | ~80% |
| 3 | Written communication | ≥70% |
| 4 | Initiative (→ Career & Self-Development) | ≥70% |
| 5 | Strong work ethic (→ Professionalism) | ≥70% |
| 6 | Technical skills (→ Technology) | ≥70% |
| 7 | Verbal communication | >67% |
| 8 | Flexibility/adaptability | >67% |
| 9 | Analytical/quantitative skills (→ Critical Thinking) | >67% |

**Implication:** When surfacing competencies from raw experience, prioritize Problem-solving
and Teamwork signals first — they match the highest employer demand.

### 1.4 WEF Future of Jobs 2025: Top Skills on the Rise (supplementary)

For CS/technical role applications, cross-check mapped competencies against these signals:
AI and big data · Networks and cybersecurity · Technological literacy · Creative thinking ·
Resilience/flexibility/agility · Curiosity and lifelong learning · Analytical thinking.

---

## 2. Five-Type Experience Input Classifier

Before any mapping, classify the raw experience into exactly one of the five types below.
Each type has a characteristic competency yield profile. Do not mix profiles.

| Type | Label | Examples |
|---|---|---|
| A | Academic Coursework / Project (学术课程/项目) | Course assignments, semester projects, capstone, paper |
| B | Research / Lab Work (科研/实验室) | Research assistantship, thesis, lab data processing, paper replication |
| C | Extracurricular / Club / Organization (课外活动/社团) | Student org officer, club event, Model UN, debate, campus media |
| D | Paid or Unpaid Work (工作经历) | Internship, part-time job, freelance, co-op |
| E | Volunteer / Community Service (志愿/公益) | Community service, skills-based nonprofit consulting, tutoring volunteers |

**Classification rules:**
- A single experience may span types (e.g., a research internship = B + D). Apply the
  profile of the dominant context; note the secondary type in the evidence field.
- Hackathons: classify as A if course-organized, C if independent club event, D if sponsored.
- Teaching assistantships paid by the university = D; unpaid peer tutoring = E.

---

## 3. Evidence Threshold

### 3.1 The "Tell Me More" Test

**Rule:** Every competency claim must survive a 2-minute STAR follow-up in an interview.
If the candidate cannot tell a specific Situation → Task → Action → Result story, the claim
is over-reach. Assign a more conservative label or mark as "developing."

STAR components required before assigning a competency label:
- **Situation/Context:** scope (team size, project type, constraints)
- **Task/Action:** specific behavior performed — not "helped with" but "built," "led," "resolved"
- **Result:** outcome metric (grade, user count, time saved, funds raised, team outcome)
- **Reflection (optional):** for Leadership and Career & Self-Development claims, demonstrates
  learning and self-awareness

If Result is missing or the candidate says "I don't know": downgrade from "demonstrated" to
"developing." Output: "Evidence incomplete — suggest [metric type] to strengthen this claim."

### 3.2 Three-Level Evidence Standard (CS/Tech Skills)

| Level | Label | Condition | Resume Treatment |
|---|---|---|---|
| Strong | proficient in X | Used in submitted/deployed project; can discuss for >60 min; implemented end-to-end | List in main skills section |
| Medium | familiar with X | Completed coursework or tutorial; can describe core concepts; needs 1–2 weeks to reach production speed | List in a dedicated "familiar with" or "coursework" subsection |
| Weak | exposure only | Read about it; heard in lecture; never coded with it | Do not list; omit or move to a private learning log |

Note: the 60-minute threshold is practitioner consensus (Blind community), not peer-reviewed
research. Treat as a useful rule of thumb, not an empirical threshold.

### 3.3 Outcome Quantification Hierarchy

When a large absolute number is unavailable, use the following in priority order:
1. Performance comparison: "~40% faster vs sequential baseline" (must be explainable in interview)
2. Quality signal: "85%+ unit test coverage," "reduced CI build time from 4 min to 90 sec"
3. Relative scale: "one of five contributors," "sole developer," "across 3 academic departments"
4. Collaboration scope: "collaborated with 4 engineers," "demoed to 50+ attendees"

**Rule:** "Never invent, but always estimate." A defensible estimate with a clear method is
better than a blank; an invented number collapses under "compared to what?" See `no-fabrication.md`.

---

## 4. Mapping Tables

### 4.1 CS / Technical Track

Fuses R01 competency mapping with R06 CS transferable skills matrix.

| Experience Type | NACE Competency | O*NET Sub-skill | Recommended Verbs | Evidence Required |
|---|---|---|---|---|
| Course project — solo, implemented feature (单人课程项目) | Technology, Critical Thinking | Programming, Operations Analysis | Built, implemented, developed, designed | GitHub link, deployed demo, or submitted artifact |
| Course project — team, defined architecture (团队课程项目) | Teamwork, Technology, Critical Thinking | Programming, Systems Analysis | Architected, designed, coordinated | GitHub with commit history showing individual contribution; note team size |
| Paper replication / tutorial reproduction (复现论文/教程) | Technology, Critical Thinking, Career & Self-Development | Programming, Quality Control Analysis | Implemented, replicated, reproduced, validated | Paper/tutorial source; dataset; performance vs. baseline; any extension made |
| Research assistantship — data processing (科研数据处理) | Critical Thinking, Technology | Quality Control Analysis, Systems Evaluation | Processed, analyzed, validated, cleaned | Dataset size; tool used (e.g., SPSS, Python); output (paper, report, model) |
| Kaggle competition (any rank) (Kaggle 竞赛) | Critical Thinking, Technology | Complex Problem Solving | Competed, experimented, optimized, applied | Competition name; team count; model metric (AUC/RMSE/F1); method summary |
| Hackathon (any outcome) (Hackathon) | Critical Thinking, Technology, Teamwork | Complex Problem Solving | Prototyped, integrated, demonstrated, shipped | Hours (24h/36h); team size; individual module; presentation audience count |
| Open-source contribution — code (代码类开源贡献) | Technology, Professionalism, Communication | Programming, Instructing | Contributed, fixed, reviewed, refactored | PRs merged; issues resolved; project name and scale (stars as background only) |
| Open-source contribution — docs/tests (文档/测试类开源贡献) | Technology, Communication, Professionalism | Instructing, Quality Control Analysis | Authored, clarified, implemented, added | Number of merged PRs; specific change per PR (not "fixed typos") |
| Personal project — deployed/public (个人项目已部署) | Technology, Career & Self-Development | Technology Design, Programming | Built, launched, maintained, iterated | User count, GitHub link, or deployment URL; tech stack specifics |
| Personal project — self-use tool (自用工具) | Technology, Career & Self-Development | Programming | Developed, designed, shipped | Performance comparison vs. baseline; code quality signals (test coverage, CI); problem solved |
| CS internship — engineering (工程实习) | Technology, Professionalism, Teamwork | Full Technical category + Social Skills | Developed, optimized, delivered, presented | Measurable impact: % improvement, feature shipped, tickets closed, team size |
| Algorithm competition — ICPC, LeetCode ranked (算法竞赛) | Critical Thinking | Complex Problem Solving | Solved, optimized, achieved, ranked | Competition name; ranking or percentile; problems solved count |
| CS tutoring / Teaching assistant (CS 助教/辅导) | Communication, Technology | Instructing, Service Orientation | Tutored, explained, graded, mentored | Student count; session frequency; outcome metric if available |
| Technical club leadership — ACM, IEEE (技术社团干部) | Leadership, Teamwork | Management of Personnel Resources | Organized, recruited, directed, facilitated | Member count; events held; outcomes delivered |

**CS-specific articulation rules (from R06):**

- **Verb selection by project type:**
  - Original work: built, developed, designed, architected
  - Replication/tutorial: implemented, replicated, reproduced, explored
  - Collaborative: coordinated, contributed, integrated (note team size separately)

- **Tech stack notation:** Specify tool/version/library in the bullet (e.g.,
  "PyTorch 2.x + Hugging Face Transformers"), not a generic category ("ML framework").
  Core technology goes in the project title line; auxiliary tools go in the bullet body.

- **Individual vs. team contribution:** Use first-person implied verbs for your own work
  ("Implemented the data pipeline") and explicitly scope team outcomes ("Team deployed to
  500 users; I owned the ETL pipeline and reduced ingestion latency by 30%").

- **Course project annotation:** Mark origin in title or after project name —
  "Raft Consensus (Distributed Systems Course Project)" — transparency is an asset, not a liability.

- **ML/DS metrics:** Use model performance metrics (AUC, F1, RMSE, accuracy vs. baseline)
  as the primary quantifier; ranking is secondary and must be stated honestly.

- **GitHub star rule:** Stars are background context only, not an achievement metric.
  Omit star count; replace with tech decision rationale or performance comparison.

### 4.2 Non-Technical Track

| Experience Type | NACE Competency | O*NET Sub-skill | Recommended Verbs | Evidence Required |
|---|---|---|---|---|
| Student organization officer (学生组织干部) | Leadership, Teamwork, Professionalism | Management of Personnel Resources, Coordination | Directed, coordinated, recruited, managed | Member count; budget managed; events delivered |
| Club/organization event planning (社团活动策划) | Teamwork, Leadership, Professionalism | Coordination, Planning and Organising (UCF 15) | Planned, executed, coordinated, managed | Attendee count; budget; timeline met |
| Volunteer — community service (社区志愿服务) | Equity & Inclusion, Teamwork, Professionalism | Service Orientation, Coordination | Supported, organized, facilitated, delivered | Hours; beneficiaries served; program outcomes |
| Volunteer — skills-based (nonprofit consulting etc.) (专业志愿/非营利咨询) | Critical Thinking, Communication, Leadership | Complex Problem Solving, Persuasion | Advised, analyzed, recommended, presented | Organization name; problem addressed; recommendation outcome |
| Peer tutoring / volunteer tutoring (同伴辅导/志愿辅导) | Communication | Instructing, Service Orientation | Tutored, explained, supported | Student count; session frequency; outcome (grade improvement) if available |
| Teaching assistant — non-technical (非技术课助教) | Communication, Leadership | Instructing, Persuasion | Facilitated, graded, supported, led discussion | Course size; session frequency; student outcomes |
| Research paper — course or independent (研究论文) | Critical Thinking, Communication | Analysing (UCF 12), Writing and Reporting (UCF 11) | Synthesized, analyzed, argued, evaluated | Word count or pages; sources reviewed; grade or publication status |
| Research assistantship (any language) (科研助理) | Critical Thinking, Career & Self-Development | Analysing (UCF 12), Learning and Researching (UCF 13) | Assisted, processed, analyzed, summarized | Dataset/corpus size; tools used; output type |
| Part-time retail/service job (兼职零售/服务) | Professionalism, Communication, Teamwork | Service Orientation, Social Perceptiveness | Handled, resolved, assisted, maintained | Duration; customer volume; any promotion or commendation |
| Study abroad program (海外交流项目) | Equity & Inclusion, Communication, Career & Self-Dev | Adaptability, Social Perceptiveness | Navigated, adapted, collaborated, presented | Duration; location; specific cross-cultural project or output |
| Internship — business/consulting/policy (商业/咨询/政策实习) | Critical Thinking, Communication, Professionalism | Systems Analysis, Persuasion, Writing | Researched, developed, presented, recommended | Deliverable; stakeholder count; impact metric |
| Campus media / journalism (校园媒体/新闻) | Communication, Critical Thinking | Writing and Reporting (UCF 11), Analysing (UCF 12) | Reported, wrote, edited, published | Articles published; outlet name; readership if known |
| Model UN / debate team (模拟联合国/辩论) | Communication, Critical Thinking, Leadership | Persuasion, Negotiation, Presenting | Negotiated, argued, represented, chaired | Competition level; award if any; topic represented |

**Scope calibration — oral communication example:**
- 1:1 peer tutoring → Communication (oral, simplification, audience awareness). Valid but narrow.
- Workshop or club presentation (≥10 audience) → Communication (presenting). Broader claim.
- Structured cross-functional presentation → Communication (stakeholder). Requires specific evidence.
- Do not use "stakeholder communication" for 1:1 tutoring. Scale of audience determines scope.

---

## 5. Leadership Overclaim — Downgrade Rule

### 5.1 Background: The ~30% Perception Gap

NACE data (multiple secondary confirmations) shows students self-rate Leadership
approximately 30 percentage points higher than employers rate them on the same dimension.
This gap is the largest among all 8 NACE competencies and is specific to Leadership and
Professionalism. Employers downrate candidates who claim Leadership without behavioral
evidence more harshly than candidates who accurately claim Teamwork.

### 5.2 Leadership vs. Teamwork Decision Tree

Before assigning Leadership, require at least ONE of:
- (a) A specific **direction-setting decision** (e.g., chose the technical approach, re-scoped
  the project when requirements changed, resolved a priority conflict)
- (b) A specific **conflict-resolution action** (e.g., mediated between two team members,
  realigned a disengaged contributor to a new role)

If neither (a) nor (b) is present → assign **Teamwork (coordination sub-skill)** instead.

### 5.3 Verb Calibration by Scope

| Scope | Appropriate Verbs | NOT |
|---|---|---|
| Peer-group, 2–5 people, class project | coordinated, contributed, collaborated, facilitated | led, managed, directed |
| Small organization, club, research lab | organized, led, managed, implemented | oversaw, directed strategy |
| Institutional / departmental scale | directed, oversaw, developed strategy for | (appropriate at this level) |

**Rule:** Never use organizational-scale verbs for peer-group academic contexts.

### 5.4 Specific Downgrade Cases

| If the candidate says... | Assign | Because |
|---|---|---|
| "Organized meetings and kept everyone on track" in a class project | Teamwork (coordination) | No direction-setting; no conflict resolution; logistics only |
| "Kept the group motivated when the project stalled" + has a specific story of what they said/did | Leadership (initiation sub-skill) | Motivating a disengaged group = direction-setting behavior |
| "Assigned tasks based on each person's strengths" + can describe how they identified strengths | Leadership (capitalize on team strengths) | Matches NACE Leadership definition exactly |
| "Was team captain" without a specific story | Teamwork + title mention only | Title alone is not behavioral evidence |
| "Elected by teammates to lead" + has conflict-resolution story | Leadership | Formal peer selection + behavioral evidence = defensible |

**Interview coaching note:** Candidates may mention "informal leadership" in interviews only
if they have a specific conflict-resolution or direction-setting story ready. Without the
story, the mention is a liability, not an asset.

---

## 6. International Student Experience Handling

### 6.1 Core Principle: Separate Skill from Language

Technical and cognitive skills transfer across languages. Language-specific output does not.
Claiming "strong English written communication" based on a Chinese-language deliverable is
over-reach. Claiming "data analysis using SPSS" from the same experience is fully defensible.

### 6.2 Separation Rules

| Dimension | Transferability | Treatment |
|---|---|---|
| Technical skills (SPSS, Python, statistical methods, lab protocols) | Fully transferable | Claim explicitly; name the tool and method |
| Cognitive skills (synthesis, structured argumentation, analysis, research design) | Fully transferable | Claim the skill; anchor to the analytical/structuring dimension, not the language of output |
| Written communication — English | Requires English-language evidence | Do not claim based on Chinese-language reports; supplement with English writing samples or coursework |
| Verbal communication — English | Requires English-language evidence | Same as above; English presentation experience needed |
| Cross-cultural context | Asset — map to NACE Equity & Inclusion or WEF Adaptability | Frame positively: multilingual context-switching, international research environment, institutional adaptability |

### 6.3 Institution Name Format

Spell out the full English name or romanized name + "(China)" or "(Country)" for ATS
parsing and recruiter clarity. Example: "Peking University (China)" not "北京大学."

### 6.4 Applying the "Tell Me More" Test for International Experiences

The test must be performed in the target application language (English). If the candidate
can explain their methodology, findings, and constraints in English to a hiring manager,
the technical/cognitive claim is defensible regardless of the original language of the work.

### 6.5 Anti-patterns for International Candidates

- **Under-claiming:** Dismissing Chinese-university research as "not real experience" —
  incorrect. Technical and cognitive competencies are fully valid. Imposter syndrome is not
  a reason to omit legitimate skills.
- **Over-claiming:** Asserting "excellent English written communication" from a Chinese-
  language thesis — not defensible without supplementary English evidence.
- **Vague framing:** "International experience" as a standalone competency — not a NACE
  competency. Must be operationalized: cross-cultural collaboration → Equity & Inclusion;
  adapting to different institutional norms → Professionalism + Career & Self-Development.

---

## 7. Over-Reach Red List

The following patterns must trigger a warning — do not assign a competency label without
additional evidence. These are the most common resume over-reach patterns among new graduates.

### 7.1 Activity ≠ Competency

| Over-reach Pattern | Why It Fails | Correct Action |
|---|---|---|
| "Participated in a group project" → Leadership | Participation is presence, not leadership behavior | Apply Leadership downgrade rule (Section 5); default to Teamwork |
| "Attended a workshop on X" → Technology (X) | Passive attendance is not skill acquisition | Do not list X as a skill; list only if actively used in a project |
| "Helped with X" | "Helped" hides the actual contribution; not a competency statement | Ask: what specifically did you do? Then use a first-person action verb |
| "Was involved in X" | Same problem as "helped" — passive framing | Elicit the specific action and rewrite with an action verb |

### 7.2 Credential ≠ Competency Evidence

| Over-reach Pattern | Why It Fails | Correct Action |
|---|---|---|
| GPA → Critical Thinking or Analytical Skills | GPA is a credential filter, not a competency demonstrator (NACE employer screening of GPA dropped from 73% in 2019 to 42% in 2026) | Competencies need behavioral evidence: projects, research, problem-solving contexts |
| Dean's List / Honors → any competency | Award is a credential; it does not demonstrate a specific behavior | Cite the underlying project or coursework that earned it |
| "Completed X certification" → proficient in X | Certification shows course completion, not applied use | Cross-check against three-level evidence standard (Section 3.2) |

### 7.3 Skill Claim ≠ Evidence

| Over-reach Pattern | Why It Fails | Correct Action |
|---|---|---|
| "Familiar with X" in main skills section | Familiar with ≠ proficient; main skills section implies readiness | Move to "familiar with" subsection; or upgrade by adding a project citation |
| Tech stack list with no project evidence | List without proof is an empty claim; interview will expose the gap | Every listed skill must link to a project bullet with a verb + outcome |
| "Expert in X" | Expert implies mastery; triggers high-difficulty interview questions | Use "proficient" with project evidence, or simply show it in the bullet |
| "Strong [communication/leadership/X] skills" as a standalone claim | Adjective-noun claims without behavioral evidence are universally discounted | Replace with a STAR-structured bullet that demonstrates the behavior |

### 7.4 Scale/Scope Inflation

| Over-reach Pattern | Why It Fails | Correct Action |
|---|---|---|
| "Production-grade system" / "production-ready" for a course project | Implies deployment, SLA, monitoring — will collapse under deep-dive questioning | "Working prototype," "local deployment," "course project" |
| "Scalable architecture" without load-test data | No actual concurrency data = unverifiable claim | Omit, or "designed with horizontal scaling in mind (not yet load-tested)" |
| "Handled millions of requests" for a personal project | Without real traffic data, this is invented | Omit, or "load-tested to X RPS on local setup" |
| "Led the development" for informal peer collaboration | Implies formal authority that does not exist | "Contributed [module] in a [N]-person team" |
| "State-of-the-art model" without paper citation + data | SOTA is a technical claim requiring evidence | "Replicated [Paper, Year] achieving X% on [Dataset]" |
| "From scratch" for framework-based implementation | Implies zero external dependencies — almost never true | "Using [framework] with custom modifications to [component]" |
| Kaggle "competitive result" without stating rank | Vague framing invites harder follow-up questions | State rank honestly; lead with model metric instead |

### 7.5 Authorship Misrepresentation

| Over-reach Pattern | Why It Fails | Correct Action |
|---|---|---|
| Tutorial/replicated project presented as original design | Recruiters and engineers identify tutorial projects instantly; interview will expose it | Use "implemented / replicated / followed [source] and extended with [X]" |
| Team project presented as solo ("I built X") when it was collaborative | Contradicted by commit history, references, or follow-up | State team size; separate "I" contributions from team outcomes |
| GitHub star count as achievement metric | Stars are not a meaningful impact indicator; 40 stars may include self-star + friends | Remove star count; use performance comparison or code quality signals |

---

## Sources

All URLs are from R01 and R06 research reports. No URLs have been added or modified.

- NACE Career Readiness Competencies (April 2024): https://www.naceweb.org/career-readiness/competencies
- NACE Job Outlook 2025 via PennWest: https://career.pennwest.edu/blog/2025/10/14/what-are-employers-looking-for-when-reviewing-college-students-resumes-from-nace/
- NACE Quick Poll (83%+ implementation): https://www.naceweb.org/career-readiness/competencies/nace-quick-poll-more-than-83-percent-of-respondents-implementing-career-readiness-competencies
- Extern — NACE 8 Competencies Explained: https://www.extern.com/post/career-readiness-competencies-guide
- O*NET Cross-Functional Skills (US DOL): https://www.onetonline.org/find/descriptor/browse/2.B
- O*NET / CFR 20 §404.1568(d) via Wikipedia: https://en.wikipedia.org/wiki/Transferable_skills_analysis
- WEF Future of Jobs Report 2025: https://www.weforum.org/publications/the-future-of-jobs-report-2025/
- WEF Skills Outlook 2025 (chapter): https://www.weforum.org/publications/the-future-of-jobs-report-2025/in-full/3-skills-outlook/
- UCL Universal Competency Framework: https://www.ucl.ac.uk/career-frameworks/how-use-career-frameworks/map-your-transferable-skills
- Yale OCS — Student Athlete Transferable Skills: https://ocs.yale.edu/resources/yale-student-athlete-transferable-skills/
- Yale OCS — GSAS Transferable Skills: https://ocs.yale.edu/blog/2020/08/03/phd-transferable-skills/
- Vitae Researcher Development Framework: https://vitae.ac.uk/vitae-researcher-development-framework/
- UC Riverside HR Transferable Skills Library: https://hr.ucr.edu/employee-and-organizational-development/transferable-skills-library
- Binghamton University — Research on Resume: https://careertools.binghamton.edu/resources/how-to-add-research-experience-to-your-resume-or-cv/
- Penn State Smeal — NACE for Employers: https://careerconnections.smeal.psu.edu/resources/skills-employers-are-looking-for-nace-career-competencies/
- Prosper/University of Liverpool — Skills Inventory: https://prosper.liverpool.ac.uk/postdoc-resources/reflect/skills-inventory/
- Wiley/CDQ — Co-Curricular Activities and Competency Articulation (2024): https://onlinelibrary.wiley.com/doi/full/10.1002/cdq.12358
- UT Austin CNS — Strong Bullets Technical Resumes: https://careerservices.cns.utexas.edu/resources/resumes/strong-bullets-technical-resumes
- freeCodeCamp — Killer SWE Resume: https://www.freecodecamp.org/news/writing-a-killer-software-engineering-resume-b11c91ef699d/
- Adithya Solai Medium — Golden Resume Rules for CS Majors: https://adithyasolai.medium.com/golden-resume-rules-for-cs-majors-af2f591d6457
- formation.dev — Ex-Meta Recruiter SWE Resume Guide: https://formation.dev/blog/software-engineer-resume-guide-examples/
- story.cv — Metrics in Resume: https://story.cv/blog/articles/metrics-in-resume
- Medium InterviewingSoftwareEngineers — Project Deepdives: https://medium.com/interviewingsoftwareengineers/project-deepdives-tips-for-interview-3dd5399ee854
- opensource.com — Add OSS to Resume: https://opensource.com/business/16/2/add-open-source-to-your-resume
- Tufts University Career Center — Hackathon on Resume: https://careers.tufts.edu/blog/2024/10/28/how-to-include-hackathons-on-your-resume/
- interviewkickstart — List Projects on SWE Resume: https://interviewkickstart.com/blogs/articles/list-projects-on-software-engineer-resume
- Kaggle Q&A — How to present Kaggle on resume: https://www.kaggle.com/questions-and-answers/363750
- Kaizen Conroy Medium — CS Resume Red Flags: https://kaizen-conroy.medium.com/4-computer-science-resume-red-flags-to-avoid-from-a-recruiter-f578720d2e4e

Framework version anchor: NACE April 2024 · WEF Future of Jobs 2025
