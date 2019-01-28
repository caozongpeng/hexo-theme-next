## Next
<p>NexT 是一个高质量并且优雅的<a href="http://hexo.io">Hexo</a> 主题。这是精心制作做出来的 hexo 主题。</p>

如果你对此主题非常喜欢，欢迎`Star` & `Fork`，非常感谢。

## 预览界面
#### 首页
![index](https://github.com/caozongpeng/github-static/blob/master/hexo-theme-next/index.png)

#### 底部
![footer](https://github.com/caozongpeng/github-static/blob/master/hexo-theme-next/footer.png)
#### 相册
![photos](https://github.com/caozongpeng/github-static/blob/master/hexo-theme-next/photos.png)
#### 文章
![detail](https://github.com/caozongpeng/github-static/blob/master/hexo-theme-next/detail.png)
#### 搜索
![search](https://github.com/caozongpeng/github-static/blob/master/hexo-theme-next/search.png)

## 安装 Installation

**1.** 在终端切换到**hexo 根**目录. 在hexo目录下一定有 `node_modules`, `source`, `themes` 和其他文件夹:
```sh
$ cd hexo
$ ls
_config.yml  node_modules  package.json  public  scaffolds  source  themes
```
**2.** 从 github 上获取主题 。
```sh
$ git clone git@github.com:caozongpeng/hexo-theme-next.git themes/next
```

**3.** 在 **hexo 根目录下** 的配置文件`_config.yml`里设置主题:

    theme: next

## 更新 Update

```sh
$ cd themes/next
$ git pull
```

#### 如何使用这个特性 How to use this feature

1. 请先确保你所使用的 Hexo 版本在 3 以上
2. 在站点的 `source/_data` 目录下新建 `next.yml` 文件（`_data`目录可能需要新建）
3. 迁移站点配置文件和主题配置文件中的配置到 `next.yml` 中
4. 使用 `--config source/_data/next.yml` 参数启动服务器, 生成或者部署。\
   例如: `hexo clean --config source/_data/next.yml && hexo g --config source/_data/next.yml`。

### 支持多国语言, 包括:
:cn: 简体中文 & 繁体中文<br>
:us: 英语<br>
:ru: 俄语<br>
:fr: 法语<br>
:de: 德语<br>
:jp: 日语<br>
:indonesia: 印度尼西亚语<br>
:portugal: 葡萄牙语 (巴西)<br>
:kr: 朝鲜语<br>
:it: 意大利语<br>
:netherlands: 荷兰语

默认语言是英语。

```yml
language: en
# language: zh-Hans
# language: zh-hk
# language: zh-tw
# language: ru
# language: fr-FR
# language: de
# language: ja
# language: id
# language: pt
# language: pt-BR
# language: ko
# language: it
# language: nl-NL
```

在站点配置文件`_config.yml`中可以将语言切换成中文

```yml
language: zh-Hans
```

### 评论支持 Comment support

NexT 已经原生支持 `多说` and `Disqus` 评论系统。

添加以下代码到你的主题配置文件 `_config.yml`:

```yml
duoshuo:
  enable: true
  shortname: your-duoshuo-shortname
```

或者

```yml
disqus_shortname: your-disqus-shortname
```

或者

```yml
# Valine.
# You can get your appid and appkey from https://leancloud.cn
# more info please open https://valine.js.org
valine:
  enable: true
  appid:  # your leancloud application appid
  appkey:  # your leancloud application appkey
  notify: false # mail notifier , https://github.com/xCss/Valine/wiki
  verify: false # Verification code
  placeholder: 正确填写邮箱, 才能及时收到回复哦♪(^∇^*) # comment box placeholder
  avatar: mm # gravatar style
  guest_info: nick,mail,link # custom comment header
  pageSize: 10 # pagination size
```


### 标签页 Tags page

> 添加一个标签页面，里面包含您网站中的所有标签。

- 创建一个名为 `tags` 页面

        hexo new page "tags"

- 编辑标签页, 设置页面类型为`tags`.

        title: All tags
        date: 2014-12-22 12:39:04
        type: "tags"

- 添加 `tags` 到主题配置文件 `_config.yml` 里:

        menu:
          home: /
          archives: /archives
          tags: /tags

### 分类页 Categories page

> 添加一个分类页面，里面包含您网站中的所有分类。

- 创建一个名为 `categories` 页面

        hexo new page "categories"

- 编辑分类页, 设置页面类型为 `categories`.

        title: All categories
        date: 2014-12-22 12:39:04
        type: "categories"

- 添加 `categories` 到主题配置文件 `_config.yml` 里:

        menu:
          home: /
          archives: /archives
          categories: /categories

### 社交媒体 Social Media

NexT 可以自动添加链接到您的社交媒体帐户里:

```yml
social:
  GitHub: https://github.com/caozongpeng || github
  CSDN: https://blog.csdn.net/qq_22067469
  E-Mail: mailto:kyriecao@163.com || envelope
  Resume: https://caozongpeng.github.io
  #Google: https://plus.google.com/yourname || google
  #Twitter: https://twitter.com/yourname || twitter
  #FB Page: https://www.facebook.com/yourname || facebook
  #VK Group: https://vk.com/yourname || vk
  #StackOverflow: https://stackoverflow.com/yourname || stack-overflow
  #YouTube: https://youtube.com/yourname || youtube
  #Instagram: https://instagram.com/yourname || instagram
  #Skype: skype:yourname?call|chat || skype
```

### Feed 链接 Feed link

> 显示 feed 链接。

在主题配置文件`_config.yml`里设置`rss` , 如下所示:

1. `rss: false` 会禁用 feed 链接。
2. `rss:  ` 使用站点 feed 链接。这是默认的选项。

    按照插件[hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed)的README中的安装说明进行操作。在完成这个插件的配置后，Feed链接也生成好了

3. `rss: http://your-feed-url` 设置你的 feed 链接.

### 内置5种代码高亮主题 Up to 5 code highlight themes built-in

NexT 使用的是 [Tomorrow 主题](https://github.com/chriskempson/tomorrow-theme) ，一共有5种主题供你选择。
Next 默认使用 `normal`. 下面是 `normal` 和 `night` 主题的预览:

![Tomorrow Normal Preview](http://iissnan.com/nexus/next/tomorrow-normal.png)
![Tomorrow Night Preview](http://iissnan.com/nexus/next/tomorrow-night.png)

查看更多信息点击[Tomorrow 主题](https://github.com/chriskempson/tomorrow-theme)。

## 配置 Configuration

NexT 的配置很少

```yml

# Menu configuration.
menu:
  home: /
  archives: /archives

# Favicon
favicon: /favicon.ico

# Avatar (put the image into next/source/images/)
# can be any image format supported by web browsers (JPEG,PNG,GIF,SVG,..)
avatar: /default_avatar.png

# Code highlight theme
# available: normal | night | night eighties | night blue | night bright
highlight_theme: normal

# Fancybox for image gallery
fancybox: true

# Specify the date when the site was setup
since: 2013

```
更多配置请详细查看`_config.yml`文件

