# Handoff Contract · 跨-skill 接口契约

> career-skills pack 里每个 skill 都是链条的一环。本契约定义它们之间**怎么交接数据**,让整条链
> (role-finder → gap-planner → jd-analyzer → experience-mapper → bullet-builder → resume-tailor → interview-*)
> 真正咬合,而不是各写各的、拼不起来。
>
> **Single source of truth.** 改这里 → 把各 skill 的 `## Handoff` 段落对齐 → commit。

---

## 1. 原则 / Principles

1. **每个 skill 声明 `consumes` 和 `produces`。** 上游的 `produces` 必须等于下游的 `consumes`。
2. **数据以结构化交接块流转**,而非自由散文。核心字段名固定(见 §3),skill 可加自有字段,但不得改核心字段名。
3. **格式是 markdown 标签块,不是严格 JSON。** prompt 驱动的 skill 产出 markdown 更稳;字段名足够规整,需要时也能机器抽取。
4. **红线随块流转(铁律)。** `gaps` 与 `integrity_flags` 必须原样带到下游;任何下游 skill **绝不可**用编造的数字 / 事实去填 `gaps`,只能 (a) 用保守写法,或 (b) 回问用户。这是 `no-fabrication.md` 红线的跨-skill 延伸。

---

## 2. 交接块格式 / Block format

每个"工作单元"(一段经历 / 一条 bullet / 一个岗位 / 一道面试题)产出一个块:

```yaml
### ⇄ Handoff · <from-skill> → <to-skill>
- unit_id: E1                       # 稳定 id,下游可引用
- context: <真实语境,诚信锚点>
- <核心字段,见 §3>
- gaps: [<待补充 / 待确认>]          # 下游不得编造填充
- integrity_flags: [<已标注的诚信事项>]
```

---

## 3. 核心字段字典 / Field dictionary

| 字段 | 含义 | 主要由谁产出 |
|---|---|---|
| `unit_id` | 工作单元稳定标识(E1 / B1 / JD1 …) | 任意 |
| `context` | 真实语境(团队规模 / 课程 / 实习 / 志愿 / 复现性质…)—— 诚信锚点 | mapper |
| `raw_facts` | M1 拆解出的事实清单,供下游重组(不止改写句子) | mapper |
| `competencies` | 能力 + 强度,如 `Critical Thinking(strong)` | mapper |
| `target_role` / `relevance` | 目标岗位 + 相关性(strong / weak / none / generic) | mapper · jd-analyzer |
| `draft_expression_en` | 草表达(探索性,**非成品**) | mapper |
| `zh_reasoning` | 中文思路(可选) | mapper |
| `formula` | PAR / XYZ / CAR | mapper → bullet-builder |
| `evidence_strength` | strong / weak —— 决定下游动词档位 | mapper |
| `final_bullets` | 成品 bullet(可多变体,可直接粘) | bullet-builder |
| `ats_keywords` | 该 bullet 命中的关键词 | bullet-builder |
| `gaps` | 待补充 / 待确认项 —— **下游禁止编造填充** | 任意,向下累积 |
| `integrity_flags` | 已标注的诚信事项(团队 / 课程 / 复现…) | 任意,向下累积 |

> skill 可按需扩展字段(如 jd-analyzer 的 `required_competencies`、interview-* 的 `question_type`),
> 但 §3 的核心字段名全 pack 统一,不得各起各的名。

---

## 4. 链路交接图 / Who produces what

```
jd-analyzer ──required_competencies──┐
                                     ▼
raw experience ─► experience-mapper ─handoff(competencies / draft / formula / gaps / flags)─► bullet-builder
                          │                                                                       │ final_bullets
                          │ competencies / raw_facts                                              ▼
                          ▼                                                                  resume-tailor ─► 整份投递简历
                  interview-stories (STAR)
```

**当前已实现:** `experience-mapper`(producer)。其余为 roadmap。
新建每个 skill 时,在其 `SKILL.md` 写一个 `## Handoff` 段,`consumes` / `produces` 对齐本契约。

---

## 5. 版本 / Versioning

v0.1 · 2026-05 · 随 pack 演进。任何破坏性字段变更,必须同步更新所有已存在 skill 的 `## Handoff` 段。
