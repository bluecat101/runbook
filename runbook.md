# 自作コマンドを作ろう
参考::https://qiita.com/yoshiken/items/2b8e6c24d6b95e65b625
    ::https://qiita.com/saki-engineering/items/57956af61c191b0e3282
(PATHのコマンドのみ)

1. ファイルを作る

~/self_command/exe_c
``` sh
#!/bin/sh
gcc $1
./a.out $2 $3
```
先頭に **#!/bin/sh**を書く

2. 権限の付与をする

chmod a+x exe_c
a+x=権限(authority)を全員に付与

3. PATHを通す

each $PAThに書いてあるファイルならどこでもOK

~/profile
```sh
export PATH=$HOME/command:$PATH
```

ターミナルを再起動して終了
