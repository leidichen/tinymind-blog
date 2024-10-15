---
title: 如何用五分钟搭建一个memos
date: 2024-10-15T04:07:42.386Z
---


### 使用 Gitblog 搭建一个很酷 Memos

GitHub 新建一个专门存放 memos 仓库，只需用到 Issues 。打开 gitblog 网站，创建，选择一个刚才创建的仓库。填入 blog 名称，上传一个网站图标，完事！

简单到令人不敢相信。

当然，在 GitHub 的 Issues 写博客有点怪怪的，毕竟这种毫无美感的文字排版未免有些不尽如人意，因此我想到可以把它当作 memos，不必通过 docker 安装 [离线memos](https://github.com/usememos/memos?tab=readme-ov-file) 项目，几分钟搞定的事情就不要复杂化。

你可以把它当作一个私人朋友圈，如果不想公开，直接把项目一关即可。

原理很简单，把 GitHub Issues 转换成一个漂亮博客页面，后台也有相当美观的数据展示。

![](https://img-1259210397.cos.ap-guangzhou.myqcloud.com/qnlg7.png)

Gitblog 安装选择指定仓库之后，自动配发一个仓库名称的外链。我知道，域名这种事情完全难不倒你，开发者免费提供绑定域名的服务，只需在域名服务商后面添加一条 CNAME 记录。记得回到 gitblog.io 填入域名地址保存后才生效。

![](https://img-1259210397.cos.ap-guangzhou.myqcloud.com/z5c2k.png)

整个部署过程不会超过十分钟。主题排版确实存在问题，后续或许可以通过修改 CSS 改变样式。

秒开页面，总的体验感就是一个字：快！

🎉欢迎访问开放式 memos，「冷板凳碎语」

>🔗 [https://memos.lenband.com/](https://memos.lenband.com/)

### GitHub 编辑好处

- 可以使用 Markdown 语法
- 不必考虑图片是否上传图床及流量问题
- 右侧还有漂亮的标签，项目，里程碑，进展等联动使用，让普通的一条闪念笔记插上翅膀
- 不用考虑数据备份，Gitblog 项目即使没了，GitHub 仓库 Issues 保留了全部内容
- GitHub 搜索功能强大，不怕笔记多了找不到
- 开放式笔记，评论直接跳转该项目仓库，对笔记有问题， Issues 留言即可，让博客写手体验到程序员开发的快乐

![](https://img-1259210397.cos.ap-guangzhou.myqcloud.com/7z27s.png)

### 没有完美的笔记工具

- 目前感觉不方便支出，需要打开 GitHub 进入 Issues 编辑文字，不像 Flomo 类工具，随时打开记录
- Gitblog 付费版提供了 API，估计就是用于解决快速输入的问题
- 页面主题免费版只有一个，关键在于排版，点进去之后，标题太大，给人一种触目惊心感觉
- 目测似乎只能驾梯使用，如果你连打开 GitHub 都觉费劲，就别玩了

![](https://img-1259210397.cos.ap-guangzhou.myqcloud.com/hrrej.png)

ps.为了加速打开 GitHub Issues，只需在 Quicker 添加一个按钮，想记录时鼠标一甩即可打开，非常快捷。

---

Gitblog 是一款轻量级、简单而强大的博客解决方案

这个工具可以将 GitHub Issues 转成一个静态的博客网站，单个博客使用免费。

官网地址： [https://gitblog.io/](https://gitblog.io/)