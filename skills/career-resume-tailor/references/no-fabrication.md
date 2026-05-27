# no-fabrication.md — career-skills Pack 共享红线文件

**归属 skill：** `career-experience-mapper` | **版本：** v1.0 | **来源：** intermediate/research/R03-integrity-boundary.md
**作用域：** 本文件是整个 `career-skills` pack 的诚信地基，所有 skill 必须引用并遵守本文件全部条款。
**编译层级：** RULE-* 条款及 CLAUSE-URL-01 须编译为 system prompt 级硬性约束，不得降级为建议。
**双语约定：** 中文思路，英文产出；NACE 8 能力词汇为主。

---

## 1. 硬性禁止清单 Hard Prohibitions

以下字段严禁编造、虚报或与候选人提供信息不符。背调可核查、法律可追责、面试可戳穿。

**RULE-01｜禁止虚构雇主**
不得列出候选人从未工作过的公司名称、公司性质或雇主联系方式。
Do not generate any employer name, entity type, or contact not confirmed by the candidate.

**RULE-02｜禁止伪造任职日期**
不得拉长、缩短、合并或修改起止日期（精度：月份级别）。
Do not alter, extend, compress, or merge employment dates. Accuracy required to month level.

**RULE-03｜禁止职级跳升**
不得在未使用双职称透明格式的情况下，将"实习生"写成"工程师"，将"助理"写成"经理"，或进行任何实质性职级提升。
Do not inflate job titles without the transparent dual-title format (Industry Title / Official Title).

**RULE-04｜禁止发明成果数字**
不得生成候选人无法在面试中解释来源的具体百分比、金额、用户数或增长率。
Do not generate any metric the candidate cannot explain the source of in an interview.

**RULE-05｜禁止虚构奖项荣誉**
不得列出候选人未实际获得的任何奖项、称号、荣誉或竞赛名次。
Do not list any award, honor, or recognition not confirmed by the candidate.

**RULE-06｜禁止虚构项目**
不得描述候选人未参与的项目，或候选人未完成的交付物。
Do not describe projects not participated in, or deliverables not completed by the candidate.

**RULE-07｜禁止动词越级**
在候选人没有决策权或领导职能的情况下，不得使用 Led / Managed / Directed / Spearheaded 等 Level 4 动词。
Do not use Level 4 verbs (Led, Managed, Directed) without evidence of actual decision-making authority.

**RULE-08｜禁止虚报技术技能**
不得列出候选人不具备的编程语言、框架、工具或证书（包括仅"听说过"但从未实际使用的技能）。
Do not list technical skills, tools, or certifications the candidate has not actually used.

**RULE-09｜禁止学历造假**
不得声称候选人未完成的学位、未就读的学校，或未获得的专业认证。
Do not claim any degree, institution, or professional certification not completed or awarded.

**RULE-10｜禁止编造链接（见 CLAUSE-URL-01）**
不得生成候选人未提供的 GitHub 仓库、作品集网址、已发布产品或论文链接。
Do not generate any URL not explicitly provided by the candidate. See CLAUSE-URL-01.

**RULE-11｜禁止将团队成果全归个人**
不得在无说明的情况下，将团队整体成果以第一人称单数直接归于候选人个人。
Do not attribute team achievements solely to the candidate without contextualizing team scope and individual role.

---

## 2. CLAUSE-URL-01 不得编造链接条款

> **CLAUSE-URL-01（全 Pack 强制，不得降级）**
>
> `career-experience-mapper` 及所有依赖本文件的 skill，在处理候选人输入时，**严禁生成以下内容**：
> - 候选人未提供的 GitHub 仓库链接
> - 候选人未提供的作品集网址（Portfolio URL）
> - 候选人未提供的已发布产品 / APP / 论文链接
> - 任何由 AI 自行推断、补全或猜测的 URL
>
> **处理规则：**
> - 候选人提供了真实链接 → 原样引用，不修改、不缩短、不替换
> - 候选人未提供链接 → 省略链接字段，不占位，不写"[insert URL]"，不伪造
> - 候选人描述了项目但未提供链接 → 仅描述项目内容，不生成任何 URL
>
> **违反后果（供 skill prompt 引用）：**
> 编造链接是可即时核查的造假行为。招聘方点击即知真伪，一经发现将直接导致录用撤销，且对候选人信誉造成不可修复的损害。

---

## 3. 诚信决策树 Integrity Decision Tree

对每一条候选人经历描述，在输出前按顺序执行以下判断：

```
输入：候选人描述某段经历 / 某项技能 / 某项成就

Q1｜雇主 / 职称 / 日期是否真实？
    ├── 否 → REJECT：不得生成，提示候选人核实后重新输入
    └── 是 → 继续 Q2

Q2｜成果数字是否有可解释的依据？
    ├── 无依据 → 删除数字，改用定性描述（流程改善 / 交付物 / 认可记录）
    ├── 有依据（估算区间可解释）→ 保留，使用区间而非精确值
    └── 候选人能说出数据来源 → 保留原数字，继续 Q3

Q3｜动词级别是否与实际贡献匹配？
    ├── 动词越级（用 Led 但无决策权）→ 降级至 Level 1-2 保守动词
    ├── 动词不足（Participated in 但有具体贡献）→ 升级至 Level 2 具体动词
    └── 匹配 → 继续 Q4

Q4｜内容能否在面试中自圆其说？（"tell me more" 测试）
    ├── 无法展开回答 → 重写或降级表述
    └── 能展开、有细节 → OUTPUT：允许输出
```

---

## 4. 保守动词工具箱 Conservative Verb Toolkit

**使用原则：**
- 无法在面试中举出具体例子的动词 → 强制降级一档
- 团队项目中默认使用 Level 1-2，除非有明确证据支持更高级别
- 避免全简历使用同一动词，多样化展示不同贡献类型

### Level 1｜支持 / 辅助类 — 适用于次要贡献角色

| 中文 | 英文动词 | 适用场景 |
|------|---------|---------|
| 协助 | Assisted | 在他人主导下完成具体任务 |
| 支持 | Supported | 为核心工作提供后勤或技术支撑 |
| 配合 | Collaborated with | 与他人平等合作完成任务 |
| 贡献 | Contributed to | 为整体成果提供具体的一部分 |
| 参与 | Participated in | 作为团队成员参与某项活动（最弱，慎用，优先升级为具体描述） |

**降级触发：** 候选人在他人指导下完成任务；无独立决策权；贡献为整体的一个子部分。

### Level 2｜执行 / 实施类 — 适用于独立完成某部分工作

| 中文 | 英文动词 | 适用场景 |
|------|---------|---------|
| 执行 | Executed | 按规格独立完成了具体任务 |
| 分析 | Analyzed | 收集、整理、分析数据或信息 |
| 准备 | Prepared | 制作文档、材料、报告 |
| 整理 | Organized | 对信息、资源或流程进行整合 |
| 研究 | Researched | 进行调研、文献综述 |
| 记录 | Documented | 撰写技术文档或会议记录 |
| 测试 | Tested | 进行功能或质量测试 |
| 汇总 | Summarized | 整理并提炼信息 |

**适用条件：** 候选人独立负责某个明确子任务，有具体交付物，但不涉及他人管理或整体方向决策。

### Level 3｜协调 / 推进类 — 适用于有横向协调职责但无下属管理权

| 中文 | 英文动词 | 适用场景 |
|------|---------|---------|
| 协调 | Coordinated | 跨团队或多方资源协调 |
| 跟进 | Tracked | 跟踪进度、维护记录 |
| 促进 | Facilitated | 推动会议或流程顺利进行 |
| 沟通桥接 | Communicated | 作为信息传递节点 |
| 辅助设计 | Assisted in designing | 参与设计讨论但非最终决策者 |

**适用条件：** 候选人负责跨职能沟通或流程推进，但无正式下属或预算控制权。

### Level 4｜主导 / 所有权类 — 仅适用于有充分证据的领导职能

| 中文 | 英文动词 | 适用场景（需有真实依据） |
|------|---------|---------|
| 主导 | Led | 有团队领导权或项目决策权 |
| 管理 | Managed | 管理人员、预算或项目整体 |
| 建立 | Established | 从零创建某个流程、系统或团队 |
| 设计 | Designed | 独立完成设计方案并被采纳 |
| 开发 | Developed | 独立开发了完整功能或产品 |
| 交付 | Delivered | 完整交付了某项有明确范围的成果 |

**使用门槛：** 候选人须能在面试中说明：谁向你汇报 / 你做了哪些技术或产品决策 / 最终成果是否由你sign-off。不能回答则降至 Level 2-3。

---

## 5. 重构 OK vs 造假 NOT-OK 对照表

| 场景 | NOT-OK 造假 | OK 重构 | 判断依据 |
|------|-------------|---------|---------|
| 课程项目（非真实工作） | "Deployed ML model to production serving 10K users" | "Developed ML model for image classification as part of graduate coursework, achieving 92% accuracy on held-out test dataset" | 虚构生产环境 vs 真实学术成果 |
| 团队主导的项目 | "Led cross-functional team to launch product feature" | "Contributed front-end development to cross-functional team launch of X feature; owned [具体模块] end-to-end" | 无领导权时不得使用 Led |
| 实习辅助工作 | "Managed social media strategy resulting in 50% growth" | "Assisted marketing team in executing social media calendar; created 3 posts/week across Instagram and LinkedIn" | 辅助≠管理；50%增长无数据来源 |
| 兼职/零工职级 | "Operations Manager at [餐厅]"（实际是服务员） | "Server, [餐厅名] — handled high-volume service for 30+ tables/shift, resolved customer issues, cross-trained 2 new staff members" | 职级跳升 vs 如实描述真实职责 |
| 无量化数据 | "Improved team efficiency by 35%" | "Streamlined onboarding documentation, reducing average ramp-up time for new team members from 3 weeks to 2 weeks" | 无来源数字 vs 具体 before/after 对比 |
| 职称翻译（内部非标准名） | "Software Engineer"（实际是"Software Engineer in Test"，隐去 in Test） | "Software Engineer in Test (QA)" 或 "Quality Assurance Engineer (Software Engineer in Test)" | 隐瞒信息 vs 透明双格式 |
| 技能熟练度夸大 | "Expert in Python, TensorFlow, Kubernetes, AWS"（仅上过一门课） | "Familiar with Python and TensorFlow through [课程名] coursework on Coursera; deployed model in local environment" | 虚报专家级 vs 如实标注来源和程度 |
| 无链接时占位 | 在简历列出未部署或不存在的 GitHub URL | 不列链接；或仅在有真实可访问 repo 时列出 | 虚假 URL vs 真实或省略，见 CLAUSE-URL-01 |
| 团队成果全归个人 | "Built and launched the company's new onboarding system" | "Contributed backend API development to team-built onboarding system; personally owned user authentication module" | 团队协作成果须说明个人职责范围 |
| 实习期间"推动"结果 | "Drove 20% increase in pipeline by redesigning outreach strategy" | "Supported sales team's outreach redesign initiative; drafted 15 email templates used in A/B test that contributed to pipeline growth" | 夸大个人决策影响力 vs 如实描述个人具体贡献 |

---

## 6. 背调现实 Background Check Reality

### 核查字段

| 字段 | 是否核查 | 精度 |
|------|---------|------|
| 雇主名称（Employer Name） | 必查 | 直接联系 HR 或第三方核查 |
| 职位名称（Job Title） | 必查 | 与简历对比，不符即标记 |
| 起止日期（Employment Dates） | 必查 | 月份级别精度 |
| 学历 / 学位（Degree & Institution） | 必查 | 教育核查独立流程 |
| 薪资（Salary） | 通常不查 | 多数背调服务明确排除 |
| 工作职责细节（Job Duties） | 通常不查 | 背调不验证，面试验证 |

**关键推论：** 职责描述层面的合理重构空间更大，但面试仍会追问，候选人须能自圆其说。

### 行业数据（HireRight 2025 Global Benchmark Report）

- 超过 **75%** 的雇主在过去 12 个月内发现了候选人信息差异
- **13%** 的企业平均每 5 位候选人中发现 1 例差异
- 就业核查差异自 2021 财年起增长 **44%**
- APAC 地区：72% 的差异来自就业核查；EMEA：64%

### 法律后果分级

| 行为类型 | 后果级别 | 法律性质 |
|---------|---------|---------|
| 虚构学历 / 专业执照 | 高风险：撤职 / 诉讼 / 刑事 | 可能构成欺诈罪（联邦雇主、政府职位） |
| 虚构就业经历 / 雇主 | 中高风险：录用撤销 / 终止合同 | 民事欺诈（需证明实质性依赖 + 损失） |
| 夸大职级 / 职责 | 中风险：录用撤销 | 通常非刑事；签署声明后升级为书面欺诈 |
| 合理重构（有真实基础） | 低风险 | 一般合法；面试时须能自圆其说 |

**红线：** 候选人签署"所提供信息真实"声明后，任何已知虚假信息均可构成法律责任。

---

## 7. "tell me more" 可解释数字测试

在输出任何数字或成就描述前，对候选人的原始输入执行以下测试：

**测试 1｜数字来源测试**
> "你能说出这个数字是用什么工具或报告追踪的吗？"
- 能回答（具体说出工具名称、报告周期、样本范围）→ 数字可用
- 不能回答 → 删除数字，改用定性描述

**测试 2｜展开测试（"tell me more"）**
> 假设面试官追问："能具体说说你是怎么做到的吗？"
- 候选人能展开 2-3 个具体细节 → 内容可保留
- 候选人无法展开 → 重写或降级动词和表述

**测试 3｜无数字时的替代链**（Case B 规则，按优先级排序）
1. 频率 / 规模：每周服务多少客户、处理多少工单
2. 具体交付物：交付了什么、解决了什么问题
3. 可验证的认可：奖项、晋升记录、管理层表扬的具体形式
4. 流程对比（before/after）：改变前后的状态描述

禁止跳过以上四层直接发明数字。

---

## 8. Skill 输出前自检 Checklist

在生成任何简历条目、职责描述或技能列表前，执行以下全部检查。所有项目须为 ✅ 方可输出：

- [ ] **R01｜雇主一致**：雇主名称与候选人提供信息完全一致，无自行修改
- [ ] **R02｜日期一致**：起止日期与候选人提供信息完全一致，无拉长或缩短
- [ ] **R03｜职称合规**：职称使用了透明双格式（如适用），或与候选人确认的官方职称一致
- [ ] **R04｜无幽灵链接**：未生成候选人未提供的任何 URL（遵守 CLAUSE-URL-01）
- [ ] **R05｜数字可解释**：所有数字候选人能说出来源，或已替换为定性描述
- [ ] **R06｜动词级别匹配**：未越级使用 Led / Managed / Directed（无领导权则降至 Level 1-2）
- [ ] **R07｜团队成果已归因**：团队项目明确标注了个人职责范围，未将整体成果归于个人
- [ ] **R08｜技能真实**：所有技能均为候选人实际使用过的，无"仅听说过"或"计划学习"的技能
- [ ] **R09｜学历真实**：所有学历、证书均为候选人已完成并获得的
- [ ] **R10｜tell-me-more 通过**：内容能在面试中展开 2-3 个具体细节自圆其说

---

## Sources

- GoodHire — Employment Verification: https://www.goodhire.com/screening/employment-verification/
- iprospectcheck — Do Background Checks Show Employment History: https://iprospectcheck.com/do-background-checks-show-employment-history/
- HireRight 2025 Global Benchmark Report: https://www.hireright.com/company/newsroom/identity-fraud-and-candidate-discrepancies-remain-key-concerns-for-employers
- PARWCC Code of Ethics: https://parwcc.com/code-of-ethics/
- Harvard FAS Mignone Center — Create a Strong Resume: https://careerservices.fas.harvard.edu/resources/create-a-strong-resume/
- MIT CAPD — Resume Action Verbs: https://capd.mit.edu/resources/resume-action-verbs/
- Cruit — How to Ethically Change Your Job Title: https://www.askcruit.com/resume/writing/reframe-job-title
- Cruit — Quantify Resume Achievements: https://www.askcruit.com/resume/writing/quantify-resume-achievements
- Jobscan — You Don't Need Numbers on Your Resume: https://www.jobscan.co/blog/dont-need-numbers-accomplishments-resume/
- LawDepot — Legal Consequences of Lying on Your Resume: https://www.lawdepot.com/us/resources/business-articles/legal-consequences-of-lying-on-your-resume/
- FindLaw — Lying on a Resume or Job Application: https://www.findlaw.com/employment/hiring-process/lying-on-a-resume-or-job-application.html
- Indeed — How Do Background Checks Verify Employment: https://www.indeed.com/career-advice/finding-a-job/how-do-background-checks-verify-employment
- PerfectlyHired — Job Title Discrepancy Background Check: https://perfectlyhired.com/knowledge-hub/candidate-screening/job-title-discrepancy-background-check-recruitment
- NACE — Principles for Ethical Professional Practice: https://www.naceweb.org/career-development/organizational-structure/principles-for-ethical-professional-practice/
- University of Colorado Boulder Career Services — Action Verbs: https://www.colorado.edu/career/job-searching/resumes-and-cover-letters/resumes/action-verbs-use-your-resume
