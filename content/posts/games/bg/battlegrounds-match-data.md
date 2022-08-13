---
title: バトグラの戦績を自動で記録する神ツールの紹介
draft: false #draft。-Dをつけないと表示されない。
date: 2021-12-17T23:34:00+09:00
lastmod: 2021-12-17T23:34:00+09:00
images: [1.png] #twitter cards.

tags: [バトグラ] #tag
categories: [ゲーム] #カテゴリ

featuredImage: "1.webp" #記事の頭に表示する画像。static/posts/<title>/からの相対パス。 
featuredImagePreview: "posts/games/bg/battlegrounds-match-data/1.webp" #ブログ一覧画面に表示するPreview 。staticからの相対パス。

hiddenFromHomePage: false #ホームページ非表示にする場合はtrue
hiddenFromSearch: false #検索結果非表示にする場合はtrue

---
## はじめに
バトグラでレート9000ぐらいをウロチョロしている人間です。
シーズン1の頃からなんとなくやってましたが、シーズン4後半あたりから熱が入り、Twitchの動画をみたりtwitterで流れてくる攻略を見たりするようになりました。
どこの記事だったか忘れましたが、バトグラを上達するには戦績を記録して自分の得意なヒーローを把握するとよい、という話を聞きました。バトグラで戦績を取るアプリを調べてみましたが、大半は自分で戦績を記録する必要があり、面倒くさがりな自分にはちょっと…という感じでした。
一応職業プログラマの端くれの私、デッキトラッカーとうまく連携して自動で戦績取れるツール作れないかな、、となんとなくググったところ、そのものずばりのツールがあった！ということで私はこれを使っています。

### ツールの紹介

PCでバトグラをする場合に使用できます。使い方は簡単で、

1. バトグラ起動
2. Hearthstone Deck Tracker起動
3. バトグラする
これだけです。これだけで、このnote記事のタイトル画像のようなダッシュボードに自分の戦績が表示されます。

こんな画面で、自分のレートの上がり下がりのグラフが見れます。
{{< figure src="2.webp" title="" >}}

左下には、ヒーローごとの平均順位が出ます。俺結構レノで勝ってるんだよな…
{{< figure src="3.webp" title="" >}}

戦闘毎の順位を見ることもできます。
{{< figure src="4.webp" title="" >}}

めちゃくちゃ楽。

## ツールのインストール方法
### 1. Hearthstone Deck Trackerのインストール
ググれば手順落ちてると思います。一応ググって最初に出てきたページのリンク張っておきます。

[【ハースストーン】デッキトラッカーの使い方](https://nekokuma.com/78192/)

### 2. Battlegrounds-Match-Dataのインストール
[Githubのページの記載](https://github.com/jawslouis/Battlegrounds-Match-Data#installation)の通りやればインストールできます。一応解説。

1. 以下のURLから最新の「BattlegroundsMatchData.zip」をダウンロードします。

   https://github.com/jawslouis/Battlegrounds-Match-Data/releases

   画面の一番上にある、以下の「BattlegroundsMatchData.zip」ってとこをクリックします。（何個か同じリンクありますが、最新＝一番上の奴をダウンロードしてください）
{{< figure src="5.webp" title="" >}}
{{< figure src="6.webp" title="" >}}
2. デッキトラッカーを起動し、プラグインの設定画面を開きます。
{{< figure src="7.webp" title="" >}}
3. こんな画面が開くので、この画面に１－１でダウンロードしたファイルを直接ドラッグドロップします。
{{< figure src="8.webp" title="" >}}
4. プラグインの設定をします。↑の画面を閉じて、以下の通りプラグイン設定画面に移動します。
{{< figure src="9.webp" title="" >}}
5. こんな画面が開くので、「Enable Upload to BGStats Battleground」をオンにします（以下の画面の赤丸のところを有効にする。↓の設定は他のところも有効になってますが、しなくていいはずです。）
{{< figure src="10.webp" title="" >}}
6. 以下のURLをブラウザから開きます。```<user>-<id>```のところはバトルタグを入れます。なお、バトルタグの```#```は```-```に変えてください。

```
http://bgstats.cintrest.com/<user>-<id>
```

たとえばバトルタグ：あああ#1234の場合はこんな感じのURLになります。

```
http://bgstats.cintrest.com/あああ-1234
```

ちなみに、戦績の保存方法は

* ダッシュボードにアップロードする（Upload to BgStats Dashboard）
* Google Spreadsheetに保存する（Auto-upload to Google Spreadsheet）
* CSVに保存する

の3つのやり方ができますが、ダッシュボードにアップロードする方法設定すれば使えます。

## バトグラ技術部データ分析班のご紹介

choxさんという方が、このツールを使ってバトルグラウンドプレイヤーの戦績を収集し、データ分析をされているそうです。データ提供をすると、さまざまな分析結果を参照することができます。discordチャンネルのリンクを張っておきますので、興味のある方は参加されてはいかがでしょうか。ちなみに以下のdiscordチャンネルにもBattlegrounds-Match-Dataのインストール手順があります。私の手順じゃわからん！とか、うまくいかん！という方は、こちらのDiscordチャネルの手順を見ていただくとよいかと思います。

[バトグラ技術部データ分析班 Discord Server](https://t.co/GXiyhzSjKB)

## おまけ：twitch配信細々としてます

一応、バトグラをPCでやるときはtwitchで配信してます。酒飲みながらだらだら遊んでるだけですが。ちなみに40代後半バトグラ系バ美肉VTuberという設定です（言いたいだけ）。

ちなみに、現在はBotしか見にきません。一人で黙ってバトグラしてるとなんかさみしいので配信してます。レート9000がギリギリで巣母持て余す雑魚ですが、もし気が向いた方がいたら見に来ていただけると嬉しいです。

[twitch](https://www.twitch.tv/yukari_0918)
