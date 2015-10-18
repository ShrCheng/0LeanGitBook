# 服务 serve
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;serve 服务是将书籍转换为静态网站,供用户在线查看预览.当用户选择的图书没有生成静态网站时,调用 serve 会自动在该书籍目录下生成 _book 文件夹并生成静态页面.
##### 命令格式
---

    build [book] --port 4000 --lrport 35729 --watch true --format website --log info

##### 生成预览网站
---
    gitbook serve testBook/

生成过程:

    Live reload server started on port: 35729
    Press CTRL+C to quit ...
    
    info: loading book configuration....OK 
    info: load plugin gitbook-plugin-highlight ....OK 
    info: load plugin gitbook-plugin-livereload ....OK 
    info: >> 2 plugins loaded 
    info: start generation with website generator 
    info: clean website generator
    info: OK 
    info: generation is finished 

    Starting server ...
    Serving book on http://localhost:4000
    
当我们使用浏览器打开 http://localhost:4000 页面时,会看到该书籍的内容,使用 **CTRL+C** 退出预览服务

##### 生成指定端口的预览网站
---
    gitbook serve testBook/ --port 5000
    
生成过程:

    Live reload server started on port: 35729
    Press CTRL+C to quit ...

    info: loading book configuration....OK 
    info: load plugin gitbook-plugin-highlight ....OK 
    info: load plugin gitbook-plugin-livereload ....OK 
    info: >> 2 plugins loaded 
    info: start generation with website generator 
    info: clean website generator
    info: OK 
    info: generation is finished 

    Starting server ...
    Serving book on http://localhost:5000
    
这时浏览器访问的地址端口已经改变为我们指定的端口

##### 启用文件监控
---
    gitbook serve testBook/ --port 5000 --watch true
    
生成过程:

    Live reload server started on port: 35729
    Press CTRL+C to quit ...

    info: loading book configuration....OK 
    info: load plugin gitbook-plugin-highlight ....OK 
    info: load plugin gitbook-plugin-livereload ....OK 
    info: >> 2 plugins loaded 
    info: start generation with website generator 
    info: clean website generator
    info: OK 
    info: generation is finished 

    Starting server ...
    Serving book on http://localhost:5000
    
貌似没有任何反应,其实是服务器对各文件进行了监控.当我们在线修改书籍文件时,网站内容也会重新部署.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;将图书运行为服务时默认端口为 **4000**,系统监控的端口默认为 **35729** (在此我们没有进行测试,其效果和 --port 一致,只是系统监控改变成了指定的端口)