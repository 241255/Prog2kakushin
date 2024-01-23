# 問題1
## 概要
このプログラムは、読み込んだ料理の栄養価一覧表から1日の必要カロリー量を満たす献立を自動で生成するプログラムです。

## なぜこれを作ったのか
自分で1から3食分の献立を考えるのがめんどくさくなったため。

また、自分で献立を考えるうえで、摂取している食事のバランスが悪いらしく慢性的な体調不良に悩まされたため。

## 事前準備
* 料理の栄養価一覧表をネットワーク上からダウンロードしておく必要があります。

ダウンロード:
https://data.bodik.jp/dataset/402036_0009100_00005

## 入力と出力
性別区分を入力する。

性別区分に応じた1日の必要カロリー量での3食分の献立が自動で出力される。

※3食分の献立で1日の必須カロリー量に達していない場合、追加で補填食品のおすすめを出力される。

## 反省点
反省点は主に2点。
* 1日の必要カロリー量を満たすという1点の条件を満たせばたんぱく質や脂質などといった各栄養素のバランスが乱れても問題にならないというものとなってしまった
* 読み込んだ料理の栄養価一覧表に含まれる食品の種類が少なく献立のバリエーションに限界があった

今後は、
* 各栄養素の上限値なども条件に入れ、RFCバランスなどにも配慮した献立を作れるようにする
* 料理のバリエーション豊かなファイルを使用可能な状態に加工できるようにする

という2つのことを意識して改良していきたい。

# 問題2
## 概要
このプログラムは、読み込んだ2つのcsvファイル(dataとdata2)から行列の任意の四則演算を行いcsvファイル(r_data)に出力するプログラムです。

## なぜこれを作ったのか
簡単な計算でのミスを減らすために計算結果を確認をできるようにするため。

## 事前準備
* 計算したい行列の要素を2つのcsvファイル(dataとdata2)に入力しておく必要があります。

* 要素を持たない空のcsvファイル(r_data)を用意しておく必要があります。

**※r_dataと名前を付けた空のexcelを用意するだけで大丈夫です。**

## 入力と出力
計算区分を入力する。

計算区分に応じた結果を自動で出力し、csvファイル(r_data)に結果が保存されます。

## 反省点
反省点は主に2点。
* 簡単な四則演算以外の計算を盛り込むことができなかった
* ファイルの保存が適切に行われないことが度々あった

今後は、
* 逆行列の計算などバリエーション豊かな計算が行えるようにする
* ファイルの保存が適切に行えるように、また保存が重複してしまわないようにする

という2つのことを意識して改良していきたい。


# 問題3
## 概要
このプログラムは、入力された任意の画像から人の顔の顔と目の位置を自動的に検出するプログラムです。

## 事前準備
* 人の顔の画像or写真を用意しておく必要があります。

写真引用元:https://www.photo-ac.com/main/genface

* 処理に伴い「haarcascade_frontalface_alt.xml」と「haarcascade_eye.xml」という2つのファイルを事前にダウンロードしておく必要があります。

ダウンロード:https://github.com/opencv/opencv/tree/master/data/haarcascades

## 入力と出力
事前に用意した画像or写真を読み込むことで、顔の部分を黒い線で、目の位置を白い線で自動的に囲むことができます。

## 備考
**※現在エラーが発生しており正常に動作しません。**
