# 构建 build
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;build 构建图书,可以将图书构造格式化成各种各样的格式,生成相应的文件及结构目录.构造的格式有:website(静态网站:默认),json(json 格式图书),ebook(ebook 格式图书).
##### 命令格式
---

    build [book] [output] --format [website] --log [info]

##### 默认构造图书
---
    gitbook build testBook/

构造过程:

    info: loading book configuration....OK 
    info: load plugin gitbook-plugin-highlight ....OK 
    info: >> 1 plugins loaded 
    info: start generation with website generator 
    info: clean website generatorOK 
    info: generation is finished 
    
    Done, without error
    
这时一本名为 testBook 的图书构造成功.

    tree testBook
    
testBook 目录结构

    testBook/
    ├── _book
    ├── README.md
    └── SUMMARY.md
    
书籍构造成功后在该书籍文件夹下生成了 _book 文件夹,该文件夹下存放该书籍的所有静态网站页面.
    
##### 构造 json 格式图书
---
    gitbook build testBook/ --format json

构造过程:

    info: loading book configuration....OK 
    info: load plugin gitbook-plugin-highlight ....OK 
    info: >> 1 plugins loaded 
    info: start generation with json generator 
    info: clean json generatorOK 
    info: generation is finished 
    
    Done, without error
    
这时一本名为 testBook 的图书构造成功.

    tree testBook
    
testBook 目录结构

    testBook/
    ├── _book
    │   └── README.json
    ├── README.md
    └── SUMMARY.md
    
书籍构造成功后在该书籍文件夹下生成了 _book 文件夹,该文件夹下存放一个名为 README.json 的文件,该文件保存了 testBook 图书的所有信息.

##### 构造 ebook 格式图书
---
    gitbook build testBook/ --format ebook

构造过程:

    info: loading book configuration....OK 
    info: load plugin gitbook-plugin-highlight ....OK 
    info: >> 1 plugins loaded 
    info: start generation with ebook generator 
    info: clean ebook generatorOK 
    info: write SUMMARY.html 
    info: generation is finished 
    
    Done, without error
    
这时一本名为 testBook 的图书构造成功.

    tree testBook
    
testBook 目录结构

    testBook/
    ├── _book
    │   ├── gitbook
    │   │   ├── app.js
    │   │   ├── fonts
    │   │   │   └── fontawesome
    │   │   │       ├── FontAwesome.otf
    │   │   │       ├── fontawesome-webfont.eot
    │   │   │       ├── fontawesome-webfont.svg
    │   │   │       ├── fontawesome-webfont.ttf
    │   │   │       └── fontawesome-webfont.woff
    │   │   ├── images
    │   │   │   ├── apple-touch-icon-precomposed-152.png
    │   │   │   └── favicon.ico
    │   │   ├── plugins
    │   │   │   └── gitbook-plugin-highlight
    │   │   │       ├── ebook.css
    │   │   │       └── website.css
    │   │   ├── print.css
    │   │   └── style.css
    │   ├── index.html
    │   └── SUMMARY.html
    ├── README.md
    └── SUMMARY.md
    
书籍构造成功后在该书籍文件夹下生成了 _book 文件夹,该文件夹下存放所有有关该书籍的信息.

##### 构造图书增加日志显示
---
    gitbook build testBook/ --format ebook --log warn

构造过程:

    Done, without error

没有任何日志信息输出,由于我们指定日志为 warn 的输出,在构造过程中没有 warn 的日志,故不会输出任何日志信息.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在构造图书时,不指定 format 类型默认为 website 格式.