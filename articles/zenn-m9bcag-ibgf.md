---
title: "zenn用のエンコード"
emoji: "📝"
type: "tech"
topics: ["Testing Library"]
published: false
---
# Qiita/Zennに直接投稿できて、最高に書きやすいMarkdown Editorを作った

技術記事を投稿しよう！
そう思っていざ書いてみてもなかなかうまくいかないですよね
特に面倒なのが、markdownです。

- Readme くらいは書くんだけどイマイチ苦手
- Tableがむちゃくちゃ不便
- どれがどのmarkdownか覚えてない。

こんなことがよく起こります

そこで作ったのが、リアルタイムプレビュー付きの Markdown エディタ **No Markdown(Not Only Markdown)** です。
Markdownに慣れている人にも慣れていない人にも優しいツールを目指しました。

[No Markdown](https://nomarkdown.vercel.app/)

:::details 主な機能
[1.editorからmarkdownとして編集する](#1-editorからmarkdownとして編集する)
[2.previewから見た目どおり編集する](#2-preview%E3%81%8B%E3%82%89%E8%A6%8B%E3%81%9F%E7%9B%AE%E3%81%A9%E3%81%8A%E3%82%8A%E7%B7%A8%E9%9B%86%E3%81%99%E3%82%8B)
[3.qiitaもしくはzennに投稿する](#3-qiita%E3%82%82%E3%81%97%E3%81%8F%E3%81%AFzenn%E3%81%AB%E6%8A%95%E7%A8%BF%E3%81%99%E3%82%8B)
:::

:::details 対応しているmarkdown
[1. 太字、斜体、打ち消し](#1-%E5%A4%AA%E5%AD%97%E6%96%9C%E4%BD%93%E6%89%93%E3%81%A1%E6%B6%88%E3%81%97)
[2. リンク](#2-リンク)
[3. 画像](#3-画像)
    
4. リスト、番号付きリスト、チェックボックス
5. 見出し
6. テーブル
7. 引用
8. 折りたたみ詳細
9. コード
10. 水平線
:::

- エディタとプレビューを並べて確認できる
- プレビュー側をそのまま編集できる
- 画像、表、チェックリスト、details を扱いやすい
- 下書きを複数保存できる
- Markdown をコピー / `.md` として保存できる
- Qiita と Zenn にそのまま投稿できる

## 1. エディタとプレビューを並べて書ける

左で文章を書きながら、右で見た目をすぐ確認できます。`Editor / Both / Preview` の切り替えもあるので、書くときと整えるときで画面の使い方を変えやすいです。

![エディタとプレビューが同期する様子](https://example.com/nomarkdown/editor-preview-sync.gif)

## 2. プレビューをそのまま編集できる

`No Markdown` の一番使いたかったポイントはここです。プレビュー上のテキストを直接触って、見出しやリスト、チェックボックスをその場で直せます。

「Markdown は最終出力として欲しい。でも書いているときはなるべく Markdown 記法を意識したくない」という人にはかなり合うと思っています。

![プレビューをそのまま編集する様子](https://example.com/nomarkdown/wysiwyg-preview-edit.gif)

<h1 id="link">h1</h1>

## 3. 表や画像まわりも詰まりにくい

表は専用 UI で編集でき、画像のサイズ変更もできます。ただし、プラットフォームの違いも考えて、qiita、zennに直接投稿しない場合は、サイズが保存されません。画像サイズや alt の調整もプレビュー側から触れるので、記事レイアウトの調整がしやすいです。

![画像アップロードとサイズ調整の様子](https://example.com/nomarkdown/image-upload-and-resize.gif)

![テーブル編集の様子](https://example.com/nomarkdown/table-edit.gif)

## 4. 下書きを残しながら書ける

ブラウザに編集中の内容が残るので、途中で閉じても戻りやすいです。さらに下書き一覧から切り替えられるので、記事を複数並行で書く用途にも向いています。

![下書き一覧から切り替える様子](https://example.com/nomarkdown/draft-switch.gif)

## 5. 最後は Markdown として持ち出せる

「投稿は別の場所でしたい」「とりあえず md ファイルを残したい」というときのために、Markdown のコピーと `.md` ダウンロードを用意しています。

ローカル画像を使っている場合は、コピー / 保存のタイミングで公開 URL に置換するかどうかも選べます。

![Markdown をコピー / 保存する様子](https://example.com/nomarkdown/markdown-export.gif)

## 6. Qiita / Zenn 投稿までつなげている

Qiita は OAuth 連携して、そのまま API 経由で投稿できます。Zenn は GitHub 連携したリポジトリに `articles/*.md` と画像をコミットする形で投稿できます。

投稿前に毎回別ツールへ移動して体裁を確認する手間が減るようにしました。

![Qiita 投稿ダイアログの様子](https://example.com/nomarkdown/qiita-publish.gif)

![Zenn 投稿ダイアログの様子](https://example.com/nomarkdown/zenn-publish.gif)

## こんな人に向いています

- Qiita や Zenn の記事をブラウザでさっと書きたい人
- Markdown は必要だけど、記法の記憶にあまり脳のリソースを使いたくない人
- プレビューを見ながら表や画像を調整したい人
- 下書き保存と最終的な Markdown 持ち出しを両立したい人

## まだ伸ばしたいところ

まだ作り込み途中の部分もあります。特にモバイル操作、プレビュー上の編集体験、UI の整理は継続して改善したいです。

使ってみて「ここが詰まる」「この操作が欲しい」があれば、GitHub の Issue や PR で教えてもらえると助かります。

## まとめ

**No Markdown** は、Markdown を捨てるツールではなく、Markdown を最終成果物として持ちながら書く過程を少し楽にするためのエディタです。

Qiita / Zenn に記事を書く頻度が高い人ほど相性がいいと思うので、よければ触ってみてください。

|  |  |
| :--- | ---: |
|  |  |
|  |  |

# 2. previewから見た目どおり編集する
# 3. qiitaもしくはzennに投稿する
# 1. 太字、斜体、打ち消し