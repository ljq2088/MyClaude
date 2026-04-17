---
name: zotero-scholar
description: 讨论学术问题时通过 Zotero MCP 实时检索相关文献。
user-invocable: true
---

# Zotero Scholar

## 触发条件
讨论物理/数学问题时，涉及具体概念、方程或结果，主动查询 Zotero 文献库。

## 工作流
1. 识别核心概念（Teukolsky、GSF、NIT、FEW 等）
2. 用 Zotero MCP 工具搜索相关文献
3. 提取：标题、作者、年份、关键结论
4. 引用格式：`作者 (年份) — 核心结论`

## 注意
- 优先搜索最相关的 2-3 篇，不堆砌
- 若有 abstractNote，提取关键方程或数值结果
- Zotero 桌面客户端需运行（本地模式，端口 23119）
