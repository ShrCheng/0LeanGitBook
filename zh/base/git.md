# Git 安装
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Git是一个开源的分布式版本控制系统,用以有效,高速的处理从很小到非常大的项目版本管理.Git 是 Linus Torvalds 为了帮助管理Linux内核开发而开发的一个开放源码的版本控制软件.
##### 在线安装
---
    yum install git

##### 离线安装
---
 - 安装 expat 依赖包

        yum install expat

 - 安装 zlib 依赖包

        yum install zlib

 - 安装 perl 依赖包

        yum install perl

 - 安装 gcc 编译器

        yum install gcc

 - 安装 gcc-c++ 编译器    

        yum install gcc-c++

 - 安装 perl-ExtUtils-MakeMaker 依赖包

        yum install perl-ExtUtils-MakeMaker package

 - 安装 curl-devel 依赖

        yum install curl-devel

 - 下载 git 源码

        wget https://www.kernel.org/pub/software/scm/git/git-2.6.1.tar.gz

 - 解压 git 源码包

        tar -xvzf git-2.6.1.tar.gz

 - 进入 git 目录

        cd git-2.6.1

 - 配置 git

        ./configure

 - 编译并安装 git

        make && make install

 - 检查安装结果

        git --version

    输出以下内容:
    
        git version 2.6.1

 - 初始化 git

        git init

    在初始化的目录下会存在一个名为 .git 的文件夹
    
        drwxr-xr-x.  3 root root   17 10月 14 13:09 .
        dr-xr-x---.  5 root root 4096 10月 14 13:09 ..
        drwxr-xr-x.  7 root root 4096 10月 14 13:09 .git

##### 参考资料
---
[Git 离线安装](http://www.ttxit.com/thread-21-1-1.html)