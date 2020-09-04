---
title: きつねゆっくり素材をYMM4用に変換するやつ
slug: kitsune-ymm4
date: 2020-03-12T10:23:00.000Z
image: /img/ymm4_chara.png
categories:
  - ソフト
archives:
  - 2020/03
---
YMM4が単体出力できることを知って、最近はそっちを使うようにしています。\
しかし、YMM4にはYMM3ほど簡単にキャラ素材を入れられないことが分かりました。\
なのでPythonで適当にコード書いて自動で変換してくれるやつを作りました。（目と口専用です。）

### ダウンロード

動作の保証はしません。\
[YMM4Chara.zip](https://dl.accessto.net/dl/software/YMM4Chara.zip)



### ソースコード

[YMM4K – pastebin.com](https://pastebin.com/ATiGiDFS)\
[YMM4F – pastebin.com](https://pastebin.com/e6CbaAKR)

### 仕組み

動作フォルダを判別し、口の場合は00a→00.1のように、目の場合は00a→00.5のように処理させました。\
このコードをもっとよくしてくれたらうれしいです。（需要があるかどうかはわかりませんが…）

### 参考

<https://qiita.com/yaju/items/9b81ef370bdc02b49fdd>