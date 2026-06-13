# 贡献指南

感谢愿意贡献 ✨

本项目是一个 Claude Skill，**核心都是 Markdown**，不需要写代码、不需要环境，
你只要会写中文/英文就能贡献。

## 你能贡献什么

### 🟢 最欢迎（5 分钟就能 PR）

- **新的搭配 / 替换词**：补到 `references/high-frequency-word-replacement.md`
- **新真题主题论据**：补到 `references/topic-arsenal.md`
- **发现了一个 Chinglish 没收录**：加到 `references/chinglish-redlines.md`
- **某个例句翻译不地道**：直接修

### 🟡 中等（半小时）

- 新增一个**高分主题模板**：在 `sentence-upgrade-bank.md` 加一组"低→中→高"
- 新增**开头/结尾真实范例**：到 `openings-and-endings.md`
- 修复一个**逻辑谬误举例**：在 `logic-and-critical-thinking.md`

### 🔴 重型（讨论后再做）

- 改 `SKILL.md` 的模式判断逻辑
- 改"按档发药"规则
- 改 description 字段（容易破坏触发）

> 🔴 改 `SKILL.md` 前请先开 issue 讨论，避免做完被 reject。

## 流程

```bash
# 1. fork + clone
git clone https://github.com/你的名/cet6-writing-coach.git
cd cet6-writing-coach

# 2. 建分支
git checkout -b add-collocation-X

# 3. 改 → 自测（装回 Claude 试一遍）
zip -r test.skill SKILL.md references/

# 4. 提交
git commit -m "feat(reference): 补充 surge/wave/torrent of 高阶搭配"
git push origin add-collocation-X

# 5. 开 PR
```

## Commit 规范（建议）

按 conventional commits 简化：

- `feat(reference): ...` — 加新内容到 references/
- `feat(skill): ...` — 改 SKILL.md 主入口
- `fix: ...` — 修错例 / 错搭配 / typo
- `docs: ...` — 改 README / CONTRIBUTING
- `chore: ...` — 杂项

## 自测清单

PR 前请确认：

- [ ] `wc -m SKILL.md` < 8000（如果改了主文件）
- [ ] description 字段 < 1024 字符
- [ ] 新增的英文例句**自己读着不别扭**（不是 Google 翻译腔）
- [ ] 不与现有内容冲突 / 重复
- [ ] 中文部分**不混进繁体**

## 不被接受的贡献

- 把六级 skill 改成"通用英语写作 skill"——本项目刻意限定六级 130+ 这一条赛道
- 加入与官方阅卷标准冲突的"独家秘技"（除非给得出阅卷组背书）
- 把对照例改成"看起来高级但实际有错"的句子（语法错是硬伤，宁缺毋滥）

## 行为准则

直言不讳没问题，**对事不对人**就行。
