# 🎱 Cue Note（オフライン版）

ビリヤード練習を記録するアプリ。タップでサクサク・スマホで使える。

**オフライン版**：データはこのブラウザ（端末）内だけに保存される。アカウント不要・サーバー不要。スマホ⇔PCの同期はなし、端末ごとに別データ。

## 機能
- 種別を大項目→小項目でタップ選択（基礎/出し/実戦/守備/ブレイク/メンタル）
- 各種目にプロ由来のワンポイントアドバイス
- タイマー（▶開始／■終了）または時間チップで記録
- 気づきメモ＋過去メモの自動表示
- 履歴：月カレンダー＋「気づき」一覧（種目フィルタ）
- ルーティン：手順を登録して順番に進行（出典付きおすすめ10個プリセット）
- AI評価用コピー（日次／月次）

## 技術構成
- Vanilla HTML/JS/CSS（フレームワークなし）
- localStorage に全データ保存（キー: `poollog_offline_v1`）
- PWA：マニフェスト＋Service Worker＋専用アイコン

## ローカル起動
```bash
python3 -m http.server 8700
open http://localhost:8700
```

## デプロイ
Cloudflare Pages にGitHubリポジトリを連携。ビルドコマンド不要、出力ディレクトリ `/`。

## ベース
[fileconcon/practice-log](https://github.com/fileconcon/practice-log) のSupabase接続をlocalStorage版に置き換えたフォーク。
