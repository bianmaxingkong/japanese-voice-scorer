# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## What Goes Here

Things like:

- Camera names and locations
- SSH hosts and aliases
- Preferred voices for TTS
- Speaker/room names
- Device nicknames
- Anything environment-specific

## Examples

```markdown
### Cameras

- living-room → Main area, 180° wide angle
- front-door → Entrance, motion-triggered

### SSH

- home-server → 192.168.1.100, user: admin

### TTS

- Preferred voice: "Nova" (warm, slightly British)
- Default speaker: Kitchen HomePod
```

## Why Separate?

Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes, and share skills without leaking your infrastructure.

---

## 默认转写模型
**Whisper medium** — 火眼2026-06-03确认，以后所有日语语音转写任务默认使用 medium 模型，固定不切换。

## Canvas日语朗读批改规则

**统一使用**：本地技能 `canvas-japanese-reading-grading` 中的 `references/workflow.md`

**标准答案路径**：`./answer/{COURSE_ID}_{ASSIGNMENT_ID}_answer.txt`

**核心规则**：
- 基础分 **10.0**，公式：**10.0 - 累计扣分**
- 扣分上限 **3.0**，最低分 **7.0**
- 仅3类错误各扣 **-0.5**：严重发音错误 / 漏读多读整句 / 中途中断
- 同一错误类型全篇只扣一次
- 微小误差、转写存疑不扣分
- 必须执行**两轮批改**，取宽松结果
- 等级：优秀≥8.0（50%目标），良好7.0~7.9

## Canvas日语会话测试批改规则

**统一使用**：本地技能 `japanese-conversation-scorer` 中的 `references/workflow.md`

**核心规则**：
- 评分公式：总分 = 各题得分之和 ÷ 题目数（满分10分）
- 维度权重：内容准确性 80% / 语法正确性 10% / 发音清晰度 5% / 回答完整度 5%
- 等级：优秀≥8.0 / 良好6.0~7.9 / 合格4.0~5.9 / 需加强<4.0
- 转写失败 → 标记后转人工复核，不自动判低分
- 纠错按N5/N4/N3分级严格限定条数
- 评语无emoji，关联SKILL能力维度

### GitHub

Add whatever helps you do your job. This is your cheat sheet.
