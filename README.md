# CET-6 Writing Coach · 六级作文教练 Skill

> 给中国大学生用的英语六级（CET-6）作文教练，**冲 130+ 专用**。
> 不给"多读多写"的废话，针对你这一篇、这个水平给可落地修改。
> 一个可直接装进 [Claude Cowork](https://www.claude.com) 的 Skill。

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Skill](https://img.shields.io/badge/Claude-Skill-orange.svg)](#-安装)
[![Language](https://img.shields.io/badge/lang-中文-red.svg)](README.md)
[![English](https://img.shields.io/badge/lang-English-lightgrey.svg)](README.en.md)

---

## 🎯 这玩意是什么

一个面向**中国大学六级写作**的提示词 Skill。装进 Claude（Cowork / Claude Code）后，
当你提到"六级作文 / 批改 / 升级 / 虚拟语气 / 论证不深 / 思辨"等关键词时会自动激活，按真实阅卷流程给你回应。

**默认假设用户画像**：能写完 150–200 词，卡在 100 分上下（作文 8–10/15），通病是开头 Nowadays / 通篇 important / 论证空洞 / 中式英语。

## ✨ 能做什么

| 模式 | 触发场景 | 输出 |
|---|---|---|
| **批改打分** | 粘贴一段作文 | 印象分 + 四色标注（🔴🟡🟢🔵）+ 小幅修改版 + 冲分改写版 + 1 个最该练的弱点 |
| **审题立意** | 给了题目还没写 | 拆题 → 三个立意（⭐/⭐⭐/⭐⭐⭐）→ 用户选 → 三段式骨架 |
| **句式升级** | 一句平淡句 | 低 / 中 / 高三档对照 |
| **词汇替换** | "这个词怎么换" | 语域 + 搭配 + 场景，不是简单同义词 |
| **从零写一篇** | "帮我写一篇" | **先反问**让你自己写一稿，坚持后给带💡注释范文 |

**词句精雕六技**（v1.1 新增，批改时逐句过）：动词升维 / 形容词剥离 / 名词高阶搭配 / 长句信息打包 / 短句爆发 / 物称主语去人化。

**进阶武器库**（references/）：虚拟语气 / 倒装 / 独立主格 / 名词性从句 / 定语从句 / PEEL→PEEAL-CR / Toulmin 三角 / 12 种逻辑谬误 / 钢人论证 / 思辨四工具。

## 🚀 安装

### 方式一：Cowork 安装（推荐，傻瓜式）

1. 从 [Releases](../../releases) 下载 `cet6-writing-coach.skill`（或者直接下 zip 把后缀改成 `.skill`）
2. 在 Claude Cowork 中拖入聊天框
3. 点击「Save skill」按钮 ✅

### 方式二：Claude Code 手动安装

```bash
git clone https://github.com/<YOUR_USERNAME>/cet6-writing-coach.git
# 复制到 Claude Code 的 skills 目录
cp -r cet6-writing-coach ~/.claude/skills/
```

> Windows 用户路径：`%APPDATA%\Claude\local-agent-mode-sessions\skills-plugin\...\skills\`

### 方式三：自己改了再装

clone 下来改任何 `references/*.md`，再按方式一打包：

```bash
cd cet6-writing-coach
zip -r cet6-writing-coach.skill SKILL.md references/
```

## 💡 用法示例

### 例 1：粘段作文求批改

```
我：帮我看看这篇作文怎么样
   "Nowadays, with the rapid development of society, more and more
    people pay attention to mental health. It is very important..."

Claude（教练）：
印象分：8/15（六级折算 ~92 分）
🟡 "Nowadays, with the rapid development of" — 阅卷已避雷
🟡 "more and more people" → a growing number of
🟡 "very important" → pivotal / paramount
...
【小幅修改版】...
【冲分改写版】Mental health, once relegated to the periphery of public
discourse, now sits at the heart of...
最该练的弱点：去掉万能动词 important/people，换成物称主语开头。
```

### 例 2：句式升级

```
我：Reading is very important for us. 这句怎么升级
教练：
低（8）：Reading is very important for us.
中（11）：Reading plays an indispensable role in shaping our minds.
高（13+）：Few things rival reading in its capacity to broaden the
         mind and cultivate empathy.
```

完整示例见 [examples/01-essay-review.md](examples/01-essay-review.md)。

## 📁 文件结构

```
cet6-writing-coach/
├── SKILL.md                              # 主入口（7.4k 字符，含 5 模式 + 6 精雕技 + 按档发药）
├── references/                           # 弹药库（按需读，不全堆主文件）
│   ├── advanced-grammar-arsenal.md       # 虚拟/倒装/独立主格/分词/强调/抽象名词化
│   ├── noun-and-relative-clauses.md      # 名词性从句 + 定语从句（含 which 评注、of which）
│   ├── argumentation-depth.md            # PEEL→PEEAL-CR + Toulmin + 6 类深刻论据 + 5 主题论据库
│   ├── logic-and-critical-thinking.md    # 12 逻辑谬误 + 因果链 + 钢人 + 思辨四工具（13→14 分水岭）
│   ├── sentence-upgrade-bank.md          # 30 主题低→中→高三档句式
│   ├── high-frequency-word-replacement.md # 50 高频词精准替换 + 搭配
│   ├── scoring-rubric-and-models.md      # 评分细则 + 4 篇带注释 14 分范文
│   ├── openings-and-endings.md           # 8 开头 + 8 结尾真实范例
│   ├── connector-ladder.md               # 连接词梯度表
│   ├── topic-arsenal.md                  # 近 10 年真题主题 + 不撞车论据
│   └── chinglish-redlines.md             # 中式英语黑名单
├── examples/
│   └── 01-essay-review.md                # 真实批改示例（学生原文 → 教练完整回应）
├── README.md / README.en.md
├── LICENSE                               # MIT
├── CONTRIBUTING.md                       # 贡献指南
├── CHANGELOG.md
└── .github/
    ├── ISSUE_TEMPLATE/
    └── PULL_REQUEST_TEMPLATE.md
```

## 🛠 二次开发

最常见的几种改法：

| 想改什么 | 改哪个文件 |
|---|---|
| 触发关键词不够 | `SKILL.md` 的 `description:` 字段 |
| 加新的搭配 / 替换词 | `references/high-frequency-word-replacement.md` |
| 加新题目论据 | `references/topic-arsenal.md` |
| 加新句式 | `references/sentence-upgrade-bank.md` |
| 改批改风格（更狠/更温柔） | `SKILL.md` 模式 1 |

> ⚠️ `description` 字段有 1024 字符上限，加触发词时注意核 `wc -m`。

## 🤝 贡献

欢迎补论据库、改 bug、加新真题主题。详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

发现哪里"教练说得不对"或"这个例子翻译有问题"，直接开 issue 用 [bug 模板](.github/ISSUE_TEMPLATE/bug_report.md)。

## ❓ FAQ

**Q：四级作文能用吗？**
A：不能。评分维度不同。强行用会教你超档的句子（六级 13+ 的句子在四级反而扣分）。

**Q：考研/雅思/托福呢？**
A：同上，那些是别的训练。本 skill 限定六级 130+ 这条赛道。

**Q：会让我作文"很 AI"吗？**
A：不会。教练原则是"看到中式英语和万能模板就替换"，输出的是有节奏感、有思辨的人话；
但**最终建议你自己再过一遍**，把你不熟的句型替换掉，留下能驾驭的。

**Q：8 分用户能直接用 13 分的高级句吗？**
A：千万别。按档发药规则明确：与过去事实相反虚拟、倒装、抽象名词化对 8 分用户来说**用错比不用还扣分**。
教练会在批改时主动判档，给你够得着的那一档。

## 📜 License

[MIT](LICENSE) © 2026 Herry

随意用、随意改、随意分享，注明出处即可。
