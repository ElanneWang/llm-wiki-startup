---
title: Wiki 总览
category: synthesis
created: 2026-06-14
updated: 2026-06-14
tags: [meta, guide]
---

# LLM Wiki 总览

## 这是什么？

这是一个基于 Karpathy LLM Wiki 模式的个人知识库。核心理念是：

> **让 LLM 逐步构建并维护一个持久的、结构化的 Wiki，而不是每次提问都重新从原始资料中检索。**

## 快速开始

### 1. 添加资料

将文章、论文、笔记等放入 `raw/` 目录的对应子文件夹：

```
raw/
├── articles/    # 网络文章
├── papers/      # 学术论文
├── books/       # 书籍章节
├── podcasts/    # 播客（音频 + 转录文本）
├── videos/      # 视频（视频 + 转录文本）
└── assets/      # 图片等附件
```

然后告诉我：**"请摄入 [文件名]"**

### 2. 提问查询

直接向我提问，我会：
1. 查阅 Wiki 中的相关页面
2. 综合已有知识回答你
3. 如有价值，询问是否将回答保存为新页面

### 3. 定期整理

告诉我：**"请整理 Wiki"**

我会检查：
- 页面间是否有矛盾
- 是否有孤立页面
- 是否需要更新交叉引用
- 是否有缺失的重要概念

## 目录结构

```
llm-wiki/
├── AGENTS.md          # Schema 配置（LLM 行为指南）
├── raw/               # 原始资料（只读）
└── wiki/              # LLM 维护的 Wiki
    ├── index.md       # 内容目录
    ├── log.md         # 操作日志
    ├── overview.md    # 本文件
    ├── sources/       # 源资料摘要
    ├── entities/      # 实体页面
    ├── concepts/      # 概念页面
    ├── cases/         # 案例（场景 + 解决方案 + 结果）
    └── synthesis/     # 综合分析
```

## 使用 Obsidian（推荐）

1. 用 Obsidian 打开 `llm-wiki` 文件夹作为 Vault
2. 安装以下插件增强体验：
   - **Graph View** —— 查看页面关联图谱
   - **Dataview** —— 基于 YAML 元数据动态查询
   - **Marp** —— 从 Wiki 生成幻灯片
3. 使用 Obsidian Web Clipper 浏览器插件快速保存网页文章

## 核心原则

- **原始资料不可变** —— LLM 只读取，不修改
- **Wiki 是复利资产** —— 每次摄入都在积累，不是从零开始
- **人机协作** —— 你负责审阅和提问，LLM 负责维护
- **探索即生产** —— 有价值的查询结果可以回存到 Wiki
- **案例即资产** —— 具体场景+解决方案+结果，是最可复用的知识

## 相关页面

- [[index]] —— 内容目录
- [[log]] —— 操作日志

## 引用来源

- [Karpathy's LLM Wiki Gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)
- [Chubby Skills - 播客转录](https://github.com/chubbyguan/chubbyskills/tree/main/podcast-transcribe)
