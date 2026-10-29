---
name: rts-trading-plan
description: |
  Convert Rayner Teo style trading concepts into executable trading plans, checklists, journaling templates, and practice roadmaps with default IMA knowledge-base grounding. Use when the user asks for pre-trade plans, risk management, position sizing process, stop-loss rules, trade journal fields, backtest plans, 7/30/90-day practice plans, or workflow implementation. Default IMA knowledge base: "RaynerTeo交易知识库 | 顺势而为". Triggers include $rts-trading-plan, 交易计划, 检查清单, 风控计划, 复盘表, 日志, 回测, 模拟盘, and 执行流程.
---

## 手动更新路由

用户明确要求“更新 skill / 检查更新 / 同步最新原子库”时，先执行此路由。使用当前 SKILL.md 所在目录解析脚本绝对路径：

```text
python "{skillDir}/tools/update_skill.py"
```

只检查时加 `--check`。脚本从 GitHub main 的固定提交同步本仓库整套 skill 和原子资料，覆盖前备份，写入失败回滚；不需要 Git 或 GitHub 登录。根据脚本实际结果报告当前提交、更新状态与失败原因。普通业务问题不自动更新。更新后重新读取相关 SKILL.md。


# rts-trading-plan

Convert trading education into a practical execution and review plan.

## Default IMA Knowledge Base

Use `RaynerTeo交易知识库 | 顺势而为` unless the user explicitly names another knowledge base.

## Workflow

1. Determine the user's goal: learning, paper trading, backtesting, journaling, or live-process design.
2. Ground source-specific rules through IMA when needed.
3. Build a plan with:
   - market and timeframe scope
   - setup checklist
   - entry/stop/target rules
   - risk cap and loss limits
   - trade management rules
   - no-trade conditions
   - journal fields
   - review cadence and metrics
4. Include a "stop doing" list for common execution errors.
5. Provide a short implementation schedule.

## Output Format

```markdown
## 目标
## 交易前检查
## 执行规则
## 风险规则
## 复盘字段
## 7/30/90 天练习安排
## 禁止事项
```

## Quality Bar

- Do not choose live trades for the user.
- Use percentages, R-multiples, or placeholders only as templates unless the user provides their own rules.
- Make the checklist short enough to use before a trade.
