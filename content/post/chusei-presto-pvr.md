---
title: CHUSEI PVR(Presto! PVR)のプロダクトキーがない時の対処
slug: chusei-presto-pvr
date: 2019-08-08T10:46:00.000Z
image: /img/pvr.png
categories:
  - ソフト
archives:
  - 2019/08
---
久しぶりに掃除をしていたら、ワンセグチューナーを見つけました。\
型番はDS-DT308SV\
株式会社ゾックス（現在ページなし）の販売していた製品のようです。\
ただし、見つけたはいいもののCD-ROMがないため、シリアルキーがわかりません。\
このゾックスという会社はもう存在しないようです。\
どうすればいいのかGoogleで検索してみると、その方法が書いてありました。\
（現在その記事はみつからないため、 サイトごと削除されたのではないかと思われます。）

### 方法

まず、ドライバーをダウンロードします。

WebArchive版\
<https://web.archive.org/web/20160324192508/http://zox-net.com/download/chusei_pvr/exe/chusei_pvr8_32_01.exe>

最初に、ダウンロードしたファイルを実行し、解凍します。 

![](https://accessto.net/wp-content/uploads/2020/04/c00.png)

 

![](https://accessto.net/wp-content/uploads/2020/04/c01.png)

 

![](https://accessto.net/wp-content/uploads/2020/04/c02.png)

 次に、解凍したフォルダの中にある”Setup.exe”を実行する前に、\
PVRフォルダの中にあるLUTRAY.iniを編集します。 

![](https://accessto.net/wp-content/uploads/2020/04/c03.png)

 ファイルの中にOEM-Product-IDというものがあるので、例えばT0000-00000-00000とか入力します。\
保存すれば、正常にインストールができます。 

![](https://accessto.net/wp-content/uploads/2020/04/c04.png)

ある記事ではRegeditで認証させるという方法もあったようですが、私はあまりお勧めしません。