# rtskill

Rayner Teo 风格价格行为、趋势交易与交易系统学习 Skill 工具箱。

`rtskill` 是一组面向 Agent 的 workflow skills，用来基于 IMA 知识库学习 Rayner Teo 交易教育资料，整理趋势、价格行为、支撑阻力、突破、风控、交易心理与交易系统，并把资料转成可执行的学习路径、策略研究、交易计划和复盘清单。

适用于 Codex、Claude Code、Cursor、Trae Solo 等支持 skill / system prompt 工作流的 Agent。

---

## 安装

发布后，可以用下面的命令安装整套 skills：

```bash
npx -y skills add FocusLiz-Lab/rtskill -g --all
```

安装后可以直接使用：

```text
$rts 我想系统学习 Rayner Teo 的价格行为和趋势交易，先从哪里开始？
```

也可以手动复制或导入 `skills/` 目录下的 skill 文件夹：

```text
skills/
├── rts/
├── rts-learning-map/
├── rts-strategy/
├── rts-trading-plan/
├── rts-review/
├── rts-psychology/
├── rts-content/
└── rts-ima/
```

---

## IMA 配置

整套 workflow skills 默认读取这个 IMA 知识库：

```text
Rayner Teo 知识库
```

用户不需要在每次提问时输入知识库名称。如果想使用其他 IMA 知识库，在问题里直接写知识库名称即可。

## 加入 / 访问知识库

扫描下面的二维码，加入或访问对应知识库：

![知识库二维码](docs/knowledge-base-qrcode.png)

### 安装 IMA Skill

```text
请安装 ima 技能
下载地址：https://app-dl.ima.qq.com/skills/ima-skills-1.1.7.zip
API Key 获取：https://ima.qq.com/agent-interface
```

使用前需要满足：

- 已安装官方 `ima-skill`
- 已配置 IMA `Client ID` 和 `API Key`
- 当前 IMA 账号有权限访问目标知识库

本仓库不包含、也不会保存任何 IMA API Key。

---

## 工具箱

| Skill | 用途 |
|---|---|
| `$rts` | 主入口。根据用户问题自动路由到合适的 Rayner Teo workflow。 |
| `$rts-learning-map` | 学习地图：价格行为、趋势、支撑阻力、突破、风控、心理的学习顺序。 |
| `$rts-strategy` | 策略研究：整理交易理念、入场/出场、市场环境、失效条件和回测假设。 |
| `$rts-trading-plan` | 交易计划：把方法论转成可执行计划、检查清单和复盘指标。 |
| `$rts-review` | 案例复盘：评审交易想法、图表截图、交易日志或策略方案。 |
| `$rts-psychology` | 交易心理：纪律、风险、亏损、过度交易和执行偏差诊断。 |
| `$rts-content` | 内容系统：把知识库资料转成文章、短视频、脚本、课程提纲或学习笔记。 |
| `$rts-ima` | IMA 检索入口：搜索、阅读、引用或排查 IMA。 |

---

## 常见路径

### 从入门到执行

```text
rts-learning-map
    ↓
rts-strategy
    ↓
rts-trading-plan
```

### 从交易记录到改进

```text
rts-review
    ↓
rts-psychology
    ↓
rts-trading-plan
```

### 从资料整理到内容发布

```text
rts-ima
    ↓
rts-strategy
    ↓
rts-content
```

---

## 使用示例

```text
$rts-learning-map 系统学习这个知识库，先看哪些？
```

```text
$rts-strategy 整理 Rayner Teo 关于趋势交易和突破交易的核心框架。
```

```text
$rts-trading-plan 把支撑阻力和价格行为方法转成一份交易前检查清单。
```

```text
$rts-review 帮我复盘这笔交易：入场、止损、目标、执行问题分别看哪里？
```

```text
$rts-content 围绕知识库里的核心主题，生成 10 个内容选题。
```

---

## 知识库 / 原子库

本仓库包含一个发布安全的抽象原子库：

```text
知识库/原子库/atoms.jsonl
```

它用于保存 Rayner Teo workflow 的方法论单元，不包含原始转录稿、X/Twitter 原文、PDF、书籍正文或付费材料。涉及具体原文、出处、日期和图表示例时，仍应优先使用 IMA 知识库检索。

---

## 资料边界

本仓库只包含 skill instructions、workflow 抽象、知识库索引和二维码。

本仓库不包含 Rayner Teo 的原始 YouTube 转录稿、X/Twitter 归档、PDF 书籍、私有资料文件夹或任何受版权保护的原始资料库。

这些 skills 会在运行时从用户自己的 IMA 知识库检索资料。用户需要自行确保有权上传和使用自己的资料。

交易相关输出仅用于教育、研究和流程整理，不构成投资建议、买卖建议、收益承诺或个性化金融建议。任何交易决策和风险后果由用户自行承担。

请不要提交：

- IMA API Key
- 私有资料文件
- 原始 PDF、转录稿、视频或归档
- 个人环境配置
- 任何未经授权的第三方内容

---

## 许可证

本项目默认采用 CC BY-NC 4.0 许可证，除非后续另行添加其他许可证。

许可证只覆盖本仓库原创的 skill instructions 和 workflow 抽象，不授权任何第三方原始资料。
