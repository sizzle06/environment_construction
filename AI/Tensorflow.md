# Tensorflow 導入

機械学習ライブラリのひとつである Tensorflow のインストールからサンプルの実行までを解説する。

## Ubuntu

### 動作確認環境

* OS : Ubuntu 16.04 64bit
* Python : Python 3.5.2
* Python-pip : pip 9.0.1
* Tensorflow : Tensorflow 1.3.0

### Python のインストール

Tensorflow を使用するために、まずは Python をインストールする。
Ubuntu 16.04 では python3 はインストール済み。

インストールされていない場合は、以下のようにインストールする。
<pre>
$ sudo apt-get install -y python3
</pre>

以下のコードでバージョンを確認する。バージョンが確認できたらインストール完了。
<pre>
$ python3 -V
python 3.5.2
</pre>

### pip のインストール
pip とは Pythonのパッケージ管理システムのことである。Ruby でいう Gem のようなもの。
さまざまなパッケージをインストールしたりアップデートする際に利用でき便利。
今回は、Tensorflow のインストールに利用する。

pip のインストールは、ターミナルで以下のコードを打てば良い。
<pre>
$ sudo apt-get install -y python3-pip
</pre>

pip のバージョンが最新ではない場合があるので、アップグレードを実施する。
<pre>
$ pip3 install --upgrade pip 
</pre>

pip のバージョンを確認する。
<pre>
$ pip3 -V
pip 9.0.1
</pre>

### Tensorflow のインストール
準備が整ったので、pip を用いて Tensorflow をインストールする
#### CPU版
<pre>
$ pip3 install tensorflow
</pre>
#### GPU版
<pre>
$ pip3 install tensorflow-gpu
</pre>

### 動作確認
Tensorflow パッケージがインストールされているか確認するため、"Hello, TensorFlow!"と表示するサンプルを試してみる。
以下のように表示されていれば正しく導入できている。
<pre>
$ python3
>> import tensorflow as tf
>> hello = tf.constant('Hello, TensorFlow!')
>> sess = tf.Session()
>> print(sess.run(hello))
b'Hello, TensorFlow!'
</pre>
