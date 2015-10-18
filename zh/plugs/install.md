# 插件
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;当我们在书籍中使用到一些第三方的东西时,这时我们把这些东西称之为插件.我们想要使用某种插件时,必须的先安装该插件,然后在书籍的配置中,进行对该插件的引用,以及对该插件的配置.
##### GitBook 插件的安装
---
    npm install gitbook-plugin-mermaid-2 -g

需要注意的是,我们安装插件的时候需要进入 GitBook 的安装目录进行插件的安装,不然后出现无法找到插件的错误.
##### 插件的使用和配置
---
插件的使用和配置很简单,只需要在 book.json 中配置即可.
    
    "plugins": [
        "mermaid-2"
    ],
    "pluginsConfig": {
        "mermaid-2": {
            "theme": "forest"
        }
    }
##### 参考资料
---
[GitBook 插件](https://plugins.gitbook.com/)