---
name: crossref
description: Search academic literature via CrossRef, traverse citation chains, download via Sci-Hub.
---

# crossref

## Windows 调用方式（必须用 PowerShell）
```powershell
powershell.exe -Command "cd 'C:\Users\12511\.claude\skills\crossref\scripts\bin'; python crossref_search.py --search 'EMRI gravitational wave' --rows 5 2>&1"
```

## 搜索
```bash
python crossref_search.py --search "<keywords>" --rows 5
python crossref_search.py --refs <doi>          # 列出参考文献
python crossref_search.py --cite-trail <doi>    # 自动展开综述
```

## 下载
```bash
python sci_hub_dl.py <doi>                      # 单篇
python sci_hub_dl.py --batch dois.txt           # 批量
```

## 已知问题
- sci_hub_dl GBK crash：`_http.py` 中 `subprocess.run` 加 `capture_output=True`，`.decode('utf-8', errors='replace')`
- 代理：`$env:HTTPS_PROXY='http://127.0.0.1:7890'` 在同一 PowerShell -Command 块内设置
- PRD 等期刊常遇 CAPTCHA，arXiv 论文直接用 arxiv-mcp 更可靠
