# 小学1〜6年 漢字総復習アプリ

小学校6年間の漢字を文章の中で復習する、手書き式の静的Webアプリです。

## GitHub Pagesへの設置

このフォルダの**中身**を、新しいGitHubリポジトリの最上位へアップロードしてください。
ZIPファイル自体をGitHubへ置いてもアプリとして動きません。必ず解凍します。

必要な構造:

```text
index.html
questions.json
rewards.json
images/
  reward01.jpeg
  reward02.jpeg
  ...
  reward10.jpeg
```

GitHub Pagesはリポジトリの Settings → Pages から、mainブランチの `/ (root)` を公開元にします。

## 中3版との分離

保存キーは `elementaryKanjiReview.v1` です。
中3版の `kanjiWritingApp.v1` とは異なるため、成績・周回状況・苦手一覧は混ざりません。
別リポジトリ・別URLで運用してください。

## 問題数

- 通常書き取り: 180問
- 同音異義語・同訓異字: 30問
- 四字熟語: 30問
- 合計: 240問

## 注意

- `index.html`、`questions.json`、`rewards.json`、`images`は同じ階層関係を保ってください。
- iPhone/iPadでは、GitHub上で先に `images/.keep` を作り、`images`フォルダ内へ画像をアップロードすると確実です。
- 古い表示が残る場合は、Pages URL末尾へ `?v=2` などを付けて再読込します。
