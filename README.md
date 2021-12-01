# bedoom.top（暂停）

<a href="https://github.com/bedoom">
<img src="https://img.shields.io/badge/author-Bedoom-red" alt="author">
</a><a href="./LICENSE">
<img src="https://img.shields.io/badge/license-MIT-blue" alt="license">
</a>

This is Bedoom's Blog. I will share best things with you.

My Personal Website:

Visit => [bedoom.top](https://bedoom.top)（暂停）.

Powered by [Jekyll](http://jekyllrb.com/) & [TeXt Theme](https://github.com/kitian616/jekyll-TeXt-theme).
forked by [tianqi.name](https://tianqi.name)

## 特性

- 响应式
- HTML 语意化
- 皮肤
- 代码高亮主题
- 国际化
- 搜索
- 目录
- 作者（支持多个）
- 附加样式（提示，标签，图片，图标，按钮，栅格等）
- 扩展（音频，视频，幻灯片，在线示例）
- Markdown 增强
- 分享
- RSS

## 安装

下载 [TeXt Theme](https://github.com/kitian616/jekyll-TeXt-theme)主题或者导入仓库。

方法一：下载安装包

<div align=center>    <img width = "100%" height = "100%" style="border-radius: 0.3125em;    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"     src="https://gitee.com/bedoom/images/raw/master/202112011946065.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;"></div> </div>

方法二：点击fork按钮导入仓库。

<div align=center>    <img width = "70%" height = "70%" style="border-radius: 0.3125em;    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"     src="https://gitee.com/bedoom/images/raw/master/202112011949734.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">直接fork</div> </div>

这种方式是最为快捷，但是在gitee上无法fork。这时可以用到方法三。

方法三：

<div align=center>    <img width = "100%" height = "100%" style="border-radius: 0.3125em;    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"     src="https://gitee.com/bedoom/images/raw/master/202112011951119.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">gitee导入</div> </div>

gitee很人性化的设计了从“GitHub/GitLab”导入仓库的功能，可以使用此功能来实现导入。

## 配置

关于具体配置，我推荐去看一下作者的[官方文档](https://tianqi.name/jekyll-TeXt-theme/test/)，写的特别好，我就不再班门弄斧了😁。

具体功能我全部体验了一番，有些许小问题。

* 使用网易云播放音乐时静音。（其他的音乐播放器没试，这个功能有点鸡肋不用也罢）
* 评论提供gitalk性能不够稳定，果然是免费的。。。
* 代码的字体太小（这个可以改变）

其余没有什么问题，总体来说，是一款非常完美的主题，做到了**白嫖用户看VIP视频**的体验。

第二个就是补充一下作者的官方文档中没有讲到的几点。第一，就是对于普通用户来说，需要该那几个配置文件呢？当然config文件当然需要改，除此之外还有下图两个文件也可以改。

<div align=center>    <img width = "70%" height = "70%" style="border-radius: 0.3125em;    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"     src="https://gitee.com/bedoom/images/raw/master/202112012012125.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;"></div> </div>

通过**data**文件夹可以修改license, author, local, navigation, variables。通过名称就可以看出是修改许可证类型，作者，本地语言， 侧边栏内容和变量。

通过**includes**文件夹可以修改有关主题的一些样式，比如上面提到的代码字体太小，就可以在它里面实现。

## 撰写博客

博客必须是md文档，且名称是**时间+名称**的格式。然后放在**post文件夹**下就可以实现。

关于撰写博客的选择，建议是**PicGo+Typora**工具集。**PicGo** 是上传图片到图床的工具（建议图床建在gitee上👀，这样比较方便管理）。**Typora** 是md的好伙伴😼，而且也提供**PicGo** 的图床功能，这简直天作之合😎。

<div align=center>    <img width = "90%" height = "90%" style="border-radius: 0.3125em;    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"     src="https://gitee.com/bedoom/images/raw/master/202112012025323.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;"></div> </div>

如果你觉得每次写文件头太累，可以写一个**Rekefile文件**，参考我的文件，在命名行运行

```
rake post "new post"
```

就可以得到一个md文件，而且自带yaml头文件。

<div align=center>    <img width = "80%" height = "80%" style="border-radius: 0.3125em;    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"     src="https://gitee.com/bedoom/images/raw/master/202112012105890.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;"></div> </div>





## Github与Gitee仓库同步

1. 配置私钥

   为了能让Gitee访问我们的Github仓库，首先要在Gitee中添加一个SSH-key的公钥：

   ```
   ssh-keygen -t rsa -C <你的邮箱>
   ```

   然后将`.pub`结尾的公钥上传到gitee；

   在你需要同步Github仓库中，将私钥上传到这个仓库的Secrets中；

   命名为：`GITEE_PRIVATE_KEY`

2. 配置gitee Token

   为了让Github可以操作Gitee中的仓库等内容，和Github类似，我们还需要一个Gitee中的Token；

   所以在Gitee你的个人设置中创建一个Gitee令牌(私人令牌)。

   <div align=center>    <img width = "80%" height = "80%" style="border-radius: 0.3125em;    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"     src="https://gitee.com/bedoom/images/raw/master/202112012036533.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;"></div> </div>

   然后将gitee token上传到这个仓库的Secrets中。

   命名为：`GITEE_TOKEN`

1. 创建workflow

   分享一下我的模块：

   ```
   on:
     workflow_dispatch:
     schedule:
       - cron: '0 1 * * *'
   
   name: Mirror GitHub Selected Repos to Gitee
   jobs:
     run:
       name: Run
       runs-on: ubuntu-latest
       steps:
       - name: Checkout source codes
         uses: actions/checkout@v2
       - name: Mirror Github to Gitee with white list
         uses: Yikun/hub-mirror-action@master
         with:
           src: github/JasonkayZK
           dst: gitee/jasonkay
           dst_key: ${{ secrets.GITEE_PRIVATE_KEY }}
           dst_token:  ${{ secrets.GITEE_TOKEN }}
           static_list: 'bedoom.github.io'
           mappings: "bedoom.github.io=>bedoom"
           force_update: true
   ```

   如果你需要的话，只需要改变5个变量：

   * schedule： 定义同步时间，采用的**标准UTC时间**。
   * src：github源地址。
   * dst：gitee源地址。
   * static_list：需要同步的仓库，用逗号分割。
   * mappings：同步库映像，因为github中是bedoom.github.io，而gitee中默认是bedoom，所以要同步。

## TODO

由于不能自定义域名，因此gitee和github需要两个地址才可以，暂时做一个备份吧😁