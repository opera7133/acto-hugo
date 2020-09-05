---
title: 自宅鯖を立てた
slug: my-server
date: 2020-04-02T08:09:00.000Z
image: /img/route.png
categories:
  - サーバー
archives:
  - 2020/04
---
これといった意味はない（）\
自宅鯖って…なんかいいよなぁと思っていたらいつのまにか作っていました。\
簡単ですが今運用しているサーバーについて解説します。

## 図

![](https://accessto.net/wp-content/uploads/2020/04/de1.png)

## 解説

Raspberry pi 3 model b+とLS-VLを使用しています。\
ただCPUもメモリも非力なのでウェブサーバーとして使っています。\
LS-VLは振動対策のために下に空間を空けていますが、音がうるさいです。

### Raspberry pi

| OS  | Raspbian (Buster) |
| --- | ----------------- |
| 用途  | Nextcloud         |

### LS-VL

| OS  | Debian (Buster) |
| --- | --------------- |
| 用途  | WordPress       |

## LS-VLについて

Raspberry piは皆さんご存じだと思いますが、LS-VLについてはどうでしょうか。\
LS-VLは、たしか2010年ぐらいにBuffaloから発売されたNASです。\
家にあったのは1TBモデルでした。\
最近発掘して、何に使うか悩んでいましたが、こんな記事をみてやるしかないと思いました。

リンクステーション LS-XHL(またはLS-VL)にDebian 9 (stretch)をクリーンインストール その1\
<https://wv4short.com/installing_debian_9_to_linkstation_ls-xhl_ls-vl_part1/>

ちなみに入れたDebianのバージョンはBusterです。\
[Buffaloイメージ](http://ftp.jp.debian.org/debian/dists/buster/main/installer-armel/current/images/kirkwood/network-console/buffalo/ls-vl/)は探せば出てきます。

NginxはRaspberry piの方法をみながらビルドしました。

## 今後

将来的にはマイクラサーバーを運用できたらいいな程度に思ってます。\
できるだけ消費電力の少ないやつで。（Raspberry pi 4とか）