# AIカリキュラムメーカー | 副担任mirAI

企業×学校を繋ぐ教育 OS。業界テーマを授業計画・教材・評価ルーブリックへ自動変換し、学びを進路まで一気通貫で設計します。

## 機能

| タブ | 内容 |
|------|------|
| 🏠 ホーム | 機能概要・導入効果・学びの柱 |
| 📋 カリキュラムメーカー | 9業界テンプレートから学習指導要領準拠の授業計画を自動生成 |
| 🧭 17軸キャリア診断 | スキルレーダーチャートと最適プログラム・偉人マッチング |
| 🤖 副担任mirAI | AIチャットによる進路・学習・面談準備サポート |
| 📊 クラス管理ダッシュボード | 生徒の学習状況・mirAI活用率をリアルタイム可視化 |

## GitHub Pages 公開手順

### 1. GitHubリポジトリを作成

```bash
# GitHubで新規リポジトリを作成後（例: ai-curriculum-maker）
git init
git add index.html README.md
git commit -m "Initial commit: AIカリキュラムメーカー"
git branch -M main
git remote add origin https://github.com/<ユーザー名>/<リポジトリ名>.git
git push -u origin main
```

### 2. GitHub Pages を有効化

1. GitHubのリポジトリページ → **Settings** → **Pages**
2. **Source** → `Deploy from a branch`
3. **Branch** → `main` / `/ (root)` → **Save**
4. 数分後に `https://<ユーザー名>.github.io/<リポジトリ名>/` で公開

### 3. 更新時

```bash
cp "AIカリキュラムメーカー_副担任mirAI.html" index.html
git add index.html
git commit -m "Update app"
git push
```

プッシュ後、約1〜2分で自動デプロイされます。

## ローカル確認

```bash
# Python 3 (推奨)
/usr/local/bin/python3.13 -m http.server 8765 --directory .
# → http://localhost:8765/index.html
```

## 技術構成

| 項目 | 内容 |
|------|------|
| フレームワーク | React 18 (UMD / Babel Standalone) |
| UIライブラリ | Font Awesome 6.5 |
| チャート | Chart.js 4.4 |
| フォント | Noto Sans JP / Space Grotesk (Google Fonts CDN) |
| デプロイ | **単一HTMLファイル**（外部依存はすべてCDN） |

> 単一HTMLファイル構成のため、ビルド不要でそのまま GitHub Pages に公開できます。

## ライセンス

本プロジェクトは教育目的のプロトタイプです。
