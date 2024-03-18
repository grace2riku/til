# 240318
## フォルダ共有について

[参考にしたサイト](https://isehara-3lv.sakura.ne.jp/blog/2021/08/13/vmware%E3%81%A7%E3%82%B2%E3%82%B9%E3%83%88os%E3%81%A8%E3%81%AE%E3%83%95%E3%82%A9%E3%83%AB%E3%83%80%E5%85%B1%E6%9C%89/)

マウントのコマンドを実行する前にhgfsディレクトリをつくっておく。

```
sudo vmhgfs-fuse -o allow_other -o auto_unmount .host:/ /mnt/hgfs
```

そうするとホストPCのディレクトリを

* mnt/hgfs/共有したディレクトリ名

で共有できた。
