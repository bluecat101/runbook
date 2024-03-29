# 自作コマンドを作ろう
参考::https://qiita.com/yoshiken/items/2b8e6c24d6b95e65b625
    ::https://qiita.com/saki-engineering/items/57956af61c191b0e3282
(PATHのコマンドのみ)

1. ファイルを作る

~/self_command/exe_c
``` sh
#

!/bin/sh
gcc $1
./a.out $2 $3
```
先頭に **#!/bin/sh**を書く

2. 権限の付与をする

chmod a+x exe_c
a+x=権限(authority)を全員に付与

3. PATHを通す

echo $PAThに書いてあるファイルならどこでもOK

~/profile
```sh
export PATH=$HOME/self_command:$PATH
```

ターミナルを再起動して終了

# aliasを用いて自作コマンド
参考::https://eng-entrance.com/linux-command-alias#alias-4
1. aliasに登録する
```sh
alias name='command' #alias 登録名='コマンド;コマンド;...;コマンド'
```
2. 永久化する
<.bashrc>
```sh
alias name ='command'
```
3. resorceする
```sh
source ~/.bashrc
```
# ファイルの転送(scp)
<全て自分のローカル環境から操作する。>
### ローカル環境->リモートへの送信
scp ファイル名 user名@ipアドレス:保存場所

例：：scp ./test.c aaa@123.45.67.89:~/C/
### リモート->ローカル環境への送信
scp user@ipアドレス:ファイルの場所　ローカル環境の保存先

例::scp aaa@123.45.67.89:~/C/test.c ./
(※aaaをユーザー名とする)
補足：：
- フォルダを転送する方法-> -rを付ける
(例:scp -r ./ aaa@123.45.67.89:~/C/)
※aaaをユーザー名とする

- ipアドレスの確認-> ip a