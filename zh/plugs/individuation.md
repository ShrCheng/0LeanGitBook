# 个性化
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;GitBook 会提供用户自定义书籍的设置,那么这个时候就需要我们在书籍的根目录下创建一个名为 book.json 的文件,该文件中存放的就是书籍个性化的设置.比如设置书籍标题,作者,引入插件等等.
##### 本书的 book.json
---

```
{
    "author": "ShiCheng",
    "output": null,
    "generator": "site",
    "title": "从零学习 GitBook",
    "description": "本书将带您从零学习 GitBook, 让您成为写书高手",
    "isbn": null,
    "extension": null,
    "variables": {},
    "plugins": [
                "mermaid-2"
                ],
    "pluginsConfig": {
        "mermaid-2": {
            "theme": "forest"
        },
        "links": {
            "sidebar": {
                "天天学IT-博客": "http: //blog.ttxit.com",
                "天天学IT-论坛": "http: //www.ttxit.com"
            },
            "sharing": {
                "google": null,
                "facebook": null,
                "twitter": null,
                "weibo": null,
                "qq": "http: //www.qq.com",
                "all": null
            }
        }
    }
}
```

标题|语义
---|---
author|书籍作者
generator|生成的类型
title|书籍标题
description|书籍描述
plugins|插件
pluginsConfig|插件配置
links|链接