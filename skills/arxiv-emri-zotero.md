# SKILL: arxiv-emri-zotero

每天自动搜索最新 EMRI 波形相关 arxiv 文章，展示给用户选择后写入 Zotero。

## 工作流

1. 每天 07:03 自动触发搜索，展示新文章列表（含摘要、分类建议）
2. 用户选择要导入的文章编号
3. 执行导入，文章写入 Zotero 对应集合

## 手动命令

```bash
# 搜索并展示新文章
python C:/Users/12511/arxiv_to_zotero.py search

# 导入选定文章（按编号）
python C:/Users/12511/arxiv_to_zotero.py import 0 1 3

# 导入全部
python C:/Users/12511/arxiv_to_zotero.py import all
```

## 文件位置

- 脚本：`C:\Users\12511\arxiv_to_zotero.py`
- 待导入缓存：`C:\Users\12511\Zotero\arxiv_pending.json`

## 自动分类规则

默认写入：`EMRI波形计算前沿 (K8UTAXUY)` + `未读 (3P3QAFWV)`

关键词额外分类：

| 关键词 | 集合 |
|--------|------|
| Teukolsky, Sasaki-Nakamura | T92IL7H7 Teukolsky |
| gravitational self-force | WQMGPIF6 self-force |
| FastEMRIWaveforms, FEW model | G2UUMSR2 FastEMRI |
| augmented analytic kludge | DQR76H8B AAK |
| numerical kludge | GGP7C68Q NK |
| effective one body, EOB | HMK64UK3 EOB |
| non-Kerr, beyond Kerr | CG8GMDMC non-Kerr |
| dark matter EMRI, accretion disk EMRI | ZZWAFH47 环境 |
| neutron star EMRI | LTHE6PZ5 中子星EMRI |
| surrogate model/waveform | QHTLSWUZ Surrogate |

## 定时任务

- CronJob ID: `8367c0cb`（7天后自动过期，需重新设置）
- 重新设置方法：告诉我"每天早上7点搜索最新EMRI文章展示给我"

## MCP 配置

- arxiv MCP: `C:\Users\12511\.mcp.json`
- Zotero MCP: 同上，web-api 模式，User ID: 16491712
