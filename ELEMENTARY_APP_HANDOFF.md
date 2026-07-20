# 小学1〜6年 漢字総復習アプリ 引き継ぎ

## 現在の完成版

- バージョン: v1.0
- 問題数: 240問
- 基盤: 中3漢字アプリ v1.7
- 利用端末: iPad中心、iPhoneにも対応
- 配信: GitHub Pages

## 重要な分離設定

- 小学生版保存キー: `elementaryKanjiReview.v1`
- 中3版保存キー: `kanjiWritingApp.v1`
- 別リポジトリ・別GitHub Pages URLで運用すること
- 小学生版で中3版の `index.html` をそのまま使わないこと。保存キーが衝突するため

## 機能

- Apple Pencil、指、一般タッチペン、マウスで手書き
- 解答表示後も自分の筆跡を保持
- 一つ戻す／全消去
- 自己採点 ○△×
- 240問を重複なしで一周する周回出題
- ランダム出題
- 最新評価が△または×の問題だけを苦手一覧に表示
- 10問ごとにごほうび画像
- 成績・周回状況は端末内localStorageへ保存

## データ構造

```text
index.html
questions.json
rewards.json
images/reward01.jpeg ... reward10.jpeg
```

## 問題データ

`questions.json`:
- 通常書き取り 180
- 同音異義語／同訓異字 30
- 四字熟語 30

主なフィールド:
`id`, `type`, `prompt`, `answer`, `reading`, `meaning`, `answerLength`, `enabled`

## 壊さないこと

- Apple Pencil用のPointer Events＋Touch Events併用処理
- canvasの`touch-action:none`
- 筆圧に依存しない固定線幅
- 周回用の`state.round.seen`
- 小学生版固有のAPP_KEY
- 解答表示時にcanvasを再描画して筆跡を維持する処理

## 別セッション開始文

> 小学1〜6年漢字総復習アプリの続きです。添付ZIPが現在の完成版です。最初にELEMENTARY_APP_HANDOFF.mdとVERSION.txtを読んでください。Apple Pencil対策、周回出題、ランダム出題、苦手一覧、ごほうび機能、小学生版固有の保存キーを壊さずに修正してください。修正後は差し替え用ファイルと更新済み全体ZIPをください。
