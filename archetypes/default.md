---
title: "お試しです"
draft: false #draft。-Dをつけないと表示されない。
date: 2022-08-12T22:53:03+09:00
lastmod: 2020-03-04T15:58:26+08:00
subtitle: "試してみました"
images: ["minokuba.png"] #twitter cards.

tags: ["aaa","bbb"] #tag
categories: ["AAA","BBB","CCC","DDD"] #カテゴリ

featuredImage: "xxxx.png" #記事の頭に表示する画像。static/posts/<title>/からの相対パス。 
featuredImagePreview: "minokuba.png" #ブログ一覧画面に表示するPreview 。staticからの相対パス。

hiddenFromHomePage: false #ホームページ非表示にする場合はtrue
hiddenFromSearch: false #検索結果非表示にする場合はtrue
# 省略したテンプレートは以下を参照  https://hugoloveit.com/theme-documentation-content/#front-matter

---
## タイトル {#タイトル}

xxxx

### 小タイトル１ {#小タイトル１}
xxxxxxx
xxxxxxx

xxxxxxx

### 小タイトル２ {#小タイトル２}
xxxxxxx
xxxxxxx

xxxxxxx

---
## テンプレート

## h2 Heading {#custom-id}
### h3 Heading {#custom-id}
#### h4 Heading {#custom-id}
##### h5 Heading {#custom-id}
###### h6 Heading {#custom-id}

<!-- コメント -->
___

### 文章 {#文章}
Lorem ipsum dolor sit amet, graecis denique ei vel, at duo primis mandamus. Et legere ocurreret pri,
animal tacimates complectitur ad cum. Cu eum inermis inimicus efficiendi. Labore officiis his ex,
soluta officiis concludaturque ei qui, vide sensibus vim ad.

### Bold {#Bold}

**bold textです。**

### 斜体 {#斜体}
*斜体です*

### 取り消し線 {#取り消し線}
~~取り消し線です。~~

### 斜体・Bold・取り消し線の組み合わせ
***bold and italics***
~~**strikethrough and bold**~~
~~*strikethrough and italics*~~
~~***bold, italics and strikethrough***~~

### ブロック引用 {#ブロック引用}
> **ブロック引用です。** combines a hard drive with a flash storage (solid-state drive) and presents it as a single logical volume with the space of both drives combined.
>> 入れ子の引用です。Sed adipiscing elit vitae augue consectetur a gravida nunc vehicula. Donec auctor
odio non est accumsan facilisis. Aliquam id turpis in dolor tincidunt mollis ac eu diam.

### 順不同リスト {#順不同リスト}
* Consectetur adipiscing elit
* Integer molestie lorem at massa
* Facilisis in pretium nisl aliquet
* Nulla volutpat aliquam velit
  * Phasellus iaculis neque
  * Purus sodales ultricies
  * Vestibulum laoreet porttitor sem
  * Ac tristique libero volutpat at
* Faucibus porta lacus fringilla vel
* Aenean sit amet erat nunc
* Eget porttitor lorem

---

### 順序付けられたリスト {#順序付けられたリスト}
1. 順序付けられたリストです。
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
4. Facilisis in pretium nisl aliquet
5. Nulla volutpat aliquam velit
6. Faucibus porta lacus fringilla vel
7. Aenean sit amet erat nunc
8. Eget porttitor lorem

---
### タスクリスト {#タスクリスト}
- [x] タスクリストです。
- [ ] Update the website
- [ ] Contact the media

---
### インラインコード {#インラインコード}
In this example, `<section>インラインコードです。</section>` should be wrapped as **code**.

---
### インデントされたコード {#インデントされたコード}
    // Some comments
    line 1 of code インデントされたコード　スペースを4つ入力します。
    line 2 of code
    line 3 of code

---
### ブロックフェンス {#ブロックフェンス}
```markdown
Sample text here... ブロックフェンス
```

---
### 言語の引用（jsの例） {#言語の引用}
```js
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```
### テーブル {#テーブル}
| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

---
### 外部リンク {#リンク}
<https://assemble.io> 

<contact@revolunet.com>

[Assemble](https://assemble.io)

[Upstage](https://github.com/upstage/ "Visit Upstage!")

---
### 内部リンク {#内部リンク}
#### Table of Contents
  * [文章](#文章)
  * [斜体](#斜体)

---
### 脚注 {#脚注}
This is a digital footnote[^1].
This is a footnote with "label"[^label]

[^1]: This is a digital footnote
[^label]: This is a footnote with "label"

---
### 画像リンク {#画像リンク}
![Minion](https://octodex.github.com/images/minion.png)
{{< figure src="/minokuba.jpg" title="minokuba" >}}

---
### その他の書き方
[画像やYoutube、twitterの埋め込み](https://hugoloveit.com/theme-documentation-built-in-shortcodes/)

[拡張ショートコード](https://hugoloveit.com/theme-documentation-extended-shortcodes/)

[mermaid](https://hugoloveit.com/theme-documentation-mermaid-shortcode/)

[echarts](https://hugoloveit.com/theme-documentation-echarts-shortcode/)

[mapbox](https://hugoloveit.com/theme-documentation-mapbox-shortcode/)

[音楽](https://hugoloveit.com/theme-documentation-music-shortcode/)
