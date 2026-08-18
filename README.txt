Robot Planner 插件轉換器

1. 打開 index.html。
2. 把 Windows Robot Planner 插件 ZIP 拖進去。
3. 網頁會讀 mod.json / main.py 並抽出可轉換的 JavaScript。
4. 檢查 main.js。
5. 下載雙平台插件 ZIP。

輸出會保留 main.py，並新增 main.js 與 mod.json 的 ios_entry。
目前最適合 PLUGIN_JS + ctx.inject_js / ctx.run_js 類型。
純 Python、PySide6、os/subprocess、Python hook 不保證自動轉換。

注意：index.html 目前從 cdnjs 載入 JSZip 3.10.1，因此使用時需要網路載入 JSZip。
