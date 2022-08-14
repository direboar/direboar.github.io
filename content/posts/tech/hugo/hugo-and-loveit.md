---
title: Github Pages + Hugo + Loveitでブログを作ってみた
draft: false #draft。-Dをつけないと表示されない。
date: 2022-08-14T14:00:00+09:00
lastmod: 2022-08-14T14:00:00+09:00
images: [posts/tech/hugo/hugo-and-loveit/hugo-logo-wide.svg] #twitter cards.

tags: [Hugo] #tag
categories: [Tech] #カテゴリ

featuredImage: "hugo-logo-wide.svg" 
#記事の頭に表示する画像。static/posts/<title>/からの相対パス。 
featuredImagePreview: "posts/tech/hugo/hugo-and-loveit/hugo-logo-wide.svg" 
# featuredImagePreview: "https://d33wubrfki0l68.cloudfront.net/c38c7334cc3f23585738e40334284fddcaf03d5e/2e17c/images/hugo-logo-wide.svg" 
#ブログ一覧画面に表示するPreview 。staticからの相対パス。

hiddenFromHomePage: false #ホームページ非表示にする場合はtrue
hiddenFromSearch: false #検索結果非表示にする場合はtrue
# 省略したテンプレートは以下を参照  https://hugoloveit.com/theme-documentation-content/#front-matter

---
## ブログをつくるよ
### ブログ作る目的 
最近作ったサービス[Yontaku](https://twitter.com/yukaritakayamah/status/1557671699230834688)の技術情報をどこかにメモしたいなと考えていたのですが、NotesやQiitaで共有しても広告付かないし、自分の資産にならないのでイマイチかな？と思い、せっかくなので自分のブログを立ち上げることにしました。

「はてなブログ」で立ち上げることも考えたのですが・・・。過去に「はてなダイアリー」でブログ作ってまして、Springのマニュアル邦訳（DIのところくらいまで）作っていたので多少はPVもあったのですが、「はてなダイアリー」終了で悲しい思いをしまして。。。そういう経緯もあり外部サービスに頼るのやめて、自分のブログを持とうかなと。
### ブログ作る方法
ガチでやるならレンタルサーバ借りてWordPress鉄板なんでしょうが

[【初心者でも安心】たった10分で出来るWordPressブログの始め方](https://www.xserver.ne.jp/blog/xserver-wordpress-quickstart/)

* ブログで稼ぐ気なんてさらさらない
* 左程PV集まる算段もない
* たぶん続かない

ので、そんなことしません。かわりに以下の方法でやります。これなら無料で運営できます。

* [Hugo](https://gohugo.io/)を使用してブログのコンテンツを作成する
* ブログはGithub Pagesに無料でホスティングする
* 続くかもわかんないのでドメインは取らない。Github Pagesのドメインで運用する。

ということで、これ以降はHugoを使ってブログを作成した際の覚書を記載します。

## [Hugo](https://gohugo.io/)とは 
Webサイトを生成するための静的サイトジェネレータです。Webサイトを作成する際に、HTMLを直接書く必要はありません。[Markdown](https://www.asobou.co.jp/blog/bussiness/markdown)ファイルからWebページを生成することができます。

MarkdownからどのようなWebサイトを生成するかについては、[Hugoのテーマ](https://themes.gohugo.io/)を選択することで決まります。自分が使いたいテーマを選択することができます。
Hugoの詳細は、[まくまくHugoノート](https://maku77.github.io/hugo/)にかなり詳細にまとまっていそうなので、こちらを参照ください。
### [Loveit](https://themes.gohugo.io/themes/loveit/)とは
Hugoでブログを作成するためのテーマです。開発者は中国の方みたいですね。どのテーマにするかは[Hugoのテーマ](https://themes.gohugo.io/)サイトで以下の基準で評価して決めました。

* GitHubスターの数
* 最終更新日（今もメンテされているか）
* 見た目のイメージが気にいるか。

見た目がごてごてしておらずすっきりしていたこと、ダークテーマの切り替えや検索機能が実装されていることも好印象でした。（チャイナに偏見持ちなので一瞬拒否反応出そうになりましたがｗ）

Loveitのその他の特徴は[Why choose LoveIt](https://themes.gohugo.io/themes/loveit/#why-choose-loveit)や[Features](https://themes.gohugo.io/themes/loveit/#features)を見るとよいかと思います。

### Hugo+Loveitをとりあえず使えるようになるまでに踏んだ手順
Hugo自体結構機能が多そうで、真面目に勉強すると時間がかかりそうだなーと思ったので、以下の手順でやりました。大分サボりました。

* Hugoの概要をどこかのページでいくつか眺める
* [Hugoのインストール](https://gohugo.io/getting-started/installing/)を行う
* [Hugoのusage](https://gohugo.io/getting-started/usage/)を行う
* [LoveItのTheme Documentation - Basics](https://gohugo.io/getting-started/usage/)を読み、簡単なサイトを作る

それ以降は、LoveItのマニュアルを中心に読んで対応しました。Hugoちゃんと勉強してからのが良かったかなーと思うところもあったので、最初にフォルダの意味や基本的な仕組み（layoutsとthemeの関係とか）くらいは理解しておいたほうが良いかもしれません。

実際にサイト作ってみた感想としては、マークダウンのフォーマットやテーマのカスタマイズなどは結局テーマごとに異なるので、実際に使うテーマのマニュアルを中心に取り組んだ方が結果的に早く理解できるかなーと思いました。

## Hugo+Loveit+Github Pagesでブログ作成時の細かいTips

現時点でハマっている内容も含めてメモします。

### Github Pagesでホスティングしたい
[Hugoのマニュアル](https://gohugo.io/hosting-and-deployment/hosting-on-github/)にバッチリ記載されています。Github ActionsのYAMLファイルも提供されているので、ほんとほぼこのまんまできるはずです。めちゃくちゃ楽。
### Faviconを表示したい
[Loveitのマニュアル](https://hugoloveit.com/theme-documentation-basics/#32-favicons-browserconfig-manifest)に記載されています。Faviconの作り方も書いてあって助かる。

ちなみにFaviconを表示したい場合はGithub PagesをUser/Organization Pages(URLを```[https://<USERNAME|ORGANIZATION>.github.io/]```とする)で作らないとFaviconが読み込まれないので注意（ハマったのは内緒（　＾ω＾）・・・）
### Google Adsence
[Githubのイシュー](https://github.com/dillonzq/LoveIt/issues/516)が上がっていて、この内容によるとthemeのテンプレートをカスタマイズして直接修正するしかないそうです。仕方ないので修正対象のテンプレートをlayoutsフォルダにコピーして、直接JavaScriptの読込やGoogle Adsenceタグを張り付ける実装をしました。

### タグ一覧やカテゴリ一覧の文言を日本語にしたい
[デモサイトのタグ一覧](https://hugoloveit.com/tags/)の右上の表示「All Tags」を日本語に変えたかったのですが、ちょっとハマりました。多言語対応として文言が設定されていたので、[4.3 Overwrite Translation Strings](https://hugoloveit.com/theme-documentation-basics/#43-overwrite-translation-strings)を参考にカスタマイズすればよいのですが、[Loveitが日本語に対応していない](https://hugoloveit.com/theme-documentation-basics/#language-compatibility)んですよね。

仕方ないので、config.toml上は```languageCode = "en"```として設定し、em.tomlをカスタマイズして文言を変更しましたが、なんかモヤモヤする。言語コードに何設定されても動くようにしておけばいいのに。直接テンプレートいじって直しちゃったほうが良いかもしれません。

### ソーシャルリンクをProfileに表示したい、日本語フォントに変更したい
[Toru Niinaさまのサイト](https://toruniina.github.io/ja/posts/building-a-website-powered-by-hugo-and-loveit/)を参考にさせていただきました。

### ブログのソースコード
[私のリポジトリへのリンク](https://github.com/direboar/direboar.github.io)を置いておきます。config.tomlの内容まじめによむのつらたん、、となったときのカンニング先としてどうぞ。

### まだハマっていること
以下ができてないです。なぜ？

* ブログの先頭に表示されている「74 words」「One minute」の表示が実際の内容とあってない。どこみてるんだ？？
* lunrによるサイト検索が機能しない。最初ブログ作ったときはちゃんと動いてたみたいなんだけど何故？？
