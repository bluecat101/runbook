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