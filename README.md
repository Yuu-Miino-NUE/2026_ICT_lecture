# 2026 ICT 活用講義

鳴門教育大学 2026 年度 ICT 活用講義の演習用リポジトリです。

## 📊 演習用 API

GitHub Pages 経由で数学全国統計のモックデータを公開しています。

| 種別 | URL |
|---|---|
| **JSON エンドポイント** | `https://yuu-miino-nue.github.io/2026_ICT_lecture/data/math-statistics-2025.json` |
| **API ドキュメント** | https://yuu-miino-nue.github.io/2026_ICT_lecture/ |

### クイックスタート

```js
// JavaScript (fetch)
const res  = await fetch("https://yuu-miino-nue.github.io/2026_ICT_lecture/data/math-statistics-2025.json");
const data = await res.json();
console.log(data.statistics.mean); // 66.8
```

```python
# Python
import urllib.request, json
with urllib.request.urlopen("https://yuu-miino-nue.github.io/2026_ICT_lecture/data/math-statistics-2025.json") as r:
    data = json.loads(r.read())
print(data["statistics"]["mean"])  # 66.8
```

## 📁 ファイル構成

```
.
├── data/
│   └── math-statistics-2025.json   # 演習用統計データ
├── index.html                       # API ドキュメントページ
└── .github/workflows/
    └── deploy-pages.yml             # GitHub Pages 自動デプロイ
```

## ⚠️ 注意

`data/math-statistics-2025.json` は教育目的で作成したフィクションのデータです。実際の試験結果とは関係ありません。
