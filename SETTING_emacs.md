# emacsの設定をする

## やり方
1. .emacsのファイルを作る
2. .emacsに設定を記述する


## 1.emacsのファイルを作る
カレントディレクトリに.emacsのファイルを作る
```sh
$cd
$touch .emacs #touchじゃなくてもemacs .emacsでもOK
```

## 2.emacsに設定を記述する
例えばこんな感じです。
.emacsのファイルに以下を書きます。
```
(global-set-key "\C-h" 'delete-backward-char)
```
これはバックスペースキーを有効にするやり方です。

<意味>
|コマンド|意味|
|--|--|
|global-set-key|全体に設定|
|"\C-h"|ctrlとhで実行|
|'delete-backward-char|実行する内容|

"\C-h"と'delete-backward-charの部分を変えて設定していく。


## 自分の設定
|コマンド|意味|
|--|--|
|(global-set-key "\C-h" 'delete-backward-char)|BackSpaceの有効か|
|(setq make-backup-files nil)|emacsでファイルを作ったときに予備ファイル(#)を作らない|
|(global-set-key "\C-cc" 'copy-region-as-kill)|コピー|
|(global-set-key "\C-cv" 'yank)|貼り付け|
|(global-set-key "\C-cz" 'undo)|戻す|
|(global-set-key "\C-cx" 'kill-region)|切り取り|
|(show-paren-mode 1)|対応する括弧の色付け|
※(\C-ccはctrl-cの後に続けてcを押す)

**<参考になるのはページ>**

https://www.math.s.chiba-u.ac.jp/~matsu/lisp/emacs-lisp-intro-jp.html#SEC_Top

https://uguisu.skr.jp/Windows/emacs.html

**<検索方法>**

emacs lips やりたいこと(ex:切り取り)

## 参考

https://mag.osdn.jp/09/04/23/0834240

https://www.math.s.chiba-u.ac.jp/~matsu/lisp/emacs-lisp-intro-jp.html#SEC_Top