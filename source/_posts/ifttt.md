---
title: 'if (this) /*then*/ {that};'
tags:
  - IFTTT
  - 自动化
id: 849
categories:
  - 互联网
date: 2014-01-24 12:24:04
---

_// 看到标题下意识点进来的读者请注意，**这篇文章不是教 C++ 的**……_

&nbsp;

我已经记不清这是第几次向周围人推荐 IFTTT 了。可以这么说，熟练使用 IFTTT 之后，就会发现什么使用手机应用控制的台灯、家里被盗自动发短信的报警器都是浮云。IFTTT 唯一的功能就是把用户周围一切的一切联系起来，完全可被认为是现代“物联网”的雏形——当然，经过三四年的发展，它已经不只是“雏形”了。

IFTTT 使用非常容易，这里容许我擅自以最简单的“极端天气提醒”为目的做个教程吧：

1\. 首先需要在 [ifttt.com](https://ifttt.com/) 注册一个账户，然后前往对应电子邮箱按说明激活，并返回网站登录刚刚注册的账户。（无图）

2\. 成功登录会进入叫做 dashboard 的页面，这里是个人主页，包含已共享任务、私有任务、IFTTT 社区和邀请好友四个部分。点击 "Create a Recipe" 就可以新建一个任务：

[![教程图片](/uploads/2014/01/IFTTT-create.jpg)](/uploads/2014/01/IFTTT-create.jpg)

&nbsp;

3\. IFTTT 的任务有两个重要组成部分：条件、动作。IFTTT 会周期性检查“条件”，当“条件”中指定的触发器生效时，IFTTT 会在云端自动执行“动作”中指定的内容。点击 "this" 并下拉到 "weather" 将“天气变化”触发器加入“条件”：

[![教程图片](/uploads/2014/01/IFTTT-weather.jpg)](/uploads/2014/01/IFTTT-weather.jpg)

&nbsp;

4\. 首次“天气”需要激活，因为 IFTTT 并不能通过一个电子邮箱推断出用户住址。点击 "activate" 并在弹出窗口中输入城市拼音，"search" 到具体结果，选中并 "activate" 激活城市天气。（无图）

&nbsp;

5\. “天气变化”是一个很概括的词组，IFTTT 需要一个具体的“触发器”，比如选择“天气情况发生变化”：

[![教程图片](/uploads/2014/01/IFTTT-trigger.jpg)](/uploads/2014/01/IFTTT-trigger.jpg)

&nbsp;

6\. “天气情况发生变化”似乎还不够详细，默认为“将要下雨”，用户可以也可以指定“下雪”、“阴天”或“晴朗”作为“条件”。随后点击 "Create Trigger" 完成“触发器”设置：

[![教程图片](/uploads/2014/01/IFTTT-rain.jpg)](/uploads/2014/01/IFTTT-rain.jpg)

&nbsp;

7\. 接下来要设置的是“动作”，点击 "that" 并选中 "Email" 将“发邮件”作为“将要下雨”时执行的内容。“发邮件”分类里只有“给我发送邮件”的选项，点击 "Send me an email"，设置好主题、内容后 "create action" 就会看到最后确认页面，上面很清楚地叙述了这个任务的目的：如果当前天气状况将改变为“下雨”，向 xxx@xxx.xxx 发送邮件。

[![教程图片](/uploads/2014/01/IFTTT-finish.jpg)](/uploads/2014/01/IFTTT-finish.jpg)

&nbsp;

8\. 至此，点击 "Create Recipe" 就可以在以后当地将要下雨时得到邮件通知。IFTTT 的天气检测时间为未来 24 小时，完全不存在雨点砸下来时才收到邮件的尴尬……

&nbsp;

哎，一个天气任务竟然折腾了 500 字……其实恶劣天气推送只是 IFTTT 最基本的功能，像动漫等更 (RSS)、出门关灯 (iOS Location) 都可以通过 IFTTT 设置好相应任务，也不复杂。再高级的使用方法就要灵活结合各种服务和添加标签、通配符，比如有些网站允许用户发送邮件命令，通过 IFTTT 建立任务并将“动作”设置为“发送 Gmail 给 xxx@xxx.xxx”就可以形成一环扣一环的连锁反应，从而大大减轻用户的压力。

IFTTT 目前仍在测试，且拥有很大发展空间，随着与诸如 App.net / GitHub 等知名产品的整合，相信未来的 IFTTT 真的能够实现它宣传语中所说——“让互联网为我们服务”。

&nbsp;

PS: “轻松下”要不要增加个“通过邮件建立离线下载”的功能，这样结合 IFTTT 对 Gmail 和 Dropbox 的控制，就是完全无人值守“离线”下载了。