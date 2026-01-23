# Tokyo Yokai Mapping β

東京百鬼パレード — 東京圏妖怪マッピングプロジェクト

## 概要

東京圏（23区＋多摩地区＋高尾山）を舞台にした妖怪マッピングサイト。
地図を探索すると、区→妖怪→クラン/勢力→世界観へと潜れる構造。

## β版 公開地点（3地点）

| 地点 | レイヤー | 守護者 |
|------|----------|--------|
| 高尾山 | 山・結界 | アカリ（烏天狗） |
| 麻布十番 | 街・生活 | 光葉（白狐） |
| 隅田川 | 川・境界 | 甲羅姫（河童） |

## ページ構成

- `/` - トップページ（IP入口）
- `/map.html` - 妖怪マップ（Leaflet）
- `/characters.html` - キャラクターページ
- `/lore.html` - 世界観ページ

## 技術仕様

- **フロントエンド**: 純粋HTML/CSS/JS（フレームワーク不使用）
- **地図**: Leaflet.js + OpenStreetMap + CARTO Dark Matter
- **デプロイ先**: GitHub Pages対応（静的ファイルのみ）

## GitHub Pages 公開手順

### 1. リポジトリ作成
- GitHub で新規リポジトリを作成（例: `tokyo-yokai-map`）
- Public で OK

### 2. ファイルをアップロード
**重要**: フォルダごとではなく、中身のファイルを直接アップロード

```
❌ フォルダごとアップしない
⭕ index.html がリポジトリ直下に来るように
```

アップロード方法:
1. GitHub画面 → Add file → Upload files
2. 全ファイル選択 → Commit

### 3. GitHub Pages 有効化
1. Repository → Settings → Pages
2. Source: Deploy from a branch
3. Branch: main
4. Folder: / (root)
5. Save

### 4. 公開URL確認
数十秒〜1分後に表示される:
```
https://ユーザー名.github.io/リポジトリ名/
```

## ローカル確認

```bash
# Python 3
python3 -m http.server 8080

# ブラウザで開く
open http://localhost:8080
```

## データ設計

- 聖典/カードMDは「正本」として保持
- Web側は表示用インデックスJSONを別ファイルで管理
- `data/` 以下のJSONを編集することで地点追加可能

## 今後の拡張

1. **地点を"線"で増やす**
   - 隅田川 → 浅草 → 上野
   - 麻布 → 六本木 → 渋谷

2. **事件ノードを追加**
   - 例: 「隅田川異常流」

3. **制作ログと設定の相互リンク**

---

© 2026 東京百鬼パレード Project
