# ターン手帖

HTML/CSS/JavaScriptだけで動く、ターン制の一日管理PWAです。タスクを処理するためではなく、「今日を納得して終える」ために、0.5 / 1 / 2ターン単位で一日の過ごし方を記録します。

## 特徴

- 外部ライブラリなしの静的アプリ
- `localStorage` に保存
- スマホ縦画面向け
- GitHub Pagesで公開可能
- 今日の最大ターン数、使用ターン数、残りターン数を表示
- カテゴリ: 作業 / ゲーム / 家事 / 調べもの / 休憩 / 外出 / 体調回復
- 休憩や体調回復を、今日を保つための前向きな記録として扱う
- 過去7日分の記録を確認可能
- Service WorkerとWeb App ManifestによるPWA対応

## 使い方

1. `index.html` をブラウザで開きます。
2. 今日の最大ターン数を必要に応じて変更します。
3. カテゴリ、ターン数、メモを入力して記録します。
4. 「終えるためのひとこと」で今日のまとめを確認します。

保存先はブラウザの `localStorage` です。別ブラウザ、別端末、シークレットウィンドウとはデータ共有されません。

## GitHub Pagesで公開する手順

1. このリポジトリをGitHubにpushします。
2. GitHubのリポジトリページを開きます。
3. `Settings` を開きます。
4. 左メニューの `Pages` を開きます。
5. `Build and deployment` の `Source` で `Deploy from a branch` を選びます。
6. `Branch` で公開したいブランチを選び、フォルダは `/ (root)` を選びます。
7. `Save` を押します。
8. 数十秒から数分後、表示されたGitHub PagesのURLでアプリを開けます。

## ファイル構成

```text
.
├── index.html
├── manifest.json
├── service-worker.js
└── README.md
```

## 開発メモ

このアプリはビルド不要です。GitHub Pagesではルートにある `index.html` がそのまま配信されます。
