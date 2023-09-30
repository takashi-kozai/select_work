# select_work
* このサンプルは、linux の select の動きを確認するために作ったworkです。
* 動作確認環境は、WSL2 + gcc です。

## 前提条件
* 動作確認環境は、WSL2(Ubuntu) です。
* gcc と libc6 が入っている必要があります。
```
sudo apt update
sudo apt install gcc libc6-dev
```
* ポートは、11111 と 22222 を使用しています。すでに使用済みの際は適当に他のポートに変更してください。

## 動作確認
* ターミナル1で、下記を実行
```
> gcc select_sample.c
> ./a.out
```
* ターミナル2で、下記を実行することで、動作確認ができます。
```
> nc -u localhost 11111
(port:11111に送信したい任意の文字列)
^c

> nc -u localhost 22222
(port:22222に送信したい任意の文字列)
^c

