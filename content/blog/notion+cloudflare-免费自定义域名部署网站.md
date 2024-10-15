---
title: Notion+Cloudflare 免费自定义域名部署网站
date: 2024-10-15T04:18:01.113Z
---

### 提前准备1：Notion 页面

![](https://img.lenband.com/my-img/2024/08/6ef2869ad6f1cfe672bc9a2835310d83.png)

搭建好页面之后 → 发布页面

获取 Notion 链接： https://www.notion.so/reddychen/d2550fd68abb4b05badc99e406f2c738

Notion 网站发布之后，可以点击 `Site settings` 简单设置，比如上传网站的 logo，网站主题配色，功能按钮开关显示以及 SEO。

其实如果对域名没有要求的话，点击网站发布，这样就可以了。把链接分享出去，他人能够正常访问网站。

如果你觉得 Notion 分配的域名不够酷，恰好自己有个域名，又恰好域名 Cloudflare 管理，你想再折腾一下，那么继续往下看👇

### 提前准备2：域名

Cloudflare 我新建主域名下二级域名。

类型：CNAME；名称例如：gallery；内容：notion.so；代理状态：仅代理。

![](https://img.lenband.com/my-img/2024/08/de5a873fd1ad74ca8af9386cf7b35922.png)

### 创建 Workers

创建一个 Workers，填入名称（随便取，能识别即可），点击部署

![](https://img.lenband.com/my-img/2024/08/97a83045146478eb485d22dc2217253a.png)

![](https://img.lenband.com/my-img/2024/08/be29abd9ac1f578d1910e2e2a7fe4649.png)

找到右侧「编辑代码」点击进入，会变成这样一个界面，别慌！

![](https://img.lenband.com/my-img/2024/08/0c05529353181fc779cb11fa7fa11cbb.png)

打开这个网站：https://fruition-stephenou.vercel.app/

**Fruition 是一个免费开源项目，通过 Cloudflare Workers 为 Notion 页面自定义域名。**

![](https://img.lenband.com/my-img/2024/08/634615b9c93b45f02cdd15eafbe1ff52.png)

注意，复制好之后，回到 Cloudflare，将右侧编辑框原代码清空删除，然后把 Fruition 代码粘贴到右侧编辑框中，点击部署。

![](https://img.lenband.com/my-img/2024/08/eed98e57e2f9a3d878410badb961560d.png)

Workers 部分已经完成！

### 设置 Workers 路由

点击 Cloudflare 返回域名界面，进入第一步新建二级域名时的界面。

我在这里差点迷路，域名 Workers 路由和 Workers 是两个工作区。侧面导航功能明显不同，不要搞混。

![](https://img.lenband.com/my-img/2024/08/ec164bbd814ba4397025e74be883c804.png)

选择需要绑定域名的 Workers 路由 → 添加路由。如果你有两个及以上的域名，别进错域名。

![](https://img.lenband.com/my-img/2024/08/89e69c5bf9fb2cfd23fc9418951f60c1.png)

填入域名，注意网址后面加 `/*`，我一开始没加，网页报错无法显示，所以，请加上！worker 就是那个贴代码后部署的 `Workers工程` 

![](https://img.lenband.com/my-img/2024/08/302547fd028f3b53d1beed2cfbe76f2b.png)

🎉 Workers 路由设置完成，如无意外，通过自定义链接，就可以正常访问 Notion 网站了哦。

🔗 https://week.lenband.com/

### 总结自定义域名部署流程

Notion 设计网站发布 → 申请二级域名 → 创建 Workers → Fruition 代码贴入 Workers 并部署 → 回到域名添加 Workers 路由

它的原理就是部署一个 Workers，然后让域名指向它。

比较容易出错的地方就是新手容易搞混 Workers 和 Workers 路由，以及添加路由时，网址后面没有加 `/*`，导致网页无法正常显示。

**下期预告：** 如何打通 Obsidian 和 Notion，在 Obsidian 中编辑文章，然后一键发布文章到用 Notion 搭建的网站。

---

### 参考资料

https://week.lenband.com/

https://fruition-stephenou.vercel.app/

https://dash.Cloudflare.com/3eb515cae1c2eee9d639d654a859e3d2/lenband.com/workers

https://blog.csdn.net/terrychinaz/article/details/112425014