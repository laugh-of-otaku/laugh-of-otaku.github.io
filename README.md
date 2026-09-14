# 研究ノートと日記

研究ノート・日記・AboutをMarkdownで管理する個人サイトです。

公開URL: https://laugh-of-otaku.github.io/

## 普段の更新

GitHub上でファイルを開き、鉛筆の編集ボタンから更新して **Commit changes** を押します。`main` に保存すると自動で公開されます。反映状況は **Actions → pages build and deployment** で確認できます。

| 内容 | 編集するファイル |
| --- | --- |
| 研究ノート | `_research/好きな英数字の名前.md` |
| 日記 | `_posts/YYYY-MM-DD-好きな英数字の名前.md` |
| About | `about.md` |
| 研究ノート一覧の紹介文 | `research.md` |
| 日記一覧の紹介文 | `diary.md` |
| サイト名・説明 | `_config.yml` |

記事一覧とホームの最新記事は自動更新されます。本文のMarkdownを書く際、先頭の `---` で囲まれた設定欄を残してください。本文は設定欄の下から書きます。

### 研究ノートを追加する

**Add file → Create new file** で、例として `_research/my-topic.md` を作成します。日付・見出し・説明・本文を書き換えて保存してください。

```markdown
---
title: ノートのタイトル
date: 2026-09-14 09:00:00 +0900
description: 一覧に表示する短い説明。
---
## 問い

調べたいことを書く。

## 分かったこと

学んだことや考察を書く。

## 参考資料

- [資料名](https://example.com/)

## 次に確かめること

残った疑問を書く。
```

### 日記を追加する

`_posts/2026-09-14-my-diary.md` のように **日付と半角英数字の名前** を含むファイルを作成します。ファイル名の日付と `date` の日付をそろえます。

```markdown
---
title: 今日の日記
date: 2026-09-14 21:00:00 +0900
description: 今日のひとこと。
---
ここに日記を書く。
```

未来の日時の記事は、その時刻より前には表示されません。時刻を過ぎても自動では再公開されないため、その後のコミットまたはActionsの再実行が必要です。非公開の内容はこの公開リポジトリに保存しないでください。`published: false` はサイト表示を止めるだけで、ファイルは公開されたままです。

### Aboutを編集する

`about.md` の設定欄の下を書き換えます。現在はアカウント名とサイトの目的だけを記載しています。プロフィール、研究テーマ、公開したい連絡先などは必要に応じて追加できます。

## 構成と公開設定

- Jekyll（GitHub Pages標準ビルド）
- 研究ノート: `research` コレクション
- 日記: Jekyllの投稿機能
- 共通レイアウト: `_layouts/default.html`
- スタイル: `style.css`（外部フォント・JavaScriptへの依存なし）
- 公開元: **Settings → Pages → Deploy from a branch → main / (root)**
- HTTPS: 有効

## ローカルで確認する

RubyとBundlerがある環境で実行します。

```sh
bundle install
bundle exec jekyll serve
```

http://localhost:4000/ を開きます。`_config.yml` を変えたらサーバーを再起動します。

## 初期状態の保全

2026-09-14、ログイン中の `laugh-of-otaku` の所有リポジトリ一覧が0件であることを確認して、このリポジトリを新規作成しました。既存リポジトリの削除は行っていません。

最小ページの公開確認を行ったコミットは `b818fd0a52b31938a3c34e9425d72d20bac8ac5f` です。Jekyll導入前のファイルはGit履歴から確認・復元できます。復元時は履歴の強制上書きを避け、変更を戻す新しいコミットを作成してください。

## 公式資料

- [GitHub Pagesの公開元の設定](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [Jekyllのコレクション](https://jekyllrb.com/docs/collections/)
