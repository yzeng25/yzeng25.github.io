---
slug: drlinkcheck-user-guide
title: Dr.LinkCheck 使用指南
authors: [yilin]
---

## 前情提要

前一篇博客有提到断链扫描工具的选型，最后我选择了 [Dr.LinkCheck](https://www.drlinkcheck.com/)。这篇博客就简单说一说怎么使用这个工具吧。

## 免费扫描

1. 打开浏览器，输入 `https://www.drlinkcheck.com/`，访问 Dr.LinkCheck。

1. 在文本框中输入你要扫描的网址，单击 “Start Check” 开始扫描。

1. 根据返回结果修复链接。

:::tip
Dr.LinkCheck 的免费额度是 **1500** 个链接，如果网站的链接数量大于 1500，建议付费升级或使用其他工具。注意**链接数不等于页面数**，一个页面可以有 0 个链接，也可以有非常多的链接。如果非要粗略估计的话，总链接数 ≈ 总页面数 x 5 是一个比较合理的值。
:::

## 付费扫描

1. 打开浏览器，输入 `https://www.drlinkcheck.com/`，访问 Dr.LinkCheck。

1. 单击页面右上角 “Login”，进入用户登录页面。
    
    ![login](/img/drlinkcheck/login.png)

1. 输入用户名和密码，单击 “Login”，进入用户概览页。
    
    ![login page](/img/drlinkcheck/login-page.png)

1. 单击 “rerun Check” 对已有项目进行扫描，或单击“add a project”添加新的项目并扫描。
    
    ![dashboard](/img/drlinkcheck/dashboard.png)

1. 根据返回结果修复链接。

## 进阶操作

在已经成为付费用户的基础上，这些操作可以提升工作效率，节省碎片化的时间。

### 添加过滤条件

总有那么一些链接是误报的，有两种过滤方式。

第一种，假装看不见，不处理。以后重复出现这种误报的结果可以直接挂在那里，选择性忽略掉它们。

第二种，使用正则表达式，添加过滤条件，重复出现的时候它们会被过滤掉，不出现在最终结果里面。

1. 单击 “Project Settings”，打开项目配置页。

1. 单击 “Advanced Settings”，展开高级配置项。

1. 找到 “Ignore links if...” 这一项，并在文本框中输入你的过滤条件。

    ![settings](/img/drlinkcheck/settings.png)

1. 重新运行扫描，查看扫描结果是否符合预期，如有需要可以进一步修改和完善你的过滤条件。

:::tip
Dr.LinkCheck 的官方文档中有详细讲述如何配置表达式，详情请见 [Dr.LinkCheck Documentation](https://www.drlinkcheck.com/support/docs#crawl-and-ignore-rules)。
:::

举个例子，这是我为 Rancher 中文文档网站配置的过滤条件。

```txt
Url STARTSWITH "https://git.rancher.io" OR Url STARTSWITH "https://keycloak.org/docs" OR Url STARTSWITH "http://xip.io/" OR Url STARTSWITH "https://docs.vmware.com" OR Url STARTSWITH "https://www.splunk.com"
```

可以看到我只用了两个变量 `Url STARTSWITH` 和 `OR`，就把误报的过滤掉了。建议从你想要的效果出发，去文档里面找能够满足这个效果的一个或多个过滤条件。如果反过来，先把文档读完，里面的过滤变量太多，描述太详细，容易把自己的思路弄乱，反而不好。

### 项目隔离

项目隔离是个好东西。从付费的规则讲起，我用的最便宜的付费版，限制是：

1. 每个项目扫描的链接数量不超过 10000 个。

1. 最多同时可以存在 5 个 项目。

在这些规则限制内，我能玩出什么花活？

1. 理论上我可以扫描的链接数量是 5*10000 = 50000 个。在一个项目的链接数超出 10000，或者我想要精确扫描某一个部分的时候，我可以创建新的项目，满足我的需求，而且用完可以立马删除。

1. 帮其他开源项目扫描，提交 pr 修复这些问题。

### 自动化

自动化也是个好东西。Dr.LinkCheck 支持每两周自动执行所有项目，并结果发送至指定邮箱。从初期解决完所有断链之后，我只要每两周抽一个上午出来处理这些问题即可，美滋滋。

1. 单击 “Project Settings”，打开项目配置页。

1. 找到 “Run biweekly > on Monday - at about 08: 00” 这一项，并在调整自动化扫描周期。

1. 找到 “Email results of recurring check to...”，并在文本框中输入邮件地址。

    ![settings](/img/drlinkcheck/settings.png)

1. 查看扫描结果是否符合预期，如有需要可以进一步修改和完善你的定时扫描计划。

## 总结

Dr.LinkCheck 真好用，建议大家试试看，说不定能开发出其他玩法。
