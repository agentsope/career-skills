# 能力模型提取 · competency-extraction

把 JD 的要求映射成**结构化能力模型**。关键:用**与 `career-experience-mapper` 同一套词汇**(NACE 8 + O*NET + 硬技能),这样 mapper 能直接拿这份模型去对齐用户的经历,整条链才咬得上。

---

## 1. 三层输出

把 Step 2 的清单转成:

- **required 硬能力 / 门槛**:学历、专业、年限、必须硬技能(SQL、CAD、CPA…)。→ 决定"能不能投"。
- **preferred 加分**:优先项。→ 有则前置,无则忽略。
- **competencies 软能力**:映射到统一能力词汇(见下),标核心 / 次要。→ 决定"简历里强调哪些可迁移能力"。

外加 **keywords**(freq×position 加权,见 `jd-anatomy.md`)。

---

## 2. 统一能力词汇(与 mapper 对齐)

软能力一律映射到这套词(NACE 8 为骨架),不要自创同义词:

| 能力(统一词) | JD 里常见的说法 |
|---|---|
| 批判性思维 / 分析 | 逻辑清晰、数据分析、解决问题、独立思考 |
| 沟通 | 沟通能力强、表达清晰、对接、汇报 |
| 团队协作 | 团队精神、跨部门协作、配合 |
| 领导力 | 带团队、统筹、推动、owner 意识 |
| 专业/技术 | 具体硬技能(SQL/Python/设计…) |
| 学习能力 | 学习能力强、快速上手、适应 |
| 职业素养 | 责任心、抗压、细心、主动 |
| 数字/技术应用 | 工具熟练、数据敏感、技术栈 |

> 硬技能(SQL/Python/Axure…)单独列在 required/preferred,不要塞进软能力。

---

## 3. 标核心 vs 次要

- 在 freq×position 上高权重的能力 = **核心**(简历必须正面命中)。
- 偶尔出现的 = **次要**(能体现则加分)。

---

## 4. 输出给下游(handoff 字段)

```
required:     [...]   # 硬门槛
preferred:    [...]   # 加分
competencies: [统一词(核心/次要), ...]
keywords:     [...]   # 原词, 加权排序
```

- 喂 **experience-mapper**:用 competencies 对齐用户经历(强/弱匹配)。
- 喂 **resume-tailor**:用 keywords + required 做取舍和关键词对齐。
- 喂 **gap-planner**:用 required - 用户已有 = 差距。

> 全部只来自**真实 JD**;JD 没写的能力不要"脑补补全"。
