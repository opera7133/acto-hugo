---
title: ブログをWordpressからHugoに移行した
slug: wordpress-hugo
date: 2020-09-05T10:45:57.178Z
image: /img/wp-hugo.png
categories:
  - ブログ
archives:
  - 2020/09
---
今までブログ用にWordpressを使ってきましたが、いちいち管理するのが面倒になってきたのでHugo + Netlify CMSの環境に移動させました。

## どうして移行したのか

普段はClassic Editorを使用して記事を書いているのですが、最近Wordpressの方はGutenburgを推してくるようにました。あれ、正直言って見づらいんですよね。あと超大量のボット。wordpressの管理画面にアクセスしてくるボットをIP Geo Blockで遮断していましたが、なかなかセキュリティ的にも安心できません。（過去にデータベース書き換え、記事の勝手な追加などありました）

## Ghostを使いたかった

最初はGatsby + Ghostでサーバーを立てようと思っていました（過去形）。ただ、herokuでGhostサーバーを立てるのは無理があるし、自宅鯖はうまく動かないし、Gatsbyのスターターに興味を引くものがなかったりで諦めました。Ghost自体はUIがすごいきれいだったんですけどね...

## Hugoを使おう

この前自分で作ったHugoテーマの[Blond](https://github.com/opera7133/Blonde)eを使ってサイトを作りました。（ちなみにこのテーマはyStandardぐらいシンプルなテーマを目指して作りました。）

サイトを作るにあたって、色々あったバグ類を修正して、機能をたくさん追加しました。ただし、元のサイトから記事をすべて移行するのはきつかったので、割とアクセス数が多めの記事と最近の記事だけ移行させました。

## Netlify CMS

先ほども言っていたGhostやシンプルなStrapiなど他にもいろいろなHeadless CMSはありますが、いちいちホストしなくてよいNetlify CMSを使用しました。もうGhostで痛い目を見たので...