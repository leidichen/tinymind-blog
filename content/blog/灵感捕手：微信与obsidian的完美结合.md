---
title: 灵感捕手：微信与Obsidian的完美结合
date: 2024-10-15T04:18:23.414Z
---

我试过不少记闪念工具，想着能在零碎时间，赶紧把脑子里蹦出来的点子记下来。可要是这些点子没接着往下琢磨，它们就跟烟花似的，一闪就没了影。

我老琢磨，怎样才能把那些速记的灵感笔记变成实实在在的东西。

![](https://img.lenband.com/my-img/2024/09/f0a25b5eb07e5bfe065a73de1f61a797.png)

### 各式各样的闪念笔记工具

最开始我用手机上的备忘录，拿起手机就能记，方便得很。但问题是，这玩意儿没法同步到电脑上修改，换不同牌子手机，备忘录格式还对不上。

后来用 Flomo，感觉挺顺手，记东西快得很。可等我攒了几百条笔记后，发现整理起来更头疼，总不能在 Flomo 里写文章吧，得把这些笔记搬到我的主力编辑器里继续加工。

这一通操作，不够顺手，尤其 Flomo 导出只有 HTML 格式，真是让人摇头。

![](https://img.lenband.com/my-img/2024/09/05a6be7f1ced91834258bc880c451047.png)

还试过用 Docker 部署的 memos，界面功能跟 Flomo 差不多，它能导出 Markdown 格式，本地数据管理，看着也挺安全，但它没法联网。要是想手机同步数据，还得折腾内网穿透什么的。

滴答清单不错，平时记个待办清单，习惯追踪，其实它也能记笔记，但容易跟待办事项混在一起，脑子切换不过来究竟记录待办还是笔记，试了几次之后，不灵。

Notion 当然也能快速记笔记，手机端适配不少桌面小组件，点个图标就能弹出记录窗口或对应笔记页面。但大家都知道，Notion 打开一条笔记有时候得转好几秒，等加载完，要记啥灵感，也忘得差不多了。

今年我一直在用 Fleeting notes，这工具全平台支持，包括浏览器扩展，能快速捕捉想法并同步到 Obsidian。免费版只支持一个设备同步 OB，就是说，如果选了手机端同步笔记，浏览器扩展就没法同步了。

![](https://img.lenband.com/my-img/2024/09/436247b6a55b05f8d83850b959675cea.png)

不过我的需求也简单，只要能把手机上的碎片笔记同步就行。周末在家不开电脑时，用手机上的 Fleeting notes 写写日记或者记点啥，打开电脑上的 Obsidian 时，笔记已经同步过来了，手机端的笔记会自动删除（可以设置）。

这功能我觉得挺好，手机端 APP 永远干净清爽，不会因为笔记多而焦虑。同时也能提醒哪些笔记还没同步。除了偶尔同步需要手动触发一下，免费的还要啥自行车。

总之，所有快速笔记类工具归根结底需要两个功能，支持多端同步和笔记对接能力。

### 笔记对接能力

我用 Obsidian 作为主力笔记工具。记录可以用各种 APP，但最后一定汇总到 Obsidian 中进行创作。因为我习惯，无论用什么软件记录的文字，包括语音笔记，图片，网址链接，最后都在 OB 中进行分流归档。

比如效率工具网址，经过使用测试之后，就归纳到冷板凳周刊；灵感笔记如果能够扩展成为一篇博客就归拢到文章中去；日记记录流水及一些使用工具时的技巧方法备份等等。

鉴于 Obsidian 手机端很难用，因此各个 APP 工具记录的笔记要和 Obsidian 对接同步，是一个关键问题。

Fleeting notes 挺好，但免费版多一台就要收费，而且毕竟是国外服务，网络会有延迟。只能说勉强凑合使用。

其实我的需求很简单，就是把手机记录的文字同步到电脑端的 Obsidian 中。为此我也使用过各种第三方同步软件，比如微力同步，Resilio Sync 等，但手机端 Obsidian 难用，再去折腾这些同步工具也无济于事。

今天在推上看到一条「微信给 Obsidian 发消息」，我感到一种更加快捷的方式，悄然出现在我面前。

![](https://img.lenband.com/my-img/2024/09/2818a56e034c77593652fee1f88f8fac.png)

### OB 消息助手

上述提到的所有快速记录工具都需要额外安装一个 APP，如果同样功能使用日常频率最高的微信就能做到，岂不省事。

况且不止少装一个 APP 那么简单，因为熟悉的输入环境和操作界面，会大大降低记录文字的成本。

OB 消息助手，文字图片都行，同步速度尚可。

![](https://img.lenband.com/my-img/2024/09/7779d199ce59653b5a068aad555502ae.png)

当然，这种通过微信接口的服务不收费是不可能的，免费一天10条。

无限量会员版一年39元，我觉得很良心。一杯咖啡钱，打通一年用微信将闪念笔记同步到 Obsidian。

下载安装插件，绑定微信，把令牌 ApiKey 填入 Obsidian 插件设置中即可实现，从微信发送笔记，Obsidian 接收笔记。

![](https://img.lenband.com/my-img/2024/09/c4b938f8d97e2f345940fdeb7c104434.png)

插件目前处于开发优化阶段，不必着急开通会员。可以先每天使用十条试试，等稳定之后再考虑付费。

**官方网站👇**

🔗 https://wechatobsidian.com/