---
name: rts-content
description: |
  Create trading education content from Rayner Teo knowledge-base materials with default IMA grounding. Use when the user asks for content ideas, YouTube scripts, short-video hooks, article outlines, newsletter drafts, course modules, study notes, summary cards, or repurposing price action, trend trading, breakout, support/resistance, risk management, or trading psychology topics. Default IMA knowledge base: "Rayner Teo 知识库". Triggers include $rts-content, 内容创作, 选题, 脚本, 文章, 短视频, 课程提纲, 笔记, and 资料整理.
---

# rts-content

Create educational trading content from source-grounded Rayner Teo themes.

## Default IMA Knowledge Base

Use `Rayner Teo 知识库` unless the user explicitly names another knowledge base.

## Workflow

1. Clarify audience level and content format if missing.
2. Retrieve IMA materials for specific source-backed claims, examples, or episode/video references.
3. Convert the topic into an educational angle:
   - misconception
   - framework
   - checklist
   - case review
   - practice drill
4. Add trading-risk disclaimers naturally when the content could be read as advice.
5. Avoid copying Rayner Teo's wording or imitating his persona.

## Output Format

```markdown
## 内容目标
## 选题列表
| 选题 | 角度 | 适合格式 | 需要检索的资料 |
## 推荐脚本/大纲
## 风险边界
## 下一步
```

## Quality Bar

- Do not quote source material unless retrieval actually happened and quoting is necessary.
- Keep content educational, not signal-selling.
- Preserve copyright boundaries by summarizing and transforming, not reproducing original scripts.
