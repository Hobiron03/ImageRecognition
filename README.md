# Python3による画像認識プログラム

これは、与えられた大量の画像を学習し、入力として与えられた新たな画像に対して学習した画像と一致しているか確かめることができるプログラムです。

## 実行環境
Python 3.6.2
TensorFlow 1.3.0

## 使い方
学習に使うデータと学習結果のテストに使うデータの２つを7:3ぐらいの割合で用意しておいてください。

まず、openCVを使って画像から顔だけをトリミングを行う。処理はtirm.pyというプログラムで行う。

```
$ python3 trim.py
```

学習を行うには、trainingというディレクトリを作成し、その中のtrain.txtに学習用のデータの画像のパスを記述、test.txtにテスト用のデータの画像パスを記述する必要があります。

そこで、
```
$ python3 classification-train.py
```
を実行するとtrain.txtに画像のパスを記述することができます。名前には区別のため添え字が付きます。
さらに、


```
$ python3 classification-test.py
```
を実行するとtest.txtにテスト用の画像のパスを記述できます。

ここまで準備は完了です。

```
$ python3 train.py
```

を実行し学習を行います。

最後に、
```
$ python3 test.py 判定したい画像
```
これで、学習モデルから結果を返してくれます。
