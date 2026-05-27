# role-language-bank · 岗位语言工具手册

用途：供 `career-experience-mapper` 运行时直接调用的动词库、公式集与本地化规则。
输入来源：中文原始经历（口语/职责描述/谦辞句式）。输出目标：英文简历 bullet。
红线：绝不编造雇主/职称/日期/数字/奖项/技能/URL，证据不足→保守动词，中→英不加事实。
交叉引用：`no-fabrication.md`（所有数字、头衔、成就须候选人确认，skill 不自行生成）。
词汇主轴：NACE 8 能力域（Critical Thinking / Communication / Teamwork / Technology / Leadership /
Professionalism / Career Management / Equity & Inclusion）。

---

## §1 Bullet 公式集

每个公式含：结构模板（中英）+ 中文原始经历→英文产出示例。

### 1.1 XYZ 公式（Google / Laszlo Bock，量化优先场景）

**结构：**
```
EN:  Accomplished [X] as measured by [Y], by doing [Z]
     → [强动词] + [成就/产出] + [量化衡量] + by/through/via + [方法/工具]
ZH:  [强动词] + [成就本体] + [可量化指标] + 通过 + [方法/工具]
```

**示例 A（有精确数字）：**
- 中文原始经历：给搜索加了缓存，感觉快了不少
- 英文产出：`Reduced search latency by 65% by implementing Elasticsearch caching layer, improving 30-day user retention by 12%`

**示例 B（技术岗测试覆盖率）：**
- 中文原始经历：写了很多单元测试，覆盖率提高了
- 英文产出：`Increased unit test coverage from 43% to 87% by writing 200+ pytest cases for the payment service module, catching 3 critical regression bugs pre-release`

**使用条件：** 候选人能提供 Y（度量指标）且面试中可解释估算方法。若无法提供 Y，降级为 §1.4。

---

### 1.2 PAR 公式（通用简洁场景，MIT CAPD 推荐）

**结构：**
```
EN:  [Problem/Context] → [Action: 强动词 + 具体行动] → [Result/Impact]
     实用简化：[强动词] + [what you did] + [context/scope] + [result]
ZH:  [背景] → [动作] → [结果]
```

**示例 A（学生活动）：**
- 中文原始经历：帮忙改了一下新人培训材料
- 英文产出：`Redesigned onboarding checklist into structured 2-week program, eliminating repeated questions from new hires across 3 cohorts`

**示例 B（文档整理）：**
- 中文原始经历：负责整理会议记录
- 英文产出：`Documented meeting minutes for weekly department meetings and tracked 20+ action items, ensuring 90% on-time resolution`

---

### 1.3 CAR 公式（技术/管理岗，挑战背景驱动场景，Columbia 变体）

**结构：**
```
EN:  [Challenge 背景，可融入动词] → [Action：技术决策+执行] → [Result：技术或业务指标]
ZH:  [挑战] → [行动：技术选型+实现] → [结果]
```

**示例 A（数据库优化）：**
- 中文原始经历：把慢查询优化了一下
- 英文产出：`Addressed critical performance bottleneck in legacy MySQL queries; migrated aggregation logic to Redis cache layer, reducing average response time from 4s to 280ms for 10K+ daily active users`

**示例 B（团队协作，部分所有权）：**
- 中文原始经历：协助团队优化了数据库查询
- 英文产出：`Optimized 12 PostgreSQL queries using index tuning and EXPLAIN ANALYZE within a 5-person backend team, cutting average API response time from 850ms to 180ms`

**注：** "协助/参与"类原文→先核实实际贡献范围，若为真实执行者，直接用强动词（见§5）。

---

### 1.4 无数字 Scope 版（Quantification-Free Strong Bullet）

**结构：**
```
EN:  [强动词] + [具体行动] + [scope: 规模/频率/认可] + [qualitative outcome]
ZH:  [强动词] + [行动] + [可估算规模] + [定性结果]
```

**示例 A（科研助理，无发表论文）：**
- 中文原始经历：帮导师查了很多文献
- 英文产出：`Synthesized 25+ peer-reviewed papers on NLP transformer architectures to support lab's NSF grant proposal; findings adopted as theoretical framework for 3-year research roadmap`

**示例 B（课程项目，无生产数据）：**
- 中文原始经历：做了一个网页应用课程项目
- 英文产出：`Architected and deployed a full-stack task management app (React / Node.js / PostgreSQL) with JWT authentication and role-based access control; implemented 15 REST API endpoints covering CRUD operations for 3 user roles`

**数字来源说明：** "25+"和"15"均来自候选人可回忆的实际工作量；skill 不生成此类数字，仅提供框架由候选人自填。

---

## §2 Action Verb 库（6 维，NACE 能力域对齐，中英对照）

### 维度 1：技术构建 Technical Building
（NACE: Technology）

| EN Verb | 适用场景 | ZH 对照 |
|---------|----------|---------|
| Architected | 系统设计，高层技术决策 | 架构设计 |
| Engineered | 工程实现，强技术信号 | 工程化实现 |
| Implemented | 功能实现，通用 | 实现/落地 |
| Deployed | 部署上线，含容器化 | 部署 |
| Built | 从零构建 | 构建 |
| Developed | 开发，最通用 | 开发 |
| Automated | 自动化脚本/CI-CD 流水线 | 自动化 |
| Optimized | 性能/查询/流程优化 | 优化 |
| Debugged | 问题排查，缺陷定位 | 调试/排查 |
| Migrated | 数据/架构迁移 | 迁移 |
| Refactored | 代码重构，不改外部行为 | 重构 |
| Integrated | 系统/API 集成 | 集成 |
| Configured | 配置管理，CI/环境配置 | 配置 |
| Containerized | Docker/K8s 容器化 | 容器化 |
| Tested | 编写测试，配合覆盖率指标 | 测试 |

**技术岗红线：** 不得只列技术栈（"Used Python, React, SQL"），verb 之后必须跟功能/语境/结果。

---

### 维度 2：研究与分析 Research & Analysis
（NACE: Critical Thinking）

| EN Verb | 适用场景 | ZH 对照 |
|---------|----------|---------|
| Synthesized | 文献综述，整合多源信息 | 综合梳理 |
| Investigated | 问题研究，根因分析 | 调研分析 |
| Analyzed | 数据/逻辑分析，通用 | 分析 |
| Evaluated | 方案评估，A/B 对比 | 评估 |
| Modeled | 统计/ML 建模 | 建模 |
| Validated | 假设验证，A/B 测试 | 验证 |
| Benchmarked | 性能基准测试，横向对比 | 基准测试 |
| Extracted | 特征提取，数据提取 | 提取 |
| Identified | 发现问题/规律，根因定位 | 识别/发现 |
| Designed (experiment) | 实验设计，研究方案 | 设计实验 |

---

### 维度 3：领导与推动 Leadership & Driving
（NACE: Leadership）

| EN Verb | 适用场景 | ZH 对照 |
|---------|----------|---------|
| Spearheaded | 主导推动，首创性行动 | 主导/牵头 |
| Led | 带领团队，项目负责人 | 带领 |
| Orchestrated | 多方协调，整体统筹 | 统筹协调 |
| Directed | 指导方向，管理执行 | 指导方向 |
| Initiated | 发起，提出并推动落地 | 发起 |
| Launched | 发起新项目/产品/计划 | 发起/上线 |
| Championed | 倡导推动，文化/方案 | 倡导推进 |
| Facilitated | 促成，使能关键进程 | 促进/推动 |
| Mobilized | 调动资源/人员 | 调动 |
| Founded | 创建组织/团队/项目 | 创建 |

**红线：** "Led/Spearheaded"仅在候选人实际掌控了人员或决策时使用；协作场景用§2维度4词汇。

---

### 维度 4：沟通与协作 Communication & Collaboration
（NACE: Communication / Teamwork）

| EN Verb | 适用场景 | ZH 对照 |
|---------|----------|---------|
| Presented | 汇报，正式演讲 | 汇报/演讲 |
| Collaborated | 多方协作（比 helped 强） | 协作 |
| Liaised | 跨部门/跨团队对接 | 对接协调 |
| Authored | 撰写技术文档/报告 | 撰写 |
| Drafted | 起草方案/邮件/文档 | 起草 |
| Communicated | 沟通（最通用，少用） | 沟通 |
| Negotiated | 谈判，条件协商 | 协商 |
| Briefed | 简报汇报，向上传递 | 简报 |
| Documented | 文档化，整理记录 | 记录/整理 |
| Coordinated | 统筹协调，多方对齐 | 协调 |

---

### 维度 5：成就与影响 Accomplishment & Impact
（NACE: Critical Thinking / Professionalism）

| EN Verb | 适用场景 | ZH 对照 |
|---------|----------|---------|
| Accelerated | 加速某进程/上线时间线 | 加速 |
| Achieved | 达到目标，通用成就 | 实现/达到 |
| Boosted | 提升（需配数字） | 提升 |
| Reduced | 降低成本/时间/错误率 | 降低 |
| Improved | 改善，通用 | 改善 |
| Streamlined | 简化/精简流程 | 精简/流程化 |
| Transformed | 根本性改变 | 转型/转变 |
| Eliminated | 消除问题/浪费/瓶颈 | 消除 |
| Surpassed | 超越目标/指标 | 超越 |
| Pioneered | 开创先例，首次引入 | 开创 |

---

### 维度 6：教学与指导 Teaching & Mentoring
（NACE: Teamwork / Leadership）

| EN Verb | 适用场景 | ZH 对照 |
|---------|----------|---------|
| Mentored | 一对一持续指导 | 辅导 |
| Trained | 正式培训，批量教学 | 培训 |
| Coached | 过程性辅导，提升表现 | 指导 |
| Instructed | 正式授课，课堂教学 | 授课 |
| Guided | 引导，轻量指导 | 引导 |
| Advised | 提供建议，顾问角色 | 提供建议 |
| Onboarded | 带新成员入职 | 入职引导 |

---

## §3 弱动词→强动词升级表

**使用规则：** 升级前必须核实候选人实际行动深度；禁止在贡献不变的情况下只换词（红线）。

| 弱动词 | 问题诊断 | 升级选项（按参与深度排序） |
|--------|----------|--------------------------|
| `Responsible for` | 被动、任务导向，无主体性 | Led / Owned / Managed / Directed（主导）; Implemented / Built / Designed（执行）|
| `Helped with` | 贡献模糊，角色不清 | Collaborated on / Co-developed / Contributed to（协作）; Supported + 具体产出（支撑）|
| `Worked on` | 无主体性，最泛化 | Built / Implemented / Engineered / Designed（执行类）; Contributed to / Participated in（最保守）|
| `Assisted` | 角色边缘化，旁观暗示 | Facilitated / Enabled / Supported + outcome（有产出）; 若实为执行者→直接用强动词 |
| `Was involved in` | 最弱，近乎无效 | 必须重写：明确候选人具体做了什么，选对应动词，无法明确→保守用 Contributed to |
| `Participated in` | 谦辞保留，Chinglish 来源 | 核实后：若真实执行→Developed/Built; 若协作→Collaborated with N-person team |

**升级决策树：**
```
输入含弱动词
 ↓
候选人是否掌控了整体流程/人员？
  Yes → Led / Managed / Directed
  No  → 候选人是否独立执行了某子模块？
          Yes → Built / Implemented / Developed（加 "in a team of N" 保留协作语境）
          No  → 候选人贡献是否可描述为具体产出？
                  Yes → Collaborated / Contributed to + 具体产出
                  No  → 保守：Supported + 可描述动作（避免升级）
```

---

## §4 无数字时的量化 Fallback（按优先级排序）

**原则：** 只用候选人面试中能解释方法论的数字；无法解释→用定性替代，不编造。
**技术岗首选 Priority 1（Technical Specificity）**；其余按实际情况选择。

### Priority 1：Technical Specificity（技术精度替代业务数字）
**适用：** CS / 软件 / 数据岗首选
```
模板：[动词] + [具体技术产出] + [技术规模数字：API 数/测试数/组件数/数据量级]
示例：Implemented 15 REST API endpoints with input validation and error handling across 4 resource types
示例：Wrote 200+ unit tests (pytest) covering the payment service module
```

### Priority 2：Scope Anchoring（规模锚定）
**适用：** 有团队/受众/数据集规模可估算时
```
模板：[动词] + [N+ 或 N–M 范围] + [对象/受众]
示例：Supervised 7–12 undergraduate researchers across 2 academic years
注：范围需面试中能说明"大概怎么估的"
```

### Priority 3：Frequency Signal（频率信号）
**适用：** 重复性持续工作，证明密度和可靠性
```
模板：[动词] + [工作内容] + [频率] + [受众/目的]
示例：Compiled and distributed weekly performance dashboard to 12-person cross-functional team
```

### Priority 4：Qualitative Outcome（定性结果）
**适用：** 无任何数字时，描述状态变化
```
模板：[动词] + [行动] + [从状态A到状态B的变化]
示例：Redesigned data pipeline from manual CSV exports to fully automated ETL process, eliminating weekly manual reconciliation
注：ATS 扫描数字友好度低于量化；此为最后手段，先穷尽前三优先级
```

### Priority 5：Recognition Signal（认可信号）
**适用：** 被选中/晋升/额外委托，作为影响力间接证明
```
模板：Selected by [角色/级别] to [承担的额外职责]
示例：Selected by department chair to represent student body at annual CS advisory board meeting
```

### Priority 6：Comparative Frame（对比框架）
**适用：** 有前后状态对比，无绝对值
```
模板：Reduced [X] from [描述性状态A] to [描述性状态B]
示例：Reduced deployment process from multi-step manual configuration to single-command Docker setup
```

---

## §5 中→英本地化规则清单

### 结构规则
| 规则 | 说明 |
|------|------|
| R1：格式 | 美国投 Resume（Letter 纸，.docx/.pdf），英澳投 CV（A4） |
| R2：长度 | 应届/转专业：1 页（美），1–2 页（英），2–3 页（澳） |
| R3：时序 | 倒时序，最新经历在前 |
| R4：人称 | 无个人代词（不用 I / my / me），句子以动词开头 |
| R5：bullet 开头 | 每条以强动词开头（过去职位→过去时，当前→现在时） |
| R6：bullet 长度 | 单条不超过 2 行（约 30–40 words），超长→拆分为 2 条 |
| R7：每段经历数量 | 3–5 条 bullet；避免重复同一动词 |

### 内容规则
| 规则 | 说明 |
|------|------|
| R8：删除中式个人信息 | 见§8清单（照片/生日/性别/婚姻/政治面貌等） |
| R9：自我评价处理 | 删除或改写为 Professional Summary（成就导向，2–3 句） |
| R10：职务头衔本地化 | 按功能而非级别翻译（见§7） |
| R11：技术词汇保留 | Python/React/JWT 等技术名词不翻译，直接保留英文 |
| R12：高校名称 | 用官方英译，QS/THE Top 100 可加括号排名注（候选人确认） |
| R13：签证状态 | 不主动列出；有 OPT 且无需 sponsorship 时可在 header 注 |
| R14：GPA | 超过 3.5/4.0 可列；百分制需换算并注明"converted from 100-point scale"（换算由候选人提供，skill 不自动计算） |
| R15："References available upon request" | 删除，现代简历不需要 |

### 语言规则
| 规则 | 说明 |
|------|------|
| R16："负责…" | 禁用 "responsible for"；选准确动作动词（见§2） |
| R17：谦辞处理 | "参与/协助/配合"→核实实际贡献→选对应强动词（见§3） |
| R18：时态一致 | 过去职位用过去时，当前在读/在职用现在时 |
| R19：冠词/复数 | article（a/an/the）和名词复数是中文母语者最高频语法错误 |
| R20：中→英不加事实 | 翻译时不得添加原文未提及的数字、成就、技术 |

---

## §6 Chinglish / 直译陷阱对照表

### 通用岗位

| # | 错误（Chinglish/直译） | 正确（地道英文） | 问题类型 |
|---|----------------------|----------------|---------|
| 1 | Responsible for meeting records | Documented meeting minutes for weekly team sessions | 弱动词+直译 |
| 2 | Assisted the team to finish the project | Collaborated with a 4-engineer team to deliver the project 2 weeks ahead of schedule | 被动参与表述 |
| 3 | Vice Minister of Publicity Department | Associate Director of Communications, Student Union | 头衔直译夸大 |
| 4 | I have strong communication skills and hardworking spirit | （删除，改为具体成就支撑） | 第一人称+空洞套话 |
| 5 | Have 3 years working experience in software development | 3 years of software development experience | 冠词/格式 |
| 6 | Responsible for the management of 5 interns | Managed 5 interns, increasing team output by 30% | 名词化+弱动词 |
| 7 | Took part in the company summer internship program | Completed software engineering internship at [Company], developing [X] feature | "参加项目"无实质内容 |
| 8 | Good at Python and familiar with machine learning | Python (3 yrs); Machine Learning: PyTorch, Scikit-learn | 形容词描述替代技能列表 |
| 9 | Communist Youth League member | （删除，不写） | 政治信息不适合英文简历 |
| 10 | Excellent student of the year | Dean's List (Top 5% of class, 2022–2023) | 直译荣誉，无可信度 |
| 11 | Work hard and responsible | （删除，用具体成就替代） | 空洞品质词 |
| 12 | My main responsibility is to... | （去掉开头，直接用动词） | 中文思维句式 |
| 13 | Familiar with agile development | Practiced agile development using Jira in a 6-person Scrum team | "熟悉"不具说服力 |
| 14 | GPA: 88/100 | GPA: 3.7/4.0 (converted from 100-point scale) | 未换算/无换算说明 |

### 技术岗（CS / 软件工程）专项

| # | 错误（Chinglish/直译） | 正确（地道英文） | 问题类型 |
|---|----------------------|----------------|---------|
| T1 | Participated in developing user authentication module | Implemented JWT-based user authentication module, reducing login latency by 40ms | 谦辞保留 |
| T2 | Assisted in database query optimization | Optimized 15 PostgreSQL queries using indexing and EXPLAIN ANALYZE, cutting average query time from 800ms to 120ms | 协助+无技术细节 |
| T3 | Cooperated to finish frontend refactoring using React | Refactored frontend codebase from jQuery to React, improving component reusability and reducing bundle size by 22% | Chinglish 动词+无结果 |
| T4 | Responsible for developing user login module using Python and JWT | Implemented JWT-based user authentication module (Python/Flask), reducing average login latency by 35ms | 弱动词+技术罗列 |
| T5 | Used Python, TensorFlow, SQL to build model | Trained ResNet-50 image classification model on a 10,000-image dataset, achieving 92.3% validation accuracy; deployed via Flask REST API | 技术堆砌无结果 |
| T6 | Responsible for writing unit tests and improving code coverage | Wrote 200+ unit tests (pytest) for the payment service module, increasing code coverage from 43% to 87% | 弱动词+无量化 |
| T7 | Helped the backend team add new features to the API | Implemented 3 new REST endpoints for user notification preferences within a 6-person backend team | "Helped"+角色模糊 |

---

## §7 中式职责句式→地道英文动宾结构范例（中英对照）

### 通用岗位

**Case A — 活动策划**
| | |
|---|---|
| 中文原文 | 负责组织了5次大型校园活动，共吸引了800名参与者 |
| Chinglish 译 | Responsible for organizing 5 campus events with 800 participants |
| 地道英文 | Organized 5 large-scale campus events, attracting 800+ participants and achieving 95% positive feedback rating |

**Case B — 社媒运营**
| | |
|---|---|
| 中文原文 | 参与运营微信公众号，负责内容创作 |
| Chinglish 译 | Participated in WeChat official account operation, responsible for content creation |
| 地道英文 | Authored 30+ original articles for the department's WeChat Official Account (5,000+ subscribers), averaging 2,000 reads per post |

**Case C — 数据分析**
| | |
|---|---|
| 中文原文 | 协助完成了市场调研报告，收集了300份问卷 |
| Chinglish 译 | Assisted in completing market research report, collected 300 questionnaires |
| 地道英文 | Conducted market research by collecting and analyzing 300 survey responses; delivered findings that informed product pricing strategy for Q3 2023 |

**Case D — 会议记录（诚实低调版）**
| | |
|---|---|
| 中文原文 | 负责会议记录 |
| Chinglish 译 | Responsible for meeting minutes |
| 地道英文（仅记录） | Documented meeting minutes for weekly team meetings |
| 地道英文（整理+分发） | Compiled and distributed meeting minutes to 12 team members following each weekly sync |

---

### 技术岗（CS / 软件工程）

**Case E — 功能开发**
| | |
|---|---|
| 中文原文 | 负责开发了用户登录模块，使用了Python和JWT |
| Chinglish 译 | Responsible for developing user login module using Python and JWT |
| 地道英文 | Implemented JWT-based user authentication module (Python/Flask), reducing average login latency by 35ms and supporting 10,000+ concurrent sessions |

**Case F — 性能优化**
| | |
|---|---|
| 中文原文 | 参与优化了数据库查询，提升了系统性能 |
| Chinglish 译 | Participated in optimizing database queries and improving system performance |
| 地道英文 | Optimized 12 PostgreSQL queries using index tuning and EXPLAIN ANALYZE, cutting average API response time from 850ms to 180ms (79% improvement) |

**Case G — 前端重构**
| | |
|---|---|
| 中文原文 | 协助团队完成了前端页面重构，使用React |
| Chinglish 译 | Assisted team to finish frontend refactoring using React |
| 地道英文 | Refactored 8 legacy jQuery components into reusable React functional components, reducing codebase size by 3,200 lines and improving Lighthouse performance score from 62 to 91 |

**Case H — 测试/QA**
| | |
|---|---|
| 中文原文 | 负责编写单元测试，提高了代码覆盖率 |
| Chinglish 译 | Responsible for writing unit tests and improving code coverage |
| 地道英文 | Wrote 200+ unit tests (pytest) for the payment service module, increasing code coverage from 43% to 87% and catching 3 critical regression bugs before release |

**Case I — 机器学习**
| | |
|---|---|
| 中文原文 | 负责训练了图像分类模型，准确率达到了92% |
| Chinglish 译 | Responsible for training image classification model with 92% accuracy |
| 地道英文 | Trained ResNet-50 image classification model on a 10,000-image dataset, achieving 92.3% validation accuracy (baseline: 78%), deployed via Flask REST API |

**Case J — 团队项目（部分所有权）**
| | |
|---|---|
| 中文原文 | 参与了一个5人团队的电商平台开发，主要负责后端接口 |
| Chinglish 译 | Participated in a 5-person team to develop e-commerce platform, mainly responsible for backend API |
| 地道英文 | Developed RESTful backend APIs (Node.js/Express) for a 5-person e-commerce capstone project; implemented cart, order, and payment endpoints, handling 200+ test transactions |

**Case K — 实习边缘任务（诚实版）**
| | |
|---|---|
| 中文原文 | 协助整理项目文档和技术规范 |
| Chinglish 译 | Assisted in organizing project documents and technical specifications |
| 地道英文 | Compiled and standardized 15 technical specification documents, improving onboarding time for 3 new team members |

---

## §8 不该出现在英文简历里的中式元素清单

**适用范围：** 美国（商业岗）/ 英国 / 澳大利亚；欧洲（德/法/西等）规则不同，照片/生日通常要求保留。

| 中式元素 | 处理方式（美/英/澳） | 法规/惯例依据 |
|---------|-------------------|-------------|
| 个人照片 | 删除 | 美 EEOC / 英 Equality Act 2010 / 澳反歧视法 |
| 出生日期 / 年龄 | 删除 | 年龄歧视保护法（ADEA 美） |
| 性别 | 删除 | 隐私保护 |
| 婚姻状况 | 删除 | 无关招聘 |
| 民族 / 国籍（正文中） | 删除；联系信息只需姓名+邮件+电话 | EEOC 保护项 |
| 政治面貌（党员/团员） | 删除 | 西方雇主不理解，或产生负面联想 |
| 户籍 / 籍贯 | 删除 | 无意义 |
| 身份证号 | 删除 | 个人信息安全风险 |
| 健康状况 | 删除 | 残疾歧视保护（ADA 美） |
| 自我评价（主观品质段落） | 删除或改写为成就导向 Professional Summary（2–3 句） | 文化不对等 |
| "References available upon request" | 删除 | 现代规范不需要，浪费空间 |
| 全部在校课程列表 | 删除，保留 Relevant Coursework（仅与岗位直接相关） | 中学/通识课无意义 |
| 小学 / 初高中教育经历 | 删除，仅保留大学及以上 | 西方简历惯例 |
| 爱好兴趣（无关内容） | 删除，或替换为与岗位高度相关的具体活动 | 除非明确加分 |
| 第一人称代词（I / my / me） | 删除，句子直接以动词开头 | 英文简历约定俗成 |
| "主要职责是……" 开头句式 | 替换为动词开头 bullet | 中式思维残留 |

**学生干部头衔特别说明：**
- 部长 → Director of [Function]（功能性头衔，非级别）
- 副部长 → Associate Director of [Function]
- 学生会主席 → President, Student Government Association
- 干事/委员 → Coordinator 或 Content Coordinator
- 禁止用：Minister / Vice Minister（政府级别，夸大）/ Vice President（暗示大型组织高管，超出实际）

---

## Sources

| ID | 机构 + URL | 类型 |
|----|-----------|------|
| S01 | Google/Laszlo Bock via Inc.com — XYZ Formula https://www.inc.com/bill-murphy-jr/google-recruiters-say-these-5-resume-tips-including-x-y-z-formula-will-improve-your-odds-of-getting-hired-at-google.html | 原始方法论 |
| S02 | MIT CAPD — Resume Action Verbs https://capd.mit.edu/resources/resume-action-verbs/ | 官方高校职业中心 |
| S03 | MIT CAPD — Resumes: Writing About Skills https://capd.mit.edu/resources/resumes-writing-about-your-skills/ | 官方高校职业中心 |
| S04 | Harvard FAS Mignone Center — Create a Strong Resume https://careerservices.fas.harvard.edu/resources/create-a-strong-resume/ | 官方高校职业中心 |
| S05 | Harvard FAS — 45 Rare Action Verbs https://careerservices.fas.harvard.edu/blog/2025/08/14/45-rare-action-verbs-for-your-resume-with-examples/ | 官方高校职业中心 |
| S06 | BrightLink Prep — Harvard Action Verb List（derived from HBS, via third-party）https://brightlinkprep.com/harvard-resume-action-verbs/ | 第三方整理 |
| S07 | The Muse — Quantify Without Numbers https://www.themuse.com/advice/how-to-quantify-your-resume-bullets-when-you-dont-work-with-numbers | 权威求职媒体 |
| S08 | notchresume.com — Bullet Points Without Metrics https://notchresume.com/resources/resume-bullet-points.html | 专业简历平台 |
| S09 | CNS Career Services UT Austin — Strong Bullets for Technical Resumes https://careerservices.cns.utexas.edu/resources/resumes/strong-bullets-technical-resumes | 官方高校职业中心 |
| S10 | SWE Resume App — XYZ Method for Software Engineers https://www.sweresume.app/articles/xyz-method-resume/ | CS 专业简历平台 |
| S11 | resumeworded.com — Action Verbs https://resumeworded.com/action-verbs | 专业简历分析平台 |
| S12 | askcruit.com — Quantify Without Faking https://www.askcruit.com/resume/writing/quantify-resume-achievements | 专业简历平台 |
| S13 | Columbia Career Education — Creating Strong Bullet Points https://www.careereducation.columbia.edu/resources/resumes-impact-creating-strong-bullet-points | 官方高校职业中心 |
| S14 | ResumeCoach — Chinese Resume Guide https://www.resumecoach.com/chinese-resume/ | 专业简历平台 |
| S15 | CNBC — Action Verbs to Avoid https://www.cnbc.com/2023/05/02/action-verbs-to-avoid-using-on-your-resume.html | 主流媒体/职业专家 |
| S16 | ISOA — Format a US Resume as International Student https://www.isoa.org/blog/how-to-format-a-us-resume-and-cover-letter-as-an-international-student | 国际生组织 |
| S17 | TopResume — What Not to Include https://topresume.com/career-advice/6-things-to-remove-from-your-resume-right-away | 职业服务平台 |
| S18 | Resume.io — International CV Writing https://resume.io/blog/international-resume-cv-writing | 专业简历平台 |
| S19 | VisualCV — China CV Tips https://www.visualcv.com/international/china-cv/ | 专业平台 |
| S20 | Georgetown University Career Center — Immigration Status https://careercenter.georgetown.edu/diversity-career-resources/international-students/job-search-in-the-us/sharing-your-immigration-status/ | 官方高校职业中心 |
| S21 | TopCV — CV vs Resume Differences by Country 2026 https://www.topcv.io/blog/resume-vs-cv-differences-by-country-2026 | 职业平台 |
| S22 | Front Range Staffing — Why No Photo on Resume https://www.frontrangestaffing.com/2024/11/08/why-you-shouldnt-put-a-picture-or-personal-information-on-your-resume/ | 猎头机构 |
| S23 | Bluente — Decoding Chinese Business Titles https://www.bluente.com/blog/decoding-chinese-business-titles-the-ultimate-list-of-corporate-hierarchy-and-functional-roles | 翻译/本地化服务 |
| S24 | Quantum Tech Resumes — CAR for Tech Resumes https://www.quantumtechresumes.com/blog/car-challenge-action-results-for-tech-resumes | 技术岗简历机构 |
