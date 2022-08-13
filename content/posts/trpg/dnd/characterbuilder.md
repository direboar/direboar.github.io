---
title: D&D 4版のOffline Character Builderについて
draft: false #draft。-Dをつけないと表示されない。
date: 2020-01-19T22:10:00+09:00
lastmod: 2020-01-19T22:10:00+09:00
images: [1.webp] #twitter cards.

tags: [D&D] #tag
categories: [TRPG] #カテゴリ

featuredImage: "1.webp" #記事の頭に表示する画像。static/posts/<title>/からの相対パス。 
featuredImagePreview: "posts/trpg/dnd/characterbuilder/1.webp" #ブログ一覧画面に表示するPreview 。staticからの相対パス。

hiddenFromHomePage: false #ホームページ非表示にする場合はtrue
hiddenFromSearch: false #検索結果非表示にする場合はtrue

---
## はじめに {#はじめに}
Wikipediaによると2014年に米国でD&D５版がリリースされ、既に６年目となりました。そんな今でも魂はD&D４版に惹かれている…これはそんな少数派の人向けのnoteです。

2019年にD&D Insiderがクローズしてしまい、WotCは４版については完全に手仕舞いしたといってよいのかと思います。D&D４版はデータリッチなゲームで、伝説級以降のキャラクター作成はツールがないと現実的ではなく、Insiderのキャラクタービルダーを頼りにしていた方も多いかと思います。キャラクタービルダーを失い、ついに４版から手を引かざるを得ないのでは、、、と考え始めている方もいるかと思います。私は4th cageのキャラクター作成用のExcelシートを主に使用しているのであまり困らないのですが、自分のプレイグループでも困っている人が何人かいました。

米国の４版フリークはどうしてんのかな、あいつらガチ勢だからなんか考えてんじゃないかな、、、と思って適当にググったところ、なんでも「Offlice Character Builder」というものがあるらしい、という情報に至りました。このnoteでは、「Offlice Character Builder」についての紹介をしたいと思います。

ちなみに、「Offlice Character Builder」自体、**権利的にはグレーというか、ほぼアウト**だと思います。また、ウィルス等セキュリティ的な問題が全くないとは断言できません。私の立場としては、ネットなどで調べた情報をここにまとめ、共有することは行いますが、**利用するかどうかは各自、判断してください。**

## Offlice Character Builderとは？ {#OffliceCharacterBuilderとは？}
Insiderのキャラクタービルダーと同等の機能を持つアプリケーションです。Insiderはインターネット上のサービスとして展開されていましたが、「Offline Character Builder」はデスクトップPC上のスタンドアロンアプリケーションとして動作します。そのため、Insiderがクローズされた現在でも動かすことができます。

ネットで集めた断片的な情報からの推測ですが、どうも「Offline Character Builder」はWotCが2009～2010年にかけて提供していた模様です。どのように配布していたのか、有料配布だったかどうかなどは、よくわかりません。当然、現時点では公式からはダウンロードできませんが、米国の有志が**海賊版として**公開しているものがあります。

「Offline Character Builder」は2010年で開発が打ち切られたため、2010年時点でのデータ（PHB3あたり？）までのデータしか登録されていません。ですがそこは米国オタク。ガチ勢な彼らは「Offline Character Builder」に追加データを登録するためのプログラム「[CBLoader](https://github.com/CBLoader/CBLoader)」をOSSで開発してしまいました。これらを併用することで、デスクトップPC上で４版のキャラクター作成を、Insiderとほぼ同じユーザーインタフェースで行うことができます。

なお、「CBLoader」で「Offline Character Builder」に追加するデータは、海賊版の「Offline Character Builder」と一緒に有志が**無断**で公開しており、これを使用する必要があります。（自分で作成するのは非現実的。）実際問題、過去にInsiderに加入していた人であれば、Insiderのデータをダウンロードすることは原理的にはできるはずなのでので問題ないのでは？という**気も**します。まぁ**黒に近いグレーですが。**

なおInsiderで作成したキャラクターデータを、「.dnd4e」形式のファイルで保存している場合、「Offline Character Builder」にロードすることができるそうです！

## インストール方法
さてインストール方法についてですが、、、さすがに直接ここに記載するのはためらわれるので、情報の取得方法を説明するにとどめておきます。なお以下はあくまで2020/1/19時点のものです。現時点でもまだ開発が進められているようなので、最新情報は変わる可能性があります。

1. discordのD&D4eサーバーに加入してください。招待コードを置いておきます。discordをインストールしたうえで、上記のリンクからサーバーに加入してください。
2. 「#resources」チャネルに、「Permanent DM」が2020/1/7に行ったリンク集の投稿を探してください。「CBloader Instructions with Download Link」と記載されているリンクを辿ってください。その先にインストール手順が記載されています。ちょっとはまるかもしれませんが、あとは頑張ってください。手順は英語ですが、そんな難しくないです。なんだったらgoogle翻訳にブチ込みましょう。

注意点として、OSはWindows7以降であれば大丈夫なようです。Windows10の場合は、[ProgramFilesに入れると動かないので、別のディレクトリに入れる必要がある](https://www.enworld.org/threads/d-d-4e-help-me-with-my-cbloader.572722/)みたいです。あと、起動時は必ず「CBLoader.exe」のリンクを実行するようにしてください。デスクトップにできるCharacterBuilderのショートカットを実行しても、古いデータしか参照できません。

## 参考までにスクリーンショットを
{{< figure src="2.webp" title="" >}}
{{< figure src="3.webp" title="" >}}
{{< figure src="4.webp" title="" >}}
{{< figure src="5.webp" title="" >}}

作成できるキャラクターシートはこんな感じです。だいたいInsiderのときと同じですね。

{{< figure src="6.webp" title="" >}}
{{< figure src="7.webp" title="" >}}

以上！
