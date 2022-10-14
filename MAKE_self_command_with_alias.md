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
