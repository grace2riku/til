# 240319

## boost1.74（古いバージョン）をUbuntu 22.04にインストールした方法

* ここからboost_1_74_0.zipをダウンロード、解凍する。

https://sourceforge.net/projects/boost/files/boost/1.74.0/

* ここから

https://sourceforge.net/projects/boost/files/

boost のリンクをたどり、1.74.0を選択した。


* Linuxの以下のディレクトリ（/usr/local/include）にコピーした。

```
sudo cp -r boost_1_74_0/boost /usr/local/include
```

* RXのプロジェクトでboost1.74が指定されていたため古いboostをインストールする必要があった。
