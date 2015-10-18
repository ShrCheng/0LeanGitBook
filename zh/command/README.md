# 第二章&nbsp;&nbsp;&nbsp;GitBook 命令解析
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;GitBook 提供了众多的命令行命令, 让可以通过熟悉的 command 命令进行操作 GitBook.常用命令有以下几种: init(初始化), install(安装), serve(服务), build(生成) 等各种命令.
##### 获取 GitBook 系统命令
---
    gitbook --help

出现以下窗口:

    Usage: gitbook [options] [command]
    
    Commands:

    versions                          已安装的版本列表
    versions:print                    输出当前已安装的版本
    versions:available                可用的最新版本列表
    versions:install [version]        安装指定的版本
    versions:link [version] [folder]  链接到本地文件夹的版本
    versions:uninstall [version]      卸载指定的版本
    help                              指定版本的命令列表
    *                                 运行一个指定版本的命令

    Options:

    -h, --help                        输出使用信息
    -V, --version                     输出版本信息
    -v, --gitbook [version]           指定使用的 GitBook 版本
    -d, --debug                       启用详细的错误

##### 获取 GitBook 命令
---
    gitbook help

出现以下窗口:

    build [book] [output]   生成图书
      --format   生成图书格式(默认值是为网站;可生成网站,JSON,电子书)
      --log 	 显示调试日志级别(默认为info;可用debug, info, warn, error, disabled)

    pdf [book] [output]     生成 pdf 图书
      --log 	 显示调试日志级别(默认为info;可用debug, info, warn, error, disabled)

    epub [book] [output]    生成 epub 图书
      --log 	 显示调试日志级别(默认为info;可用debug, info, warn, error, disabled)

    mobi [book] [output]    生成 mobi 图书
      --log 	 显示调试日志级别(默认为info;可用debug, info, warn, error, disabled)

    serve [book] 	       根据文件夹生成图书服务
      --port 	 该图书服务监听的端口(默认为4000)
      --lrport    对于livereload服务器监听端口（默认为35729）
      --watch 	启用/禁用文件监控（默认为启用）
      --format    生成图书格式(默认值是为网站;可生成网站,JSON,电子书)
      --log 	  显示调试日志级别(默认为info;可用debug, info, warn, error, disabled)

    install [book] 	     安装插件依赖包

    init [directory] 	   创建基于summary.md内容的文件和文件夹