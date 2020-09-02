---
author: "wamo"
title: "h5aiでインデックスを見やすくする"
image: "img/h5ai.png"
draft: false
date: 2020-08-07
description: ""
categories: ["サーバー"]
archives: ["2020/08"]
---
h5aiというサーバーのインデックスページをきれいにできるものがあります。  
これはapacheとnginxに対応しているので、これを使ってリポジトリとかファイルとかを置いてある鯖を見やすくしましょう。  

## 導入
```bash
DOC_ROOT
 ├─ _h5ai
 ├─ your files
 └─ and folders
```
まずはサイトのルートディレクトリにh5aiを解凍します。  
念のためサーバーソフトを再起動して、以下のURLにアクセスします。  
  
http://（あなたのドメイン）/_h5ai/public/index.php  
特に設定をいじっていない場合はパスワードはないので、そのままLoginを押しましょう。  
とりあえず全部緑文字になっていれば大丈夫です。  

私の環境ではCPUが32bitだったためPHPも32bitです。  
なお、PHPが32bitだと2GB以上のファイルのファイルサイズが表示できません。  

### Apacheの場合  
もしhtaccessを使えるようにしてあれば、以下の記述を追加してください。  
```bash
DirectoryIndex  index.html  index.php  /_h5ai/public/index.php  
```
### Nginxの場合
nginx.confまたは各サイトごとのコンフィグファイルのlocation内に以下の記述を追加してください。  

```bash
index  index.html  index.php  /_h5ai/public/index.php;
```
## メディア
動画ファイルの再生にはffmpeg、PDFにはgmなどのソフトを入れる必要があります。  
また、_h5aiフォルダのpublic/cacheおよびprivate/cacheを777に設定しておくとエラーが出ません。