---
name: rts-review
description: |
  Review trading ideas, chart screenshots, trade journals, and strategy drafts using Rayner Teo style price-action and risk-management frameworks with default IMA knowledge-base grounding. Use when the user asks to critique a setup, review an entry/stop/target, diagnose a failed trade, improve a trading plan, or evaluate a chart-based thesis. Default IMA knowledge base: "RaynerTeo交易知识库 | 顺势而为". Triggers include $rts-review, 交易复盘, 图表复盘, 点评交易, 策略评审, 入场, 止损, 目标, and 交易日志.
---

## 手动更新路由

用户明确要求“更新 skill / 检查更新 / 同步最新原子库”时，先执行此路由。使用当前 SKILL.md 所在目录解析脚本绝对路径：

```text
python "{skillDir}/tools/update_skill.py"
```

只检查时加 `--check`。脚本从 GitHub main 的固定提交同步本仓库整套 skill 和原子资料，覆盖前备份，写入失败回滚；不需要 Git 或 GitHub 登录。根据脚本实际结果报告当前提交、更新状态与失败原因。普通业务问题不自动更新。更新后重新读取相关 SKILL.md。


# rts-review

Review user-provided trading material using a structured, education-only process.

## Default IMA Knowledge Base

Use `RaynerTeo交易知识库 | 顺势而为` unless the user explicitly names another knowledge base.

## Required Inputs

Ask for missing details only when they materially affect the review:

- instrument and timeframe
- entry, stop, target, and reason for trade
- market condition at entry
- risk amount and trade management rules
- chart screenshot or journal text if available

## Workflow

1. Restate the user's setup without adding assumptions.
2. Check market environment, level quality, trigger, stop, target, and risk.
3. Separate strategy design issues from execution discipline issues.
4. Use IMA for Rayner Teo-specific source references if the user asks for source grounding.
5. Return a repair checklist.

## Output Format

```markdown
## 复盘结论
## 结构检查
| 项目 | 观察 | 风险 | 修改建议 |
## 策略问题 vs 执行问题
## 下次交易前检查
## 需要补充的信息
```

## Quality Bar

- Do not say the user should have bought or sold.
- Do not judge outcome quality only by profit/loss.
- Highlight missing risk rules before discussing entries.
