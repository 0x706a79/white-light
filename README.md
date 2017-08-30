# White Light

一个基于cactus-light简单修改、简洁适用的 [Hexo](http://hexo.io) 主题，适用于个人博客。

[Demo](https://blog.yangjiye.top)

## Summary

- [General](#general)
- [Features](#features)
- [Install](#install)
- [Configuration](#configuration)
- [License](#license)

## General

- **Version** : 2.0
- **Compatibility** : Hexo 3 or later

## Features

- 自适应
- 支持Disqus、友言
- 谷歌 analytics
- 代码高亮
- 阅读量统计
- Projects list

## Install
1. In the `root` directory:

    ```git
    $ git clone https://github.com/Windysec/white-light.git themes/white-light
    $ npm install hexo-pagination --save
    ```

2. Change the `theme` property in the `config.yml` file.

    ```yml
    # theme: landscape
    theme: white-light
    ```

3. Run: `hexo generate` and `hexo server`

## Configuration

### Navigation

在主题的 `_config.yml` 中设置导航菜单:

  ```
  nav:
    Home: /
    About: /about/
    Writing: /archives/
    Links: /links/
    Projects: http://github.com/gabithume
    LINK_NAME: URL
  ```

### Blog posts list on home page

关于文章首页，有两项设置

  - 默认展示五篇最近的文章

  ```
  customize:
    show_all_posts: false
    post_count: 5
  ```

  - 展示所有文章

  ```
  customize:
    show_all_posts: true
  ```

### Projects list

创建一个项目文件 `source/_data/projects.json`.

  ```json
  [
      {
         "name":"Hexo",
         "url":"https://hexo.io/",
         "desc":"A fast, simple & powerful blog framework"
      },
      {
         "name":"Font Awesome",
         "url":"http://fontawesome.io/",
         "desc":"The iconic font and CSS toolkit"
      }
  ]
  ```

### Social media links

在主题中增加社交链接，修改`_config.yml`:

  ```
  customize:
    social_links:
      github: your-github-url
      twitter: your-twitter-url
      NAME: your-NAME-url
  ```

where `NAME` is the name of a [Font Awesome icon](http://fontawesome.io/icons/#brand).

### RSS

Set the `rss` field in the theme's `_config.yml` to one of the following values:

1. `rss: false` will totally disable rss (default).
2. `rss: atom.xml` sets a specific feed link.
3. `rss:`leave empty to use the [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed) plugin.


### Comments

#### Disqus
首先在disqus中为你的站点创建一个账号: [https://disqus.com/admin/create/](http://disqus.com/admin/create/).

修改 `_config.yml` :

  ```
  plugins:
      disqus_shortname: SITENAME
  ```

`SITENAME` 是你在disqus中设置的站点名.

#### 友言

修改 `_config.yml` :

```
	changyan_appid: appid
	changyan_appkey: appkey
```
### Leancloud Visitors
添加Leancloud统计阅读次数

修改 `_config.yml` :

```
leancloud_visitors:
	  enable: true
	  app_id: 
	  app_key: 
```
### Code Highlighting

Pick one of [the available colorschemes](https://github.com/gabithume/cactus-light/tree/master/source/css/_highlight) and add it to the theme's `_config.yml`:

  ```
  customize:
      highlight: COLORSCHEME_NAME
  ```

## License
MIT
