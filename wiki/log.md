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

## [2026-06-15] ingest | 视频：YC 访谈 Bob McGrew 谈 FDE 方法论

- **来源**: B站 https://www.bilibili.com/video/BV1X6YNzKEhw
- **原始来源**: YouTube YC https://www.youtube.com/watch?v=Zyw-YA0k3xo
- **嘉宾**: Bob McGrew（OpenAI 前首席研究官，Palantir FDE 模式架构师）
- **备注**: B站 412 反爬限制无法下载音频，通过网页文章获取内容
- **创建页面**:
  - `raw/videos/YC访谈-AI创业必看的FDE方法论.md`（原始资料）
  - `wiki/sources/YC访谈-Bob McGrew谈FDE方法论.md`（源资料摘要）
- **更新页面**:
  - `wiki/concepts/FDE-前置部署工程师.md`（大幅更新：新增 Echo/Delta 结构、与咨询区别、商业模式、KPI）
- **更新**: index.md

---

## [2026-06-17] ingest | 文章：Notion CEO Ivan Zhao - Steam, Steel, and Infinite Minds

- **来源**: Notion 博客 https://www.notion.com/blog/steam-steel-and-infinite-minds-ai
- **作者**: Ivan Zhao（Notion 联合创始人兼 CEO）
- **主题**: AI 作为知识工作的"奇迹材料"，三个历史隐喻（钢铁、蒸汽机、城市）
- **创建页面**:
  - `raw/articles/Steam-Steel-and-Infinite-Minds.md`（原始资料）
  - `wiki/sources/Notion-IvanZhao-Steam-Steel-Infinite-Minds.md`（源资料摘要）
  - `wiki/concepts/AI-Agent-知识工作的未来.md`（概念页面）
- **深度挖掘后新增**:
  - `wiki/concepts/技术转变的普遍模式.md` —— McLuhan 的后视镜理论
  - `wiki/concepts/上下文碎片化与可验证性.md` —— AI Agent 两大障碍
  - `wiki/concepts/无限心智的管理者.md` —— 从执行者到编排者
  - `wiki/cases/Notion-700-Agent实践.md` —— Notion 内部 Agent 部署案例
- **更新**: index.md

---

## [2026-06-21] ingest | 播客：硅谷101 E240 - OpenAI联手PE，聊聊硅谷最火新职位FDE

- **来源**: 小宇宙 硅谷101 https://www.xiaoyuzhoufm.com/episode/6a333603351c82c12b264c56
- **嘉宾**: Jove（Cresta FDE 负责人）、Oliver（Invisible Technologies VP，前麦肯锡）
- **主题**: FDE 团队构建（FDPM/FDE 双角色）、人才画像、方法论、PE 合作
- **创建页面**:
  - `wiki/sources/硅谷101-E240-FDE-OpenAI-PE.md`（源资料摘要）
  - `wiki/cases/Cresta-FDE团队实践.md`（案例页）
- **更新页面**:
  - `wiki/concepts/FDE-前置部署工程师.md`（大幅更新：新增 FDPM 角色、人才画像、工作节奏、PE 参与）
- **更新**: index.md

---

## [2026-06-21] ingest | 视频：YC - How to Build an AI-Native Services Company

- **来源**: YouTube https://www.youtube.com/watch?v=gSNFJbgoaHI
- **嘉宾**: Charlie Warren（YC Visiting Partner）
- **主题**: AI 原生服务公司构建方法论（Service-as-a-Software、Sam Altman 测试、选市场、定价、P&L）
- **备注**: YouTube SSL 连接失败，通过 noembed API + 网页文章获取内容
- **创建页面**:
  - `raw/videos/YC-How-to-Build-AI-Native-Services-Company.md`（原始资料）
  - `wiki/sources/YC-如何构建AI原生服务公司.md`（源资料摘要）
- **更新页面**:
  - `wiki/concepts/AI企业服务.md`（新增 Service-as-a-Software、Sam Altman 测试、目标市场特征、风险陷阱）
- **更新**: index.md

---

## [2026-06-26] ingest | 文章：腾讯云AI产业应用大会-康师傅全域数字化转型

- **来源**: 用户提供的新闻稿
- **事件**: 2026腾讯云AI产业应用大会，腾讯云+康师傅+晶确科技战略合作签约
- **主题**: 快消行业全域数字化转型，六大行业智能体场景
- **创建页面**:
  - `raw/articles/腾讯云康师傅晶确科技-AI产业应用大会.md`（原始资料）
  - `wiki/sources/腾讯云AI产业应用大会-康师傅全域数字化转型.md`（源资料摘要）
  - `wiki/cases/康师傅全域数字化转型.md`（案例页，重点关注六大场景解决方案）
- **更新**: index.md

---

## [2026-06-26] ingest | 文章：晶确科技与腾讯千域计划深度合作

- **来源**: 用户提供的文章
- **主题**: 晶确科技"内脑"定位、GTM/PMF方法论、三层AI智能体矩阵、腾讯"被集成"战略
- **创建页面**:
  - `raw/articles/晶确科技GAIA-腾讯千域计划合作深度解读.md`（原始资料）
  - `wiki/sources/晶确科技与腾讯千域计划-快消数据驱动与AI智能体落地.md`（源资料摘要）
  - `wiki/entities/晶确科技GAIA.md`（实体页）
- **更新页面**:
  - `wiki/cases/康师傅全域数字化转型.md`（补充晶确科技智能体矩阵细节、GTM/PMF方法论、ADP平台信息）
- **更新**: index.md

---

*日志结束*
