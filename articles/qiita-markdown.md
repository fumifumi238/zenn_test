---
title: "qiita markdown"
emoji: "📝"
type: "tech"
topics: ["qiita"]
published: false
---
<!-- open属性なし -->
<details><summary>サンプルコード（open属性なし）</summary>

(上に空行が必要)

```rb
puts 'Hello, World'
```
</details>

<!-- open属性あり -->
<details open><summary>サンプルコード（open属性あり）</summary>

(上に空行が必要)

```rb
puts 'Hello, World'
```
</details>
:::note info
インフォメーション
infoは省略可能です。
:::

:::note warn
警告
○○に注意してください。
:::

:::note alert
より強い警告
○○しないでください。
:::

<dl>
  <dt>リンゴ</dt>
  <dd>赤いフルーツ</dd>
  <dt>オレンジ</dt>
  <dd>橙色のフルーツ</dd>
</dl>

- [ ] タスク1
- [x] タスク2

foo[^foo]
bar[^bar]
baz[^baz]

[^foo]: 最初の脚注です。
[^bar]: 二番目の脚注です。
[^baz]: 三番目の脚注です。