# AIカリキュラムメーカー 副担任mirAI

N-E.X.T.ハイスクール構想対応の教育支援プラットフォーム。
企業・自治体テーマを授業計画・教材・評価ルーブリックへ自動変換し、学びを進路まで一気通貫で設計します。

## 機能

- **AIカリキュラムメーカー** — 業界テーマから学習指導要領準拠の授業計画を自動生成
- **17軸キャリア診断** — スキルレーダーチャートと最適プログラム提案
- **副担任mirAI** — AIチャットによる進路・学習相談
- **クラス管理ダッシュボード** — 生徒の成長を可視化

## GitHub Pages 公開手順

### 1. GitHubリポジトリを作成

```bash
# GitHubでリポジトリを新規作成後（例: ai-curriculum-maker）
git init
git add index.html README.md
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<ユーザー名>/<リポジトリ名>.git
git push -u origin main
```

### 2. GitHub Pages を有効化

1. GitHubのリポジトリページを開く
2. **Settings** → **Pages** に移動
3. **Source** を `Deploy from a branch` に設定
4. **Branch** を `main` / `/ (root)` に設定して **Save**
5. 数分後に `https://<ユーザー名>.github.io/<リポジトリ名>/` で公開される

### 3. 更新時

```bash
# index.htmlを更新後
git add index.html
git commit -m "Update app"
git push
```
プッシュ後、約1〜2分で自動デプロイされます。

## ローカル確認

ブラウザで `index.html` を直接開くか、ローカルサーバーを使う場合：

```bash
# Python 3
python3 -m http.server 8080
# → http://localhost:8080 で確認
```

## 技術構成

| 項目 | 内容 |
|------|------|
| フレームワーク | React 18 (UMD / Babel Standalone) |
| UIライブラリ | Font Awesome 6.5 |
| チャート | Chart.js 4.4 |
| フォント | Noto Sans JP / Space Grotesk |
| デプロイ | 単一HTMLファイル（外部依存はすべてCDN） |

> 単一HTMLファイル構成のため、サーバー設定不要でそのまま GitHub Pages に公開できます。

## 注意事項

- Claude API等の外部APIキーは含まれていません（AIチャット機能はUI模擬動作）
- 画像はUnsplash CDN経由で表示されます（オフライン環境では非表示）
