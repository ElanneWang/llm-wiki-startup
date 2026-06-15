---
title: 操作日志
category: meta
created: 2026-06-14
updated: 2026-06-14
---

# 操作日志

按时间顺序记录 Wiki 的所有操作。

## 格式说明

每条记录以 `## [日期] 操作类型 | 描述` 开头，便于用命令行工具解析：

```bash
# 查看最近 5 条记录
grep "^## \\[" log.md | tail -5
```

---

## [2026-06-14] init | 初始化 LLM Wiki

- 创建目录结构
- 编写 AGENTS.md Schema
- 创建 index.md 和 log.md
- 创建 overview.md

---

## [2026-06-14] ingest | 播客：十字路口Crossing 对谈 Rolling AI

- **来源**: 小宇宙 https://www.xiaoyuzhoufm.com/episode/6a1e4022ac7bdb080c348b41
- **主题**: FDE（Forward Deployed Engineer）概念讨论
- **转录**: 使用 whisper base 模型，2005 个片段，检测语言 zh
- **创建页面**:
  - `wiki/sources/FDE播客-十字路口Crossing对谈Rolling AI.md`（源资料摘要）
  - `wiki/entities/Rolling AI.md`（实体页面）
  - `wiki/concepts/FDE-前置部署工程师.md`（概念页面）
  - `wiki/concepts/AI企业服务.md`（概念页面）
- **更新**: index.md

---

## [2026-06-14] update | 新增「案例」模块

- **新增目录**: `wiki/cases/`
- **更新 Schema**: AGENTS.md 增加 `cases` 分类和案例页面模板
- **更新工作流程**: 摄入流程新增「创建案例页」步骤
- **创建页面**:
  - `wiki/cases/乳品企业营养健康AI平台.md`
  - `wiki/cases/连锁奶茶门店智能体系统.md`
- **更新**: index.md

---

## [2026-06-15] update | 新增「个人思考」模块

- **新增目录**: `raw/thoughts/` 和 `wiki/thoughts/`
- **更新 Schema**: AGENTS.md 增加 `thoughts` 分类、模板和摄入流程
- **更新工作流程**: 新增「摄入个人思考」流程，与「摄入外部资料」分离
- **思考演化路径**: `raw/thoughts/` → `wiki/thoughts/` → `wiki/cases/`（实践验证后）
- **创建示例**:
  - `raw/thoughts/2026-06-15_FDE模式能否用于个人知识管理.md`（原始思考）
  - `wiki/thoughts/FDE模式能否用于个人知识管理.md`（结构化版本）
- **更新**: index.md, overview.md

---

*日志结束*
