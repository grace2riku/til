# ターゲットボード
* I-Pi LEC-IMX8MP-Q-N-2G-32G-BW/US（メモリ: 2G）

# 環境構築手順
詳細はつぎのリンクを参照のこと
* [How to Build Yocto](https://www.ipi.wiki/pages/imx8mplus-docs?page=HowToBuildYocto.html)

https://www.ipi.wiki/pages/imx8mplus-docs?page=HowToBuildYocto.html

```
export PATH=${PATH}:~/bin
```

```
repo init -u https://github.com/ADLINK/adlink-manifest -b lec-imx-yocto-kirkstone -m adlink-lec-imx8mp-yocto-kirkstone_1v0.xml
```

```
repo sync
```

```
MACHINE=lec-imx8mp DISTRO=fsl-imx-wayland source adlink-imx-setup-release.sh -b build_dir
```

```
vi build_dir/conf/local.conf
```

* viはoでカーソル行のつぎに追加できる。
* Gで末尾に移動。

```
# sets the LPDDR4 DRAM size, available options are: LPDDR4_2GB, LPDDR4_4GB, LPDDR4_8GB
UBOOT_EXTRA_CONFIGS = "LPDDR4_2GB"
```

コア数が少ないマシンだったらつぎをbuild_dir/conf/local.confに定義する
```
BB_NUMBER_THREADS = "1"
PARALLEL_MAKE = "1"
```

```
bitbake imx-image-multimedia
```

### Goal
つぎにimageができるとのこと。

imx-yocto-bsp/<build_dir>/tmp/deploy/images/lec-imx8mp/
