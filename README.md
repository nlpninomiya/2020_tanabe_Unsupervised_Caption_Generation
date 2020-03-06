# 2020_tanabe_Unsupervised_Caption_Generation

show attend and tellによるキャプション生成モデルとHDGANによる画像生成モデルを組み合わせた教師無し学習を行う。

Caltech-UCSD Birds-200-201データセットを対応関係を取り除いて使用する。

# 実行方法

画像の自己符号化器を初期化

``` device=0 sh initialize_image.sh ```

キャプションの自己符号化器を初期化

``` device=0 sh initialize_lstm.sh ```

初期化後のモデルを利用して教師無し学習

``` device=0 sh train.sh ```

# 補足

画像生成モデルはHDGANを使用していますが、Text-To-Imageタスクの他のGANを使用してもいいと思います。
