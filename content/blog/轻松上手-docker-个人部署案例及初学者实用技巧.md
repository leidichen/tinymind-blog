---
title: 轻松上手 Docker 个人部署案例及初学者实用技巧
date: 2024-10-15T04:17:37.356Z
---


![](https://img.lenband.com/my-img/2024/07/a8f480d08235fbb981154b5d2a25152a.png)

### 什么是 Docker

Docker 就像一个中央食堂，汇集了来自世界各地开发者的预制菜。你想要运行什么程序，就选择相应的预制菜，就像点餐一样简单。

这些预制菜包含了程序运行所需的一切，包括软件库、工具和配置，就像一个完整的运行时环境。Docker就像一个微波炉，只需将预制菜放进去，启动加热，就能轻松运行程序。

无论是开源软件还是其他复杂程序，Docker都能让你一键启动，无需担心繁琐的配置和环境搭建。

### Docker 安装

Docker 有桌面客户端，安装相对而言比较简单，Win 系统需要开启 Hyper-V，下一步到完成。打开客户端没有报错就表示安装成功。

![](https://img.lenband.com/my-img/2024/07/770ef3a2431bade606d2729162ef93ac.png)

![](https://img.lenband.com/my-img/2024/07/a3da9ea60d6c434c26fe78f278b05318.png)

>如果安装过程遇到奇奇怪怪问题，有时需要考虑是否安装的 win 盗版且阉割系统导致。

### Docker 应用

Docker 就像一个巨大的软件仓库，里面存放着各种预制好的软件包，就像微信小程序一样，下载并运行就能使用。

我个人用到 Docker 有三个应用，Memos，Lobehub 和 Planka。

**Lobehub 目前我使用过最好 Ai 集成工具之一**，支持 Vercel 部署。本地如果安装 Ollma，安装一个 Docker 版 Lobe-Chat 是顺其自然的事情。

![](https://img.lenband.com/my-img/2024/07/850f85de87af7f6b0af4b374fd4df732.png)

![](https://img.lenband.com/my-img/2024/07/11a50c73ad906a6a4065d5339bdd30de.png)

**Memos 轻量级笔记服务**，像 Flomo 轻松捕捉和分享你的精彩想法，可以当做离线朋友圈使用。

![](https://img.lenband.com/my-img/2024/07/8b0982bfe42911e66074b5f5a0fa7abd.png)

有些比较散碎文字，记录在 Memos，当可以构成一篇文章时，将碎片转到 Obsidian 整合创作。

这款 Trello 开源版的看板工具 [Planka](https://planka.app/) ，旨在满足个人和团队的项目管理需求。它具有与 Trello 类似的功能，包括看板、列表和卡片，但它是自托管的，这意味着你可以完全控制您的数据和隐私。

![](https://img.lenband.com/my-img/2024/07/aa0143411b28a8f20ec7712475c5b838.png)

![](https://img.lenband.com/my-img/2024/07/2be4af10f0b0816a4bde5becb56ac6e3.png)

### Docker 小技巧

我不需要熟练使用 Docker 桌面客户端，通常我只是打开，看看容器是否启动，仅此而已。

大部分操作使用命令，然而在我实际工作中，使用它们不超过五条。

我尝试使用客户端，比如删除，拉取等操作，能用，但不好用，容易出现各种小问题。

我个人琢磨最佳方式：几条常用命令+客户端可视化相结合。

**Docker 拉取并启动项目**

以 lobehub 为例，在开发者 GitHub 项目中找到 Docker 安装链接。

第一条命令，拉取镜像👇

```
Docker pull lobehub/lobe-chat
```

![](https://img.lenband.com/my-img/2024/07/99f37443d3378b9b905906a3084907e0.png)

打开 CMD，复制粘贴链接地址，敲回车。

![](https://img.lenband.com/my-img/2024/07/3635c5fbd35ab8b4b8fa62b0570efe4f.png)

项目安装好之后，需要启动，即 `下载镜像 → 启动容器`。汽车需要启动才会动，如果你不想推它上路的话。

第二条命令，启动容器👇

```
Docker run -d -p 3210:3210 lobehub/lobe-chat
```

Docker 方便之处在于提升 lucky 值 ，对于普通人而言，Docker 已经降低了使用需要各种系统环境及各种配置的难点。

通常两条命令即可完成一个项目拉取，启动。

此时打开 Docker 桌面客户端，看看容器是否正常启动，点击链接就能用啦🎉

![](https://img.lenband.com/my-img/2024/07/92df69b2ef9016bcf2b701b986be6f6d.png)

离线使用 Memos 记录闪念，用 LobeHut + Ollama 大模型进行文本生成和翻译，用 Planka 整理计划。

通过将本地端口映射到公网，并使用内网穿透技术，你可以从任何地方（家里、手机、其他电脑）访问你的 Docker 项目。

如果你想从办公室以外的地方访问你的 Docker 项目，你需要使用内网穿透，并且你的办公室电脑必须始终开机。

我习惯在本地使用 Docker，如果需要外网访问，则会使用 Vercel 或其他免费云端部署方案。

**Docker 项目更新和卸载**

Docker 核心价值在于免费，离线，安全。但它也有一个很大的劣势，项目更新，数据迁移等问题。

比如项目上游有更新，Docker 如何同步？当你需要换电脑时，本机存在项目数据该如何迁移到另外一台电脑？如何干净清爽卸载项目？

当项目上游有更新，通常会在项目应用内提示。先把容器停止移除，然后在镜像上拉取上游更新到本地，重新部署，启动容器。

停止移除容器，我们可以在 Docker 客户端操作，也可以使用命令，使用命令你需要知道容器名称。

使用客户端停止删除容器，简单直观，看图标就晓得了。

![](https://img.lenband.com/my-img/2024/07/d8d5e26357e42196029026ff9f8e6d23.png)

使用命令行停止删除容器，先看看有哪些容器，确定下容器名称，再停止删除。

```
Docker ps -a
```

![](https://img.lenband.com/my-img/2024/07/dd383b1ddac053c73d7201c7f5f30fcb.png)

停止并删除容器命令，以 memos 为例。

```
Docker stop memos & Docker rm memos
```

客户端和命令操作都可以，两者取其一。

同样更新项目镜像方式可以使用桌面客户端按钮或者使用命令。

如使用命令就是上文中的第一条拉取命令。

如使用客户端更新，点击该镜像文件的 Pull。

![](https://img.lenband.com/my-img/2024/07/d21201e7539fce8cba8f24bee7fc7ab0.png)

当下载新版本之后，旧版本镜像可以删除（Docker 镜像 pull 后生成新镜像而不是覆盖原有镜像）

现在我们需要重新启动容器，记住，这个操作不要使用客户端方式，**请使用命令启动容器，比如上文中的第二条启动容器命令**。

如此一来，项目就更新到最新版本与上游同步，通常旧的记录都会在，建议更新前备份数据。比如 memos 有笔记导出功能。

![](https://img.lenband.com/my-img/2024/07/f6b10de60ea9f3c123c9ffa4224c6444.png)

**让项目容器随 Docker 启动而启动**

一切顺利的话，想必你已经愉快玩耍起来了。

当你下班关机，第二天开机之后发现，有些程序无法运行。那是因为容器没有随着 Docker 启动而启动。

此时手动打开 Docker 客户端，选择容器，点击启动按钮即可。但每次开机都要手动点火，未免太麻烦，希望容器可以随 Docker 一起启动。

两条命令搞定。

首先我们需要判断该容器是否设置为开机自启，如果是为“Always”，如不是为“no”，以 memos 为例👇

```
Docker inspect -f "{{ .HostConfig.RestartPolicy.Name }}" memos
```

![](https://img.lenband.com/my-img/2024/07/b15ccd2513e4e950be01ef7dbc0f1b7c.png)

如果是 no，就执行下一条命令，设置随机启动。

```
Docker update --restart always memos
```

然后再运行上一条命令，检查是否设置成功，“Always”即成功设置。

### Docker 命令扩展

随着 Docker 使用的深入，越来越多的命令和操作会让人感到困惑。若不能将这些命令和操作有效地组织起来，就会形成碎片化的知识，导致 Docker 难以掌握和使用。

我个人处理方式，把命令分门别类保存。这不，使用 Docker 搭建的 Planka 不就派上用场了吗。

![](https://img.lenband.com/my-img/2024/07/1253dfada5689ddb86452b3040a5f533.png)

在 Docker 搭建项目，应当是日常使用频率较高的应用。

此外，定期清理不必要的镜像和容器至关重要。镜像是容器的底层基础，而容器则是运行中的实例。过多的未使用镜像和容器会占用大量存储空间，并可能减慢系统速度。

因此，避免安装了很多不常用的项目，造成无端消耗电脑性能。