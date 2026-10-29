---
name: rts-psychology
description: |
  Diagnose trading psychology and execution-discipline problems through Rayner Teo style trading-process frameworks with default IMA knowledge-base grounding. Use when the user mentions overtrading, revenge trading, fear of missing out, fear of loss, moving stops, cutting winners early, holding losers, drawdowns, inconsistent execution, quitting trading, full-time trading expectations, or confidence after losses. Default IMA knowledge base: "RaynerTeo交易知识库 | 顺势而为". Triggers include $rts-psychology, 交易心理, 纪律, 过度交易, 报复性交易, 扛单, 提前离场, 连续亏损, and 情绪交易.
---

## 手动更新路由

用户明确要求“更新 skill / 检查更新 / 同步最新原子库”时，先执行此路由。使用当前 SKILL.md 所在目录解析脚本绝对路径：

```text
python "{skillDir}/tools/update_skill.py"
```

只检查时加 `--check`。脚本从 GitHub main 的固定提交同步本仓库整套 skill 和原子资料，覆盖前备份，写入失败回滚；不需要 Git 或 GitHub 登录。根据脚本实际结果报告当前提交、更新状态与失败原因。普通业务问题不自动更新。更新后重新读取相关 SKILL.md。


# rts-psychology

Turn emotional trading problems into process changes and review rules.

## Default IMA Knowledge Base

Use `RaynerTeo交易知识库 | 顺势而为` unless the user explicitly names another knowledge base.

## Workflow

1. Identify the failure pattern: before trade, during trade, after loss, after win, or during drawdown.
2. Separate skill gap, system gap, and discipline gap.
3. Use IMA for source-grounded Rayner Teo material when specific claims are needed.
4. Convert the diagnosis into:
   - trigger signs
   - prevention rules
   - emergency stop rules
   - journal prompts
   - weekly review metrics
5. Suggest a small practice protocol.

## Output Format

```markdown
## 问题类型
## 可能根因
## 流程修复
| 场景 | 触发信号 | 规则 | 复盘指标 |
## 本周练习
## 风险提醒
```

## Quality Bar

- Do not provide mental health diagnosis.
- Do not shame the user for losses.
- Prefer concrete behavior rules over motivational advice.
- Keep finance boundary clear.
