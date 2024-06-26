# ターゲットボード
* stm32mp157f-dk2
* STM32 MPU ecosystem V5（wiki上部に記載されているバージョン）

# 環境構築手順
PC環境

* https://wiki.st.com/stm32mpu/wiki/PC_prerequisites

を参照。

## Install extra packages

https://wiki.st.com/stm32mpu/wiki/PC_prerequisites

https://wiki.st.com/stm32mpu/wiki/PC_prerequisites#Installing_extra_packages

3.2. Installing extra packages　を参照

* Packages required by OpenEmbedded/Yocto
```
> sudo apt-get update
> sudo apt-get install gawk wget git diffstat unzip texinfo gcc-multilib  chrpath socat cpio python3 python3-pip python3-pexpect 
xz-utils debianutils iputils-ping python3-git python3-jinja2 libegl1-mesa libsdl1.2-dev pylint xterm bsdmainutils
> sudo apt-get install libssl-dev libgmp-dev libmpc-dev lz4 zstd
```

* Packages needed for some "Developer Package" use cases:
```
> sudo apt-get install build-essential libncurses-dev libyaml-dev libssl-dev 
```

* Package for repo (used to download the "Distribution Package" source code):
```
First set python3 as default:  sudo apt install python-is-python3
```

Then follow the installation instructions described in [repo](https://source.android.com/docs/setup/download?hl=ja#installing-repo).

リンク先にインストール方法は書いていない。つぎのコマンドでインストール、パスを通しておく。

```
$ mkdir ~/bin
$ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$ chmod a+x ~/bin/repo
$ export PATH=${PATH}:~/bin
```

* Useful tools:
```
 sudo apt-get install coreutils bsdmainutils sed curl bc lrzsz corkscrew cvs subversion mercurial nfs-common nfs-kernel-server libarchive-zip-perl dos2unix texi2html libxml2-utils
```

## 3.3. Additional configurations↑
https://wiki.st.com/stm32mpu/wiki/PC_prerequisites#Additional_configurations

## 3.4. Seting up Git user information
https://wiki.st.com/stm32mpu/wiki/PC_prerequisites#Seting_up_Git_user_information

## 2. Creating the structure
https://wiki.st.com/stm32mpu/wiki/Example_of_directory_structure_for_Packages#Creating_the_structure

## 5. Installing the OpenSTLinux distribution
https://wiki.st.com/stm32mpu/wiki/STM32MP1_Distribution_Package#Installing_the_OpenSTLinux_distribution

Machines名についてはこちら

https://wiki.st.com/stm32mpu/wiki/OpenSTLinux_distribution#Machines

* stm32mp157f-dk2はstm32mp15-disco

## 2. SDK generation
https://wiki.st.com/stm32mpu/wiki/How_to_create_an_SDK_for_OpenSTLinux_distribution#SDK_generation

```
bitbake -c populate_sdk <image>
```

Image name; example:
* st-image-weston

## SDカード書込みイメージの作成

2. Usage

https://wiki.st.com/stm32mpu/wiki/How_to_populate_the_SD_card_with_dd_command#Usage

