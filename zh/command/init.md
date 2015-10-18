# 初始化 init
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;init 初始化图书,可以根据配置进行初始化,也可以使用默认方式初始化图书. init 初始化图书目录结构以及各文件.
##### 命令格式
---
    install [book]

##### 默认初始化图书
---
    gitbook init testBook

初始化过程:

    info: init book at testBook 
    info: detect structure from SUMMARY (if it exists) 
    info: create SUMMARY.md 
    info: create README.md 
    info: initialization is finished 
    
    Done, without error
    
这时一本名为 testBook 的图书初始化成功.

    tree testBook
    
testBook 目录结构

    testBook
    ├── README.md
    └── SUMMARY.md
    
##### 指定配置文件初始化图书
---
 - 创建 confBook 文件夹

        mkdir confBook

 - 创建图书 README.md 文件

        touch confBook/README.md

 - 创建图书 SUMMARY.md 文件

        touch confBook/SUMMARY.md
        
 - 查看 confBook 文件夹下所有结构

        tree confBook
    
    confBook 目录结构

        confBook
        ├── README.md
        └── SUMMARY.md
    
 - 根据编写的配置初始化 confBook 图书

        gitbook init confBook/
        
    初始化过程:

       info: init book at confBook/ 
       info: detect structure from SUMMARY (if it exists) 
       info: found README.md 
       info: initialization is finished
        
       Done, without error

    这时一本名为 confBook 的图书初始化成功.
    
        tree confBook

    confBook 目录结构

        confBook
        ├── README.md
        └── SUMMARY.md

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;两次初始化结果是一致的,但是唯独不同的是在初始化的过程中未编辑配置文件时,系统会自动创建 README.md 和 SUMMARY.md 配置文件.当编写配置文件后,系统会根据已存在的配置文件进行初始化图书,不会在创建 README.md 和 SUMMARY.md 配置文件.