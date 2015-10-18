# Node.js 安装
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Node.js是一个基于Chrome JavaScript运行时建立的平台,用于方便地搭建响应速度快,易于扩展的网络应用.Node.js 使用事件驱动,非阻塞I/O模型而得以轻量和高效,非常适合在分布式设备上运行的数据密集型的实时应用.
##### 在线安装
---
    yum install nodejs
##### 离线安装
---
 - 下载 Node.js 安装包
    
        wget http://nodejs.org/dist/v0.10.28/node-v0.10.28-linux-x64.tar.gz

    出现以下错误时:
        wget Command not found

    执行安装 wget 命令
    
        yum install wget

 - 解压 Node.js 安装包

        tar -xvzf node-v0.10.28-linux-x64.tar.gz

 - 将 Node.js 路径加入到环境变量中

        echo 'export PATH=/root/node-v0.10.28-linux-x64/bin:$PATH' >> /etc/profile

 - 重新加载环境变量

        source /etc/profile

 - 检查 Node.js 是否安装成功

        node -v
        
    输出以下内容:
    
        v0.10.23

 - 测试 Node.js 环境,新建 test.js 文件,文件中加入以下内容
        console.log('Test Node.js Environment');

 - 运行 test.js 文件

        node test.js
        
    输出以下内容:
    
        Test Node.js Environment
        
        
##### 参考资料
---
[Node.js 离线安装](http://www.ttxit.com/thread-24-1-1.html)<br />