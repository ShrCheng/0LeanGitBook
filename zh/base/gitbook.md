# GitBook 安装
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;GitBook 是开源的, 一个基于 Node.js 的命令行工具, 可使用 Github/Git 和 Markdown 来制作精美的电子书, GitBook 并非关于 Git 的教程.
##### 安装 GitBook
---
 - 安装 gitbook-cli

        npm install -g gitbook-cli

 - 安装 GitBook

        gitbook versions:install 2.4.3

 - 安装 bzip2

        yum install bzip2

 - 安装 glibc

        yum install glibc

 - 下载 phantomjs

        wget http://npm.taobao.org/mirrors/phantomjs/phantomjs-1.9.7-linux-x86_64.tar.bz2

 - 生成 phantomjs 解压包

        bzip2 -d phantomjs-1.9.7-linux-x86_64.tar.bz2

 - 解压 phantomjs

        tar -xvf phantomjs-1.9.7-linux-x86_64.tar

 - phantomjs 加入到环境变量

        echo 'export PATH=/root/phantomjs-1.9.7-linux-x86_64/bin:$PATH' >> /etc/profile

 - 重新配置环境变量

        source /etc/profile

 - 下载 fontconfig

        wget ftp://ftp.icm.edu.pl/vol/rzm5/linux-slc/slc64/x86_64/Packages/fontconfig-2.8.0-3.el6.x86_64.rpm

 - 安装 fontconfig

        rpm -ivh fontconfig-2.8.0-3.el6.x86_64.rpm

 - 安装 pdf 插件

        npm install gitbook-pdf -g

 - 安装 calibre 插件

        sudo -v && wget --no-check-certificate -nv -O- https://raw.githubusercontent.com/kovidgoyal/calibre/master/setup/linux-installer.py | sudo python -c "import sys; main=lambda:sys.stderr.write('Download failed\n'); exec(sys.stdin.read()); main()"

 - 安装 libjpeg

        yum install libjpeg

 - 安装 libjpeg-devel

        yum install libjpeg-devel

 - 安装 libpng

        yum install libpng

 - 安装 libpng-devel

        yum install libpng-devel

 - 安装 libtiff

        yum install libtiff

 - 安装 libtiff-devel

        yum install libtiff-devel

 - 安装 libungif

        yum install libungif

 - 安装 libungif-devel

        yum install libungif-devel

 - 安装 perl-CPAN

        yum install perl-CPAN

 - 安装 ImageMagick

        yum install ImageMagick

 - 安装 libXcomposite

        yum install libXcomposite

 - 检查安装结果

        gitbook versions:print

    输出以下内容:

        GitBook version is 2.4.3

##### 参考资料
---
[安装 GitBook](http://www.ttxit.com/thread-25-1-1.html)<br />
[安装 phantomjs](http://www.ttxit.com/thread-32-1-1.html)