---
title: Obsidian 图片管理方式
date: 2024-10-15T04:09:00.919Z
---


### Obsidian 图片管理方式

![](https://img-1259210397.cos.ap-guangzhou.myqcloud.com/Frame%201.png)

**1. 图像右键菜单插件：Image Context Menus**
* 支持复制图片
* 默认应用打开图片
* 打开图片所在文件夹
* 定位图片位置
![](https://img-1259210397.cos.ap-guangzhou.myqcloud.com/Pasted%20image%2020240508142633.png)

**2. 自动上传图床插件：Image auto upload Plugin**
- 联动 PicList / Picgo 图床工具
- 一键将正文中所有本地图片上传图床
- 右键本地图片链接可单张上传
- 上传本地图片后自动转换图片外链
- 上传图片之后自动移除本地图片

![](https://img-1259210397.cos.ap-guangzhou.myqcloud.com/20240508_142239.gif)

**3. 冗余图片清理：Clear Images Settings**

该插件从所有 Markdown 文档中获取所有图像链接，并将这些图像与附件库中图像文件进行比较。如果检索的图像文件中的任何一个未在仓库的任何文档中引用，它们将被自动删除。简而言之，它的作用就是清理未必应用的本地图片。

![](https://img-1259210397.cos.ap-guangzhou.myqcloud.com/Pasted%20image%2020240508151505.png)

**具体选择**

三款插件搭配使用效果最佳。

「Image auto upload Plugin」当正文图片需发布微信公众号，博客等平台时，优先使用将图片上传图床模式，转为外链后，可避免微信公众号后台复制正文时丢失图片。

「Image Context Menus」用于快速插入本地图片之后的扩展使用，比如将图片复制到其他笔记，发布各种社交平台，只需右击图片复制即可。

「Clear Images Settings」定期清理附件库中未被引用的图片，释放本地存储空间。

三款插件合理搭配使用，可以减少图床冗余，降低存储空间压力，将重要图片上传到图床，其他图片保存在本地，清理未被引用的图片。

当然，具体选择取决于个人偏好和使用场景。

以上是我个人使用 Obsidian 图片管理方式。
