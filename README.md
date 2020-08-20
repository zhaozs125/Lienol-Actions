# Lienol-Actions
基于Lienol大佬的固件云编译
----------
个性化固件说明：
因为实体机编译固件时间较长而且因为网络问题导致编译失败，可以利用github-actions实现自动化云编译  
先在实体机下载下来大佬仓库源码

Lienol大佬仓库：https://github.com/Lienol/openwrt  

首先装好 Ubuntu 64bit，推荐 Ubuntu 18 LTS x64
----------
1.命令行输入 `sudo apt-get update` ，然后输入 `sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch python3.5 python2.7 unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib antlr3 gperf wget swig rsync`

2.使用 `git clone -b dev-19.07 https://github.com/Lienol/openwrt op19` 命令下载好源代码，然后 `cd op19` 进入目录

3.进入固件定制部分

    ./scripts/feeds update -a
    ./scripts/feeds install -a
    make menuconfig


定制完固件后把op19文件夹下的.config中的内容复制到.config中保存后就自动开始编译了,编译成功后下载即可  
![](http://bkt.zblogs.top/img/20200801104043.png)