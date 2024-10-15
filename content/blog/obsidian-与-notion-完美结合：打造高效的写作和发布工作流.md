---
title: Obsidian 与 Notion 完美结合：打造高效的写作和发布工作流
date: 2024-10-15T04:19:48.437Z
---

2024 年，Notion 进行了诸多实用功能的更新，包括中文语言、悬浮目录、数据库图表、网站发布以及自动化按钮等。

然而，在国内使用 Notion 时，最大问题在于其速度。当打开一个页面需耗时数秒时，难免令人心生烦躁。

据说为解决这一问题，Notion 官方已经开始部署 CDN 加速服务，预计在 2025 年全面启用， 届时 Notion 使用速度将得到大幅提升。

![](https://img.lenband.com/my-img/2024/09/946c7f4c5811f8d890ae46860abdf8d6.png)

### Obsidian → Notion 流程

有人问，Obsidian 编辑文字有这么强？答案是肯定的。

Obsidian 是目前公认最强文字编辑器之一。强大的双链功能，离线数据的安全性，丰富的插件生态，毫无阻塞感的写作体验，跨平台兼容能力。

我所有笔记，博客，周刊，小说等文字，均在 OB 中创作编辑，但我同时又需要 Notion 数据库，日历以及网站发布功能。

以冷板凳周刊（https://lenband.com/）为例，谈一谈我如何将 Obsidian 和 Notion 联动。

我在 Obsidian 中，专门新建了一个名为「板凳周刊」文件夹，可以对相关内容进行集中管理。将所有文件的标题进行统一化处理，使得整个文件夹中的内容在视觉上更加整齐规范。

![](https://img.lenband.com/my-img/2024/09/ef768a07d57d6a80176a2c29416d84a9.png)

一键发送 Notion 之前，一定要把文章中的图片转为外链，如果你还不清楚什么是图床，请参看 [告别高昂费用：Obsidian 升级免费图床 Cloudflare R2 全攻略](https://lenband.com/Cloudflare-R2) 。

最后，使用 OB 中「Share to Notion」插件，一键同步 Notion。

设若 Notion 这个页面已经处于网站发布状态，请参看 [Notion新功能：一键发布网站，让内容创作更自由](https://lenband.com/Notion-xin-gong-neng--yi-jian-fa-bu-wang-zhan--rang-nei-rong-chuang-zuo-geng-zi-you) 。

**当我同步文章到 Notion 时，那么网站已经同步更新了内容。**

与常规 blog 操作不同，开源免费的通常会把文章通过 GitHub 编译后上传到指定仓库，或者在第三方后台手动上传文章。但如果使用 Notion 一键发布网站，你只需将文章同步到 Notion 就行。

当然，如果你直接在 Notion 编辑文章，那就一步到位了。但如果你像我一样在 Obsidian 中写文章，而发布在 Notion，就需要用到这个创作流程。

### Share to Notion 安装与配置

1.先去 Notion 创建一个集成，名字要记住。这一步是获取一个远程调用 Notion 能力的 API。

https://www.notion.so/profile/integrations

![](https://img.lenband.com/my-img/2024/09/50acdb0f1494d9ae415e8493a90b279b.png)

把这个内部集成密钥保存起来，一会就要用到。

2.在 Notion 中新建一个 page，再新建一个数据库，请使用「数据库-整页」。**数据库的第一列名称必须英文 "Name"，第二列标签名称必须英文"Tags"，否则将同步失败。**

![](https://img.lenband.com/my-img/2024/09/af4fa5d48a0da2e0b1678174eff57006.png)

![](https://img.lenband.com/my-img/2024/09/68799697f588d677226db8636cf19492.png)

3.将此数据库连接到第一步中创建的 Notion 集成。这一步表示这个数据库已经具备远程访问能力。

![](https://img.lenband.com/my-img/2024/09/75f1268be81b54e2efbc13b177b5eb78.png)

4.请务必准确复制数据库 ID，此步骤易出现错误，请瞪大你的眼睛👀！即 `/复制这里中间的数字?v=` 

![](https://img.lenband.com/my-img/2024/09/157d24a344652536bfa64e5da5b77c7d.png)

5.Obsidian 官方插件库搜索 `Share to Notion` 安装启动，或者 GitHub 开源仓库中手动安装。

6.Obsidian 插件中填入 Notion 集成密钥和 Notion 数据库 ID，其他保持默认。重启 Obsidian 。

![](https://img.lenband.com/my-img/2024/09/796b8f0105886a3005413788fb28dd07.png)

7.见证奇迹的时刻到了。

✅ Obsidian 一键同步文章到 Notion
✅ Obsidian 修改文章内容亦可同步更新到 Notion

![](https://img.lenband.com/my-img/2024/09/0032dbe88b623d7f3ce9a9dcc4ae206c.gif)

### 同步成功之后

一旦我们成功建立联结，便可进一步对 Notion 页面进行装修。其可以设计为周刊样式，亦或是博客样式，随心定制。而后使用发布网页功能，便形成了一个一键发布的自动化流程。

例如发布周刊，在 Obsidian 编辑好，点击按钮发送 Notion，完成！

实际上，鉴于文章已然发布，无需再次打开 Notion。若内容需要更新，可在 Obsidian 中进行修改更新，而后再次点击一键发送，Notion 页面内容即会被修改更新。

这是目前我使用过的发布博客最快工作流。

不足之处确实存在。Share to Notion 仅能对应一个 Notion 数据库。倘若既需通过 Obsidian 发布文章至博客，又要发布文章至周刊，目前该插件无法实现此功能。也就是说，Obsidian 仅能对应一个 Notion 数据库。

![](https://img.lenband.com/my-img/2024/09/05b8a84c17248f432287aab6df7a81b2.png)

期望开发者在后续能够添加如下功能：当点击发布按钮时，弹出一个下拉菜单，以供选择发布“博客”或者“周刊”。同时，在插件后台参数中可增加多个数据库 ID 配置。



### 参考链接

https://github.com/EasyChris/obsidian-to-notion

https://github.com/EasyChris/obsidian-to-notion/blob/master/README-zh.md