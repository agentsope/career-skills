# weak-exp-transformations · 弱经历改写工具手册

**用途：** 运行时直接引用——把中文口语/杂乱经历编译成英文岗位语言 bullet。
本文件是 `career-experience-mapper` skill 的核心 before/after 范例库，配套改写公式与诚信护栏。
**红线：** 绝不编造雇主/职称/日期/数字/奖项/技能/URL；中→英不加事实；见 → `no-fabrication.md`
**能力词汇：** 以 NACE 8 大职业能力为主（Communication, Critical Thinking, Teamwork, Technology, Leadership, Professionalism, Career Management, Equity & Inclusion）。

---

## 目录

1. 弱经历分类体系
2. 改写公式（APR / XYZ / Scope-fallback）
3. Before/After 范例库 — 通用类（8 种）
4. Before/After 范例库 — CS 专项（6 种）
5. CS Overclaim 陷阱清单
6. 通用诚信护栏规则
7. Sources

---

## 1. 弱经历分类体系

"弱经历"并不意味着无价值，而是指「未经岗位语言转化的原始经历」。分类如下：

### 通用类

| 类别 ID | 中文描述 | 典型触发词 |
|---------|---------|-----------|
| `group_project` | 小组作业 | "我们小组做了……" / "是集体完成的" |
| `research_ppt` | 查资料 / 做 PPT | "帮老师查了文献" / "做了个汇报" |
| `academic_paper` | 课程论文 / 毕业论文 | "写了篇论文" / "毕设" |
| `club_organization` | 社团活动组织 | "学生会" / "社团负责人" / "办了个活动" |
| `volunteer_service` | 志愿服务 | "做过义工" / "志愿者" |
| `professor_assistance` | 帮老师整理资料 / 数据 | "帮导师录数据" / "整理文献" |
| `part_time_tutoring` | 兼职 / 家教 | "打工" / "给学生补课" |
| `competition_no_award` | 比赛未获奖 | "参加了但没拿奖" / "没进决赛" |

### CS 专项类

| 类别 ID | 中文描述 | 典型触发词 |
|---------|---------|-----------|
| `cs_replication` | 复现论文 / 教程项目 | "跟着教程做的" / "照着论文复现" |
| `cs_course_project` | 课程项目 | "课程作业" / "lab" / "学校项目" |
| `cs_kaggle_mid` | Kaggle 中游（无奖牌） | "排名前 40%" / "没有奖牌" |
| `cs_hackathon` | Hackathon 未获奖 | "24小时做的" / "没得奖" |
| `cs_oss_docs` | 文档 / 测试类开源贡献 | "改了文档" / "加了测试" |
| `cs_small_project` | 少 star 个人项目 | "只有几十个 star" / "自己用的工具" |

---

## 2. 改写公式

### APR 公式（通用首选）

```
[Action Verb] + [Project/Problem with context] + [Result/Impact]
```

- **Action**：精确动词，描述你个人实际控制的行为
- **Project/Problem**：做了什么 / 解决了什么问题，含规模上下文
- **Result**：量化结果；无法量化则用规模/背景指标

**示例：**
> Coordinated document organization for a 5-member project team, ensuring on-time submission of all deliverables over a 10-week semester.

来源：University of Arizona Career Center

---

### XYZ 公式（成果导向，Google 推荐格式）

```
Accomplished [X] as measured by [Y] by doing [Z]
```

- 强制"先写成果，再说方法"——倒置职责描述的惯性
- 若无法量化 X，用 "Supported [outcome] by doing [Z]"

**示例：**
> Improved dataset consistency (0 formatting errors across 500+ records) by entering and cross-validating survey data in Excel.

来源：Yale OCS "Writing Impactful Resume Bullets"

---

### Scope-fallback 公式（无量化结果时）

```
[Action Verb] + [Task] + [Scale indicator: for N people / over X weeks / across Y conditions]
```

- 当无法提供百分比或结果数字时，用规模/受众/时间窗口作为锚点
- 不得用估算替代真实数据（"大约200人" → "200+ attendees"，不可凭空发明数字）

**示例：**
> Delivered weekly math tutoring sessions to 6–8 elementary students over a 12-week volunteer program.

---

### 动词精度规则

| 场景 | 用这些动词 | 不用这些动词 |
|------|----------|------------|
| 团队成员（非组长） | Developed, Implemented, Contributed, Built | Led, Directed, Owned, Managed |
| 信息整理/文献 | Compiled, Synthesized, Reviewed, Organized | Authored, Wrote, Analyzed（除非确实做了分析） |
| 数据录入/清理 | Entered, Validated, Cleaned, Maintained | Analyzed, Processed（过大）|
| 复现 / 教程 | Implemented, Replicated, Reproduced, Explored | Built, Designed, Created（暗示原创）|
| 协作原型 | Prototyped, Contributed, Integrated | Shipped, Deployed, Released（暗示生产上线）|

---

## 3. Before/After 范例库 — 通用类

> 格式：中文原始口语 → 英文岗位语言 bullet → 可迁移技能标签（NACE 对应） → 诚信注意点

---

### 3.1 小组作业（group_project）

**场景 A：有技术贡献，非组长**

中文原始口语：
> 我们小组做了一个推荐算法，我负责写代码，老师给了 A。

英文岗位语言：
```
Collaborative Project | Introduction to Machine Learning, [University] | [Semester]
- Implemented collaborative filtering recommendation algorithm in Python (scikit-learn)
  within a 4-person team, achieving 87% prediction accuracy on held-out test set
- Documented model architecture and evaluation results in a 15-page technical report
  reviewed by course instructor
```

可迁移技能（NACE）：Technology · Critical Thinking · Teamwork · Communication

诚信注意点：
- 不是整个算法的唯一作者 → "Implemented [the filtering module]"，不写 "Built the recommendation system"
- 87% 精度数字仅在真实评估时写入；无数据则改 "achieving competitive accuracy on held-out test set"
- 不写 "Led" 除非确实是组长

---

**场景 B：主要做 PPT 和整理资料**

中文原始口语：
> 我在小组里主要做 PPT 和整理资料，感觉没什么技术含量。

英文岗位语言：
```
- Synthesized findings from 12+ research papers into a structured presentation,
  delivering key insights to an audience of 30 classmates and the course instructor
- Coordinated document organization and version control across a 5-member project team
  using Google Drive, ensuring on-time submission of all deliverables
```

可迁移技能（NACE）：Communication · Teamwork · Professionalism · Critical Thinking

诚信注意点：
- "整理资料" ≠ "做了全部研究"；Synthesize findings 和 Coordinate documents 是两个分开的动作
- "没技术含量"是主观误判——coordination 和 research synthesis 是真实职场可迁移技能
- 12+ 篇文献和 30 人受众须是真实估算；若数字不确定，改 "multiple research papers … a class audience"

---

### 3.2 查资料 / 做 PPT（research_ppt）

**场景 A：市场调研汇报**

中文原始口语：
> 老师让我查一些关于市场营销的文献然后做了个 PPT 汇报。

英文岗位语言：
```
- Conducted secondary market research reviewing 20+ industry reports and academic
  articles; synthesized findings into a 15-slide executive summary presented to class
- Applied competitive analysis framework to identify 3 key market trends, informing
  team's product positioning discussion
```

可迁移技能（NACE）：Critical Thinking · Communication · Technology

诚信注意点：
- "查资料做 PPT" 拆成两个 bullet（research + synthesize/present），两条比一条更有力
- 不要写 "Developed marketing strategy"——你做的是 research input，不是 strategy ownership
- 数字（20+ 篇、15 张幻灯片）须真实；若不确定，用 "several industry reports … a slide deck"

---

**场景 B：帮教授整理竞争对手信息**

中文原始口语：
> 我帮一个老师搜集了很多竞争对手的信息，做成表格。

英文岗位语言：
```
- Compiled competitive landscape database tracking 15 industry players across pricing,
  features, and market positioning using public filings and industry reports
- Organized data into structured Excel tables, enabling professor to identify market gaps
  for ongoing research project
```

可迁移技能（NACE）：Critical Thinking · Technology · Professionalism

诚信注意点：
- "搜集信息做表格" → Compiled + Organized，两个精确动词
- 如果教授实际用了你的数据，可写 "enabling [downstream use]"；不写 "contributed to the paper's conclusions" 除非确认
- 15 个竞争对手须是真实数量

---

### 3.3 课程论文 / 毕业论文（academic_paper）

**场景 A：课程论文**

中文原始口语：
> 写了一篇关于人工智能伦理的课程论文，大概 8000 字。

英文岗位语言：
```
- Authored 8,000-word research paper examining ethical implications of facial
  recognition technology in law enforcement contexts; analyzed 15+ peer-reviewed sources
- Developed argumentation framework evaluating tradeoffs between public safety and
  privacy rights, earning an A in Applied Ethics seminar
```

可迁移技能（NACE）：Critical Thinking · Communication · Career Management

诚信注意点：
- 字数和来源数量是真实可量化的，可以放心使用
- "earning an A" 仅在真实成绩时写入
- 不写 "Published" 除非确实在期刊 / 会议发表过

---

**场景 B：NLP 方向毕业论文**

中文原始口语：
> 大四写了毕业论文，研究的是 NLP 在客服自动化里的应用。

英文岗位语言：
```
Senior Thesis: Automated Customer Service Intent Classification Using NLP
- Fine-tuned pre-trained BERT model for text classification on 10,000+ labeled
  customer query records, achieving 91% intent classification accuracy
- Conducted comparative analysis of 4 transformer architectures, documenting
  performance trade-offs across precision, recall, and inference latency
- Presented findings to panel of 3 faculty reviewers; thesis received distinction
```

可迁移技能（NACE）：Technology · Critical Thinking · Communication

诚信注意点：
- 若模型基于开源框架，写 "fine-tuned pre-trained BERT model"，不写 "developed BERT from scratch"
- "received distinction" 仅在真实获得时使用
- 10,000+ 条数据须真实；91% 准确率须来自实验记录

---

### 3.4 社团活动组织（club_organization）

**场景 A：学生会文艺部组织晚会**

中文原始口语：
> 我是学生会文艺部的，组织过一次晚会，大概来了 200 人。

英文岗位语言：
```
Event Coordinator, Student Union Arts & Culture Department | [University] | [Dates]
- Planned and executed annual cultural gala attended by 200+ students and faculty,
  managing event logistics including venue booking, performer scheduling, and AV setup
- Coordinated a 10-member volunteer team across 3 planning phases (8 weeks pre-event),
  ensuring all deliverables completed on schedule
```

可迁移技能（NACE）：Leadership · Teamwork · Professionalism · Communication

诚信注意点：
- 如果 200 人是大约数，写 "200+"（加 "+" 是诚实写法）
- 如果你是执行负责人而非主席，用 "Coordinator" 或 "Lead Organizer"，不写 "Director"
- 10 人义工团队须是真实数字；若不确定，改 "a team of volunteers"

---

**场景 B：编程社团普通成员**

中文原始口语：
> 我是校内 Python 编程社团的成员，参与了几次活动。

英文岗位语言：
```
Member, Programming & Algorithms Society | [University] | [Dates]
- Participated in weekly coding workshops covering data structures and algorithm
  optimization; completed 3 competitive programming challenges per semester
- Collaborated with 20-member peer group on monthly technical project showcases
```

可迁移技能（NACE）：Technology · Teamwork · Career Management

诚信注意点：
- 只是普通成员（不是组织者）→ 诚实写 "Member"，不写 "Officer" 或 "Lead"
- 量化参与度（workshops 数量、challenges 数量）比泛泛"参与活动"更有锚点
- 20 人须真实，或改 "a peer group of approximately 20 members"

---

### 3.5 志愿服务（volunteer_service）

**场景 A：养老院数字助手**

中文原始口语：
> 我去养老院做过志愿者，陪老人聊天，帮他们用手机。

英文岗位语言：
```
Digital Literacy Volunteer | [Nursing Home Name] | [City] | [Dates]
- Provided one-on-one technology assistance to 10+ elderly residents weekly, teaching
  smartphone navigation, video calling, and app installation
- Demonstrated patient and adaptive communication to accommodate varying cognitive and
  physical abilities; completed 40+ volunteer hours over 3 months
```

可迁移技能（NACE）：Communication · Equity & Inclusion · Professionalism · Technology

诚信注意点：
- "帮用手机" → "Digital Literacy Volunteer / technology assistance"：精确职能描述，不是夸大
- 小时数是真实可量化指标；40 小时须真实，或改 "multiple volunteer hours over [duration]"
- "10+ 位老人"须是真实估计，若不确定改 "elderly residents"（无数字）

---

**场景 B：小学义教数学**

中文原始口语：
> 我去学校附近的小学做过义教，教小孩数学。

英文岗位语言：
```
Math Tutor Volunteer | [Elementary School Name] | [Dates]
- Delivered weekly small-group math tutoring sessions to 6–8 students (grades 3–5),
  adapting lesson content to individual learning levels
- Tracked student progress over 12-week program; several students demonstrated
  measurable improvement in arithmetic per teacher feedback
```

可迁移技能（NACE）：Communication · Equity & Inclusion · Critical Thinking · Professionalism

诚信注意点：
- "5 of 6 students improved" 仅在有教师反馈或成绩记录时使用；否则用 "several students demonstrated noticeable improvement per teacher feedback"
- 不虚构具体百分比改善；无数据时去掉数字，只引用教师反馈
- 12 周须真实

---

### 3.6 帮老师整理资料 / 数据（professor_assistance）

**场景 A：实验数据录入**

中文原始口语：
> 我帮一个老师整理实验数据，输入到 Excel 里，就是很简单的录入工作。

英文岗位语言：
```
Research Assistant (Volunteer) | Prof. [Last Name], [Dept.], [University] | [Dates]
- Entered and validated 500+ experimental data records in Excel, cross-checking for
  inconsistencies to ensure dataset integrity for downstream statistical analysis
- Maintained organized file structure for raw data files across 4 experimental conditions
```

可迁移技能（NACE）：Technology · Professionalism · Critical Thinking

诚信注意点：
- "很简单的录入工作" 是自我贬低——data validation 是真实价值；任何后续分析都依赖数据准确性
- 不要写 "Analyzed data"——你做的是录入和验证，边界要清晰
- 500+ 条和 4 个实验条件须真实；若不确定，改 "hundreds of experimental records across multiple conditions"

---

**场景 B：文献搜集整理**

中文原始口语：
> 帮老师找过一些参考文献，整理成了一个文档。

英文岗位语言：
```
- Conducted systematic literature search using Google Scholar and PubMed, identifying
  25 relevant peer-reviewed articles on [topic area] for professor's ongoing research
- Compiled annotated bibliography in APA format, summarizing methodology and key
  findings of each source
```

可迁移技能（NACE）：Critical Thinking · Communication · Technology

诚信注意点：
- "找文献" ≠ "写综述"；若没有撰写分析，用 "compiled and summarized"，不用 "authored literature review"
- 标注数据库名（PubMed, Google Scholar）增加专业度，无需夸大
- 25 篇须真实数量；若不确定，改 "peer-reviewed articles on [topic]"（无具体数字）

---

### 3.7 兼职 / 家教（part_time_tutoring）

**场景 A：奶茶店收银员（目标 CS / 分析类岗位）**

中文原始口语：
> 我在奶茶店打工过，当收银员，半年。

英文岗位语言：
```
Cashier | [Store Name] | [City] | [Dates]
- Processed 100+ customer transactions daily with zero cash discrepancy over
  6-month tenure, demonstrating accuracy under high-volume conditions
- Trained 2 new hires on POS system and store procedures, reducing onboarding
  time by approximately 2 days
```

可迁移技能（NACE）：Professionalism · Teamwork · Technology

诚信注意点：
- "零误差" 仅在确实如此时使用；若偶有误差，删去该描述
- 不要强行将收银工作技术化为"数据分析"；诚实展示 operational skills 即可
- "100+ 笔" 须是真实估算；"减少约 2 天入职时间" 是合理估算，面试时应能解释依据
- 若简历空间有限且有更强经历，可以省略本段

---

**场景 B：数学物理家教**

中文原始口语：
> 我做过家教，帮高中生补数学和物理，大概每周 3 小时。

英文岗位语言：
```
Private Tutor (Mathematics & Physics) | Self-Employed | [Dates]
- Provided weekly 3-hour individualized tutoring sessions to 2 high school students
  preparing for college entrance examinations
- Designed customized practice problem sets targeting each student's specific knowledge
  gaps; both students achieved passing scores in targeted subjects
- Managed scheduling, billing, and parent communication independently
```

可迁移技能（NACE）：Communication · Critical Thinking · Career Management · Professionalism

诚信注意点：
- "both students achieved passing scores" 仅在有具体成绩支撑时使用
- "Self-Employed" 是合法头衔；也可写 "Independent Contractor" 或 "Freelance Tutor"
- 如果只教过 1 个学生，写 "a high school student"，不改成复数

---

### 3.8 比赛未获奖（competition_no_award）

**场景 A：校级数据分析比赛**

中文原始口语：
> 参加过一个校级数据分析比赛，没拿奖，感觉没意义写。

英文岗位语言（Projects 区）：
```
Campus Data Analytics Challenge | Python, Pandas, Seaborn | [Month Year]
- Analyzed 10,000-row e-commerce sales dataset to identify seasonal purchasing
  patterns and high-value customer segments using clustering techniques
- Developed 3 visualization dashboards using Seaborn and Matplotlib; presented
  findings to panel of 5 faculty and industry judges
- Implemented data cleaning pipeline reducing missing value rate from 18% to 0.3%
```

可迁移技能（NACE）：Critical Thinking · Technology · Communication

诚信注意点：
- 不提名次，除非进入 Top 3 / 决赛（"Finalist" 可写；"未获奖"不写）
- 技术细节（数据集规模、缺失值率）须真实可验证
- 参与经历本身有价值，不必因没得奖而省略

---

**场景 B：ACM 校内选拔未通过**

中文原始口语：
> 参加过 ACM 校内选拔，没有通过。

英文岗位语言：
```
ACM Programming Contest Participant | [University] | [Date]
- Competed in competitive programming selection covering dynamic programming,
  graph algorithms, and optimization problems
- Solved 3 of 5 contest problems within 3-hour time limit, demonstrating
  proficiency in algorithmic problem-solving under time pressure
```

可迁移技能（NACE）：Critical Thinking · Technology · Professionalism

诚信注意点：
- "solved 3 of 5 problems" 是诚实量化，既展示能力也不夸大
- 不写 "competed nationally" 如果只是校内选拔
- 不写获奖或晋级，不提排名

---

## 4. Before/After 范例库 — CS 专项

---

### 4.1 复现论文 / 教程项目（cs_replication）

中文原始口语：
> 跟着 Hugging Face 官方教程做了一个情感分析模型，用的 SST-2 数据集。

**Before（错误写法）：**
> Built a BERT-based sentiment analysis system achieving 93% accuracy on SST-2.

**After（诚实可信写法）：**
```
- Implemented BERT fine-tuning pipeline for sentiment classification (SST-2) using
  Hugging Face Transformers; explored effect of learning rate decay schedules,
  achieving 93.1% validation accuracy consistent with published baseline
```

可迁移技能（NACE）：Technology · Critical Thinking

诚信注意点：
- 使用动词 "implemented / replicated / explored" 替代 "built / designed / created"
- 标注数据集来源（SST-2 公开数据集）
- 写清楚"与 baseline 的对比关系"而非绝对声称
- 若额外做了学习率对比实验，可单独说明；若只是原样跑通，去掉 "explored" 部分

---

**扩展范例：ResNet 复现**

中文原始口语：
> 照着论文和 GitHub repo 复现了 ResNet，在 CIFAR-10 上训练，accuracy 达到 92%。

**Before：** Built a deep learning image classification system achieving 92% accuracy.

**After：**
```
- Replicated ResNet-18 architecture (He et al., 2016) in PyTorch; trained on
  CIFAR-10 achieving 92.3% test accuracy, matching reported baseline; profiled
  training bottlenecks and reduced epoch time by 15% via mixed-precision training
```

诚信注意点：标明"复现"性质（Replicated）、论文来源、框架、数据集，以及自己做的一个真实延伸动作（mixed-precision）。

---

### 4.2 课程项目（cs_course_project）

中文原始口语：
> MIT 6.824 风格的课程作业，实现了简版 Raft，用 Go 写，3 人小组，通过了全部测试。

**Before（模糊版）：** Implemented distributed consensus algorithm in a team project.

**After（有深度版）：**
```
Raft Consensus Implementation | Distributed Systems Course | [University] | [Semester]
- Implemented Raft consensus algorithm in Go; designed leader election, log
  replication, and fault-tolerance mechanisms within a 3-person team
- Passed all 100 test cases including network partition scenarios, validated
  against course autograder
```

可迁移技能（NACE）：Technology · Critical Thinking · Teamwork

诚信注意点：
- "100 test cases" 须真实；若数量不确定，写 "all course-provided test cases including network partition scenarios"
- 用标题行标注 "Distributed Systems Course"——透明度是加分项，不是减分项
- 标明团队规模（3 人）

---

### 4.3 Kaggle 中游成绩（cs_kaggle_mid）

中文原始口语：
> 参加了 Kaggle 房价预测竞赛，1200 支队伍中排名约 480，前 40%，用了 XGBoost + 特征工程。

**Before（自欺版）：** Participated in Kaggle competition and achieved competitive results.

**After（有说服力版）：**
```
Kaggle House Prices: Advanced Regression Techniques | Python, XGBoost | [Date]
- Built XGBoost + Ridge stacking pipeline with feature engineering (log transform,
  interaction terms, missing value imputation); achieved RMSE 0.118 on public LB
- Ranked ~480 / 1,200+ teams; documented approach in shared Kaggle notebook
```

可迁移技能（NACE）：Technology · Critical Thinking · Career Management

诚信注意点：
- 诚实标注排名（480 / 1200），但以 RMSE 等模型指标作为主要量化点，排名不作主角
- 不写 "competitive result" 而不说明具体排名——模糊信息引起更多追问
- 附 Kaggle notebook 链接增加可信度

---

### 4.4 Hackathon 未获奖（cs_hackathon）

中文原始口语：
> 参加了一个学校 hackathon，4 人团队，24 小时，做了一个心理健康 AI 聊天机器人，有基本 demo，未得奖。

**Before（过度包装）：** Built an AI mental health chatbot at [Hackathon], leveraging cutting-edge LLM technology.

**After（诚实可信）：**
```
[University Hackathon 2024] | Python, Flask, React | 24 hrs
- Contributed Flask backend and REST API integration in a 4-person team; integrated
  OpenAI GPT-4 API with LangChain for context retention
- Developed user onboarding flow and preference-matching UI; prototype demoed
  to 50+ attendees during final presentations
```

可迁移技能（NACE）：Technology · Teamwork · Communication

诚信注意点：
- 标注时间限制（24 hrs）体现快速交付能力
- 用 "prototype / demo" 替代 "system / platform"；未部署就不是 "deployed product"
- 只写你个人负责的模块（Flask backend + API），不写 "I built" 整个项目
- "demoed to 50+ attendees" 须真实估计

---

### 4.5 文档 / 测试类开源贡献（cs_oss_docs）

中文原始口语：
> 给一个有 5k+ star 的 Python 工具库提交了 3 个 PR，都是文档改进：修正了 2 处 API 描述错误，添加了缺失参数说明，写了一个 Getting Started 示例。

**Before（低估）：** Fixed some documentation in an open source project.

**Before（夸大）：** Core contributor to [Project], improving documentation for 5k+ user community.

**After（诚实得当）：**
```
Open Source Contributor | [ProjectName] (Python; 5k+ GitHub stars)
- Contributed 3 merged PRs: corrected 2 API specification errors in official docs,
  added missing parameter documentation for fit() method, and authored
  Getting Started tutorial to reduce onboarding friction for new users
```

可迁移技能（NACE）：Communication · Technology · Professionalism

诚信注意点：
- 精确数量（3 merged PRs）；具体说明每个 PR 做了什么，不笼统
- 项目规模（5k stars）仅作背景，不作个人成就
- 不写 "core contributor"——非 core maintainer 不使用
- "reducing onboarding friction" 描述文档价值，无需凭空量化具体用户数

---

### 4.6 少 star 个人项目（cs_small_project）

中文原始口语：
> 用 Python 写了一个本地批量图片压缩脚本工具，有 CLI，GitHub 上 35 star，平时自己用。

**Before（自我否定）：** Made a small Python script for image compression (not widely used).

**Before（夸大）：** Built an open source image optimization tool with 35+ GitHub stars.

**After（有专业感）：**
```
imgcrush — Python CLI Image Compression Tool | Python, Pillow | [Date]
- Developed CLI tool for lossless/lossy batch image compression using Pillow and
  mozjpeg; implemented concurrent processing (ThreadPoolExecutor) achieving
  ~3x throughput vs sequential baseline on local benchmark
- Includes configurable quality presets and Bash-completable argument parsing;
  tested with pytest (90%+ coverage) and GitHub Actions CI
```

可迁移技能（NACE）：Technology · Critical Thinking · Career Management

诚信注意点：
- 完全不提 star 数；用技术选型和性能数字（~3x）替代规模指标
- "~3x throughput" 属于合理估算范畴，面试中需能解释测试方法（"本地基准，顺序 vs 并发对比"）
- 代码质量信号（pytest 90% coverage）体现工程规范

---

## 5. CS Overclaim 陷阱清单

以下是 CS 背景候选人最常见的 overclaim 模式。面试官和工程师能识别这些写法；遇到即在 deep-dive 中暴露。

| 陷阱表达（X，不要写） | 应改为（Y） | 原因 |
|---------------------|-----------|------|
| "Built a production-grade system" | "Built a working prototype of X" / "Developed a local deployment of X" | 未上线就不是 production；会被追问部署/监控/SLA |
| "Scalable architecture" | 省略，或 "designed with horizontal scaling in mind (not yet load-tested)" | 无实际负载数据不能声称 scalable |
| "Led the development of X" | "Contributed [frontend module] in a 3-person team" | 非正式小组合作不能称 led；追问时无法说清各人贡献 |
| "Implemented state-of-the-art model" | "Replicated [paper name] (CVPR 2023) achieving X% accuracy on [dataset]" | SOTA 须有论文引用和数据支撑 |
| "Developed X from scratch" | "Implemented X using [framework] with custom modifications to [component]" | from scratch 暗示无任何外部依赖，几乎不成立 |
| "Handled millions of requests" | 省略，或 "load-tested to 1,000 RPS on local setup" | 无实际流量数据不能声称 |
| "Full-stack developer"（无佐证） | 在 bullet 里展示前后端各自的具体贡献 | 声明须有项目验证 |
| "Expert in X"（skills section） | "X (proficient)" 或直接在项目里展示 | Expert 级别引发高难度面试问题 |
| 教程项目不标注来源，直接写 "Built" | "Followed [Course/Tutorial] and extended with [my addition]" | 面试追问时必须能诚实解释来源 |
| "Open source project with 40+ stars" 作为成就 | 省略 star 数，聚焦技术细节 | Star 数不是有意义的 impact 指标 |
| "Competitive result" 不说明具体排名 | 直接写排名 + 主要模型指标 | 模糊信息引起更多追问；被动解释更尴尬 |
| "Cutting-edge technology" | 具体列出框架/模型名称 | 空洞修饰词，对有经验的面试官是减分项 |

---

## 6. 通用诚信护栏规则

> 红线参考：`no-fabrication.md`（本文件任何规则与 R03 冲突时，以 R03 为准）

### 规则 G1 — 动词主语只覆盖你个人控制的范围

- 你亲手做的 → 用第一人称隐含动词："Developed / Implemented / Analyzed"
- 团队整体效果 → 明确区分："Team achieved Y; I owned [my module]"
- 禁止用 "Led / Directed / Managed" 描述你参与但不领导的工作

### 规则 G2 — 无数字时用规模描述，不发明数字

优先级顺序（当大数字不可得时）：

1. 性能对比（~X% faster vs sequential baseline，须能解释测试方法）
2. 测试覆盖率（85%+ unit test coverage）
3. CI/CD 时间（reduced build time from 4 min to 90 sec）
4. 代码规模（migrated X KLOC）
5. 协作规模（collaborated with X engineers / in a N-person team）
6. 展示受众（demoed to X attendees / presented to class of 30）
7. 时间周期（over 12-week program / across 3 experimental conditions）

**禁止：** 凭空估算百分比（"提升了 40%"但实际无数据支撑）

### 规则 G3 — 自授头衔须描述真实职能

- 合法：Research Assistant (Volunteer) / Event Coordinator / Freelance Tutor
- 合法：UC Berkeley 明确：志愿经历可直接以职能命名，无须标注 "volunteer"
- 禁止：课程项目 → "Lead Engineer" / "Software Architect"
- 禁止：普通社团成员 → "President" / "Director"（除非确实担任该职）
- 原则：头衔描述的职能必须与你实际负责的工作范围相符

### 规则 G4 — 比赛未获奖放 Projects，不提名次

- 放位置：Projects / Technical Competitions 区块，不放 Awards / Honors
- 可写："Finalist, [比赛名]"（若确实进入决赛）
- 不写：排名、未获奖名次、"honorable mention"（若无实际颁发）
- 聚焦：技术实现、数据规模、方法论、评审受众

### 规则 G5 — 中→英不加事实

- 中文原始表述是信息边界：英文输出只能精确化表达，不能添加不存在的经历、数字、或成果
- 改写动词是允许的（"帮老师整理数据" → "Entered and validated experimental data"）
- 添加事实是禁止的（"帮老师整理数据" → "Analyzed experimental data and drew conclusions"）

### 规则 G6 — 证据不足时使用保守动词

| 情境 | 保守动词（用这个） | 激进动词（避免这个） |
|------|----------------|----------------|
| 没有明确成果数据 | Contributed to / Supported | Led / Drove / Achieved |
| 工具是教程来的 | Implemented / Replicated | Designed / Built |
| 团队成果我参与 | Collaborated on / Assisted with | Delivered / Shipped |
| 数据是估算的 | ~X / approximately X | X（确定数字的形式）|

---

## 7. Sources

以下 URL 均来源于 R05 和 R06 研究报告，均为真实可访问链接（研究时间：2026-05-26）。

**大学 Career Center（最高权威度）**

- Harvard FAS Mignone Career Center, "No Work Experience? Here's What to Highlight Instead" — https://careerservices.fas.harvard.edu/blog/2025/09/10/no-work-experience-heres-what-to-highlight-instead/
- Yale Office of Career Strategy, "Writing Impactful Resume Bullets" — https://ocs.yale.edu/resources/writing-impactful-resume-bullets/
- MIT CAPD, "Resumes: Writing About Your Skills" — https://capd.mit.edu/resources/resumes-writing-about-your-skills/
- MIT CAPD Resume Toolkit — https://capd.mit.edu/resources/career-toolkit-crafting-an-effective-resume/
- University of Arizona Career Center, "APR Format" — https://career.arizona.edu/resources/write-impressive-bullet-points-using-apr-format/
- Columbia Career Education, "Resumes with Impact" — https://www.careereducation.columbia.edu/resources/resumes-impact-creating-strong-bullet-points
- UC Berkeley Career Engagement, Resumes — https://career.berkeley.edu/prepare-for-success/resumes/
- Tufts University Career Center, "Hackathon on Resume" — https://careers.tufts.edu/blog/2024/10/28/how-to-include-hackathons-on-your-resume/
- Binghamton University Career Tools, Research Experience — https://careertools.binghamton.edu/resources/how-to-add-research-experience-to-your-resume-or-cv/
- UT Austin CNS Career Services, Strong Bullets for Technical Resumes — https://careerservices.cns.utexas.edu/resources/resumes/strong-bullets-technical-resumes
- Penn West Career Blog, Projects on Resume — https://career.pennwest.edu/blog/2022/08/10/how-and-when-to-include-projects-on-your-resume-plus-examples/
- University of Missouri Career Center — https://career.missouri.edu/career-scoop/how-to-get-your-first-internship-with-no-relevant-experience/

**诚信 / 背调权威来源**

- Penn State Ethicist, "Embellishing Resume" — https://www.psu.edu/news/impact/story/ask-ethicist-embellishing-resume
- John W. Mitchell, Resume Integrity Guide — https://johnwmitchell.com/integrity-on-your-resume-can-you-stretch-the-truth/

**职场 / 行业资源**

- freeCodeCamp, "Writing a Killer SWE Resume" — https://www.freecodecamp.org/news/writing-a-killer-software-engineering-resume-b11c91ef699d/
- opensource.com, "Add Open Source to Your Resume" — https://opensource.com/business/16/2/add-open-source-to-your-resume
- story.cv, "Metrics in Resume" — https://story.cv/blog/articles/metrics-in-resume
- Extern / NACE Competencies Guide — https://www.extern.com/post/career-readiness-competencies-guide
- interviewkickstart.com, "List Projects on SWE Resume" — https://interviewkickstart.com/blogs/articles/list-projects-on-software-engineer-resume
- Kaggle Q&A, "How to Present Kaggle on Resume" — https://www.kaggle.com/questions-and-answers/363750
- Adithya Solai Medium, "Golden Resume Rules for CS Majors" — https://adithyasolai.medium.com/golden-resume-rules-for-cs-majors-af2f591d6457
- formation.dev, "Ex-Meta Recruiter SWE Resume Guide" — https://formation.dev/blog/software-engineer-resume-guide-examples/
- Medium InterviewingSoftwareEngineers, "Project Deepdives" — https://medium.com/interviewingsoftwareengineers/project-deepdives-tips-for-interview-3dd5399ee854
- Teal HQ, XYZ Resume Formula — https://www.tealhq.com/post/xyz-resume
- Novoresume Career Blog — https://novoresume.com/career-blog/resume-advice-for-students-with-no-experience
