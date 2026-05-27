# 安装指南 / Installation

`career-skills` 的每个 skill 是一个**自包含文件夹**(`skills/career-*`,内含 `SKILL.md` + `references/` + `examples/`)。下面任一方式都会把整个文件夹带上;**别只拷 `SKILL.md`**,否则会丢掉 `references/` 里的方法论,功能静默失效。

> 先装好 [Claude Code](https://docs.claude.com/en/docs/claude-code)。把下文 `agentsope` 换成你实际的 GitHub 用户名 / 组织名。

---

## 方式 A — npx 一行装(推荐)

最快。装哪个 skill 就跑哪行:

```bash
npx skills add agentsope/career-skills/skills/career-experience-mapper   # 经历→简历(灵魂)
npx skills add agentsope/career-skills/skills/career-bullet-builder       # 磨简历 bullet
npx skills add agentsope/career-skills/skills/career-resume-tailor        # 组装可投递简历
npx skills add agentsope/career-skills/skills/career-jd-analyzer          # 拆 JD
npx skills add agentsope/career-skills/skills/career-gap-planner          # 算差距 / 补什么
npx skills add agentsope/career-skills/skills/career-role-finder          # 找真实在招
```

`skills` CLI 来自 [skills.sh](https://skills.sh),会把整个 skill 文件夹装好。

---

## 方式 B — Claude Code 插件市场(一次装整包)

想 6 个一起装、跟随仓库更新:

```
/plugin marketplace add https://github.com/agentsope/career-skills
/plugin install career-skills
```

---

## 方式 C — 手动 copy

```bash
git clone https://github.com/agentsope/career-skills.git
cp -R career-skills/skills/career-experience-mapper ~/.claude/skills/   # 换成你要的 skill
```

> ⚠️ 一定是 `cp -R 整个文件夹`;只复制 `SKILL.md` 会丢 `references/`。`git pull` 后重拷即可更新。

---

## 方式 D — 其他 agent / 便携使用

整个 skill 文件夹就是个便携 prompt bundle:把 `skills/career-*/` 整体喂给任何支持长上下文的 agent,`SKILL.md` 是入口,`references/` 按需展开。

---

## 验证安装

随便给一段口语经历测一下,例如:

> 我没实习,课上做过一个社会企业的小组作业,我负责财务和风险分析。想投项目助理,这能写进简历吗?

`career-experience-mapper` 应触发,先给一句判断 + 中文草表达 + 一句补强,再问你要不要展开 / 要英文版。

---

*中文优先(国内求职),英文按需。把 `agentsope` 换成你的 GitHub 用户名 / 组织名。*
