---
name: rts-learning-map
description: |
  Build Rayner Teo trading learning paths with default IMA knowledge-base grounding. Use when the user asks where to start, how to learn price action, trend trading, support/resistance, breakout trading, candlestick patterns, indicators, risk management, trading psychology, or how to turn the Rayner Teo knowledge base into a staged curriculum. Default IMA knowledge base: "RaynerTeo交易知识库 | 顺势而为". Triggers include $rts-learning-map, 学习地图, 学习路径, 系统学习, 先学什么, 入门, 价格行为学习, and 交易学习计划.
---

## 手动更新路由

用户明确要求“更新 skill / 检查更新 / 同步最新原子库”时，先执行此路由。使用当前 SKILL.md 所在目录解析脚本绝对路径：

```text
python "{skillDir}/tools/update_skill.py"
```

只检查时加 `--check`。脚本从 GitHub main 的固定提交同步本仓库整套 skill 和原子资料，覆盖前备份，写入失败回滚；不需要 Git 或 GitHub 登录。根据脚本实际结果报告当前提交、更新状态与失败原因。普通业务问题不自动更新。更新后重新读取相关 SKILL.md。


# rts-learning-map

Create a structured learning path for Rayner Teo trading materials.

## Default IMA Knowledge Base

Use `RaynerTeo交易知识库 | 顺势而为` unless the user explicitly names another knowledge base.

## Workflow

1. Clarify the user's current level, market type, timeframe, and goal if missing.
2. Use IMA retrieval for source-grounded topic lists, lesson names, or quote-level claims.
3. Organize learning into stages:
   - market environment and trend/range recognition
   - price action and support/resistance
   - entries, stops, targets, and trade management
   - risk management and position sizing
   - psychology, journaling, and review
   - strategy testing and iteration
4. For each stage, specify the learning output: notes, checklist, chart examples, backtest sheet, or review log.
5. End with the next 3 actions the user should take.

## Output Format

```markdown
## 学习目标
## 默认知识库
## 阶段路线
| 阶段 | 主题 | 要解决的问题 | 产出 |
## 推荐检索词
## 练习任务
## 下一步
```

## Quality Bar

- Do not promise trading results.
- Do not give live trade recommendations.
- Separate beginner, intermediate, and advanced paths when relevant.
- Prefer practice outputs over passive reading lists.
