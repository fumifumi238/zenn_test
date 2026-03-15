---
title: "Qiita/Zennに直接投稿できて、最高に書きやすいMarkdown Editorを作った"
emoji: "📝"
type: "tech"
topics: ["TypeScript", "React", "Zenn", "Markdown", "個人開発"]
published: false
---
# Qiita/Zennに直接投稿できて、最高に書きやすいMarkdown Editorを作った

技術記事を投稿しよう！
そう思っていざ書いてみてもなかなかうまくいかないですよね
特に面倒なのが、markdownです。

markdownを使ってるとこんなことがよく起こります。

- Readme くらいは書くんだけどイマイチ苦手
- Tableがむちゃくちゃ不便
- どれがどのmarkdownか覚えてない。

そこで作ったのが、リアルタイムプレビュー付きの Markdown エディタ **No Markdown(Not Only Markdown)** です。
Markdownに慣れている人にも慣れていない人にも優しいツールを目指しました。

[No Markdown](https://nomarkdown.vercel.app/)

# 目次

:::details 1. 主な機能
[1. editorからmarkdownとして編集する](#1.-editorからmarkdownとして編集する)
[2. previewから見た目どおり編集する](#2.-previewから見た目どおり編集する)
[3. qiitaもしくはzennに投稿する](#3.-qiitaもしくはzennに投稿する)
:::

:::details 2. 対応しているmarkdown
[1. 太字 斜体 打ち消し](#1.-太字-斜体-打ち消し)
[2. リンク](#2.-リンク)
[3. 画像](#3.-画像)
[4. リスト 番号付きリスト チェックボックス](#4.-リスト-番号付きリスト-チェックボックス)   
[5. 見出し](#5.-見出し)
[6. テーブル](#6.-テーブル)
[7. 引用](#7.-引用)
[8. 折りたたみ詳細](#8.-折りたたみ詳細)
[9. コード](#9.-コード)
[10. 水平線](#10.-水平線)
:::

[3. 使用技術](#3-使用技術])
[4. 追加したい機能](#4.-追加したい機能)
[5. まとめ](#5.-まとめ)

# 1. 主な機能
# 1. editorからmarkdownとして編集する

最もシンプルな使い方は、左側のediotrから直接編集することです。
上部にあるツールバーから直接markdownを挿入できるので、markdownを覚える必要がありません。
また/を使うことによりマウス操作せずともコマンドを呼び出せます。

## ツールバーの例

![toolber.png](/images/qiitazennmarkdown-editor/c106e8c4-4611-4331-bb4c-f80b4017d793.png)

## スラッシュコマンドの例

![slash.png](/images/qiitazennmarkdown-editor/62b5fc1e-30f0-4377-88d5-8725bd457141.png)

# 2. previewから見た目どおり編集する

見た目から直接編集したい方には、previewから編集がおすすめです。
ダブルクリックで行を編集したり、範囲選択で一部分だけ太字にできたりします。
また、空白行を押して画像や表の挿入もできます。

## preview編集の例

![preview_toolber.png](/images/qiitazennmarkdown-editor/7421a358-4552-4b11-b139-3fbadbc27112.png)

## 範囲選択の例

![select.png](/images/qiitazennmarkdown-editor/29959d1b-d57d-4936-aae7-d0f73523ebfd.png)

# 3. qiitaもしくはzennに投稿する

書いた記事を直接、qiita、zennに投稿することも可能です。
  qiita、zenn(github連携)のアカウントがあれば直接投稿できます。
  セキュリティが不安な方はmarkdownをコピーやDLすることも可能です。

## qiita投稿の例

![qiita_publish.png](/images/qiitazennmarkdown-editor/f13170fa-6ce5-4e6b-8391-9554e9f1fc1d.png)

# 対応しているmarkdown
# 1. 太字 斜体 打ち消し

太字は `/bold`、斜体は `/italic`、打ち消しは `/strike` で入力できます。
また、htmlタグの `<b>(<strong>)`、`<i>`、`<s>` も使用可能です。
htmlタグは投稿やコピーの際には、markdownに変換されます。

# 2. リンク

リンクは`/link`または`/url`で入力できます。
htmlタグの`<a>`も使用可能です。

# 3. 画像

画像は `/image` で入力できます。
htmlタグの`</img>`も使用可能です。
editor側、preview側から画像をアップロードでき、Altや大きさの変更も可能です。
ただし、コピー、DLの際は適応されません。
また直接qiitaに投稿する際は、ローカル画像は
[catbox](https://catbox.moe/)
にアップロードされるので、プライベートな画像の際はコピーをお試しください。

## 画像編集の例

![no_markdown_icon.png](/images/qiitazennmarkdown-editor/d9434884-c035-42d5-9bf4-280214de235b.png =284x)

# 4. リスト 番号付きリスト チェックボックス

リストは `/list`、番号付きリストは `/olist`、チェックボックスは`/checkbox`で入力できます。
**editorでは次のリスト要素(-、や2.)が自動挿入されます。**
解除の際は `Enter` を二回押すか、そのまま消してください
チェックボックスはpreviewから直接チェックすることもできます。

# 5. 見出し

それぞれ`/h1~/h6`で入力できます。
htmlタグの `<h1>~<h6>` も使用可能です。

# 6. テーブル

`/table`で入力できます。
preview側で直接tableの操作が可能です。
**テーブル要素はmarkdownでも使いにくい要素のため、previewでの編集をおすすめします**
preview側のテーブルをクリックすると編集できます。

## previewでのテーブル編集の例

![edit_table.png](/images/qiitazennmarkdown-editor/4747bf1b-aede-439f-8245-4769fbcd5b53.png)

# 7. 引用

`/quote` で入力できます。
`> >`で二重引用以上にできますが、markdownの形式によっては対応していない場合があるので注意が必要です。

# 8. 折りたたみ詳細

`/details` で入力できます。
一行空行が必要です。
zennは独自のdetailsを採用しているため、`<details open>`と書いても、openが無効化されます。

```html:details.html
:::details 詳細
　<!-- openはzennでは無効です。 -->
<!-- 一行空行が必要です。 -->
内容
:::
```

# 9. コード

インラインコードは `/inlinecode`、コードブロックは `/codeblock` で入力可能です。
htmlタグの `code`、`<pre><code>` も使用可能です。
コードブロックでは、`言語名:ファイル名` `例 js:app.js` のように入力すると、
qiitaとzennではシンタックスハイライトが適用されます。
ハイライトされるかどうかは、qiitaとzennのシンタックスハイライターに依存しているため、投稿時にはハイライトされない場合もあります。

## コードブロックの例

![codeblock.png](/images/qiitazennmarkdown-editor/54ba47d5-f66d-4e97-98aa-dc22601efc44.png)

## シンタックスハイライトの例

![syntax.png](/images/qiitazennmarkdown-editor/22c99ae5-a9f9-40a0-9524-2f990d234f97.png)

# 10. 水平線

`/hr` で入力できます。
htmlタグの`<hr>`も使用可能です。

# 3. 使用技術

- **Framework**: Next.js 15 (App Router)
- **Language**: TypeScript
- **Editor**: Code Mirror
- **Styling**: Tailwind CSS
- **Code Highlight**: Shiki
- **Auth**: NextAuth.js
- **Database**: Supabase
- **Test**: Vitest, Playwright

# 4. 追加したい機能

- モバイルのUI改善
- qiita、zenn独自の記法の拡張

## 5. まとめ

自分で書いていても使いやすいmarkdown editorができたと感じます。
前々から作ってみたかったものができたのは、codexやclaudeなどのその他AIツールのおかげです。
スマートフォン対応はまだ気に入ってませんが、よければ使ってみてください。