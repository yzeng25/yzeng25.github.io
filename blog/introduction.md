---
slug: introduction
title: 第一篇博客
authors: [yilin]
---

## 我是谁

我是曾奕霖，GitHub ID：[yzeng25](https://github.com/yzeng25)，是一个拥有三年多工作经验的文档工程师，曾就职于华为、Rancher Labs（2020 年底被 SUSE 收购）和 API7.ai。

2018.11~2020.01，我负责华为云中间件 ROMA（后更名为 [Roma Connect](https://support.huaweicloud.com/roma/index.html)） 的用户文档写作，截止至目前，该项目的文档仍有 70% 的内容是我当时留下的。说人话就是：文章是我写的，图片也是我画的。

2020.02~2021.07，[Rancher 2.x 中文文档](https://github.com/cnrancher/docs-rancher2/graphs/contributors)的维护者。我作为 Rancher/SUSE 大中华区唯一一个文档工程师，我翻译和编辑了 Rancher 2.x 中文文档、翻译了 Rancher 2.5.3 和 Rancher 2.5.8 的 UI、对 Rancher 2.x 中文文档网站进行了 SEO 改造并使月均浏览量从 30000+次 上涨至 96000+次。除此之外，我还引入了一些便捷的工具以减轻工作量和简化工作流程，如断链扫描、百度统计等。我在这个代码库的贡献者中排名第一，commits 数量是第二名的 3 倍，修改的行数是第二名的 17 倍。如无意外，近一年内霸榜的应该还是我。

2021.07~2022.04，API7.ai 文档工程师，Apache APISIX 首个以文档工程师身份成为 Apache Committer 的人，纵观国内的 Apache 项目，以文档工程师身份成为 Apache Committer 的人只有四个，前两个在 Apache Pulsar，第三个是我，第四个是我在 API7.ai 的前同事，她的 git 命令都是我教的。
参与 Apache APISIX 博客网页设计，编辑、翻译博客文章，拓展 Apache APISIX 并成功与多个国内外知名社区展开联动。

2022.04~present，公司 B 轮融资玩砸了，喜提离职补偿，目前属于灵活就业。

自带行业冥灯 debuff。

从华为离职后，华为云中间件深圳资料团队大换血，最终被划到了一个很边缘的部门。

从 SUSE 离职后，半年多找不到人顶我的位置，恰好碰到大版本和新产品上线，现在属于是债多不愁了。

从 API7.ai 离职后，公司 B 轮没融到，不知道还能撑几年 hhh。

## 为什么要用 Docusaurus 做这个网站

因为从 2020.02 到 2022.04，我一直在使用 Docusaurus。一方面是恰好两个公司都选择了这个框架，另一方面是这个框架简单易用，且拥有一个非常友好活跃的开源社区，提问题提 issues 都能在短时间内获得解答。

1. 用魔法打败魔法，用 Docusaurus 写 我的 Docusaurus 踩坑指南，我觉得是一件很酷的事情。

1. 技术大佬们都有自己的博客，我在全职打工的时候就想建一个自己的博客，但是在已有的博客平台上面写东西太逊了，既然 Docusaurus 这么好用，可以先拿它试试看，最坏的结果不就是删库嘛。

1. 我在全职打工时候基本上就是碰到问题就去看文档、看 Google、看 Stack Overflow 帖子，面向问题开发文档。首先是只局限在了码字上面，其次是没有完整地、系统地了解过 Docusaurus 的框架和结构，这容易把路走窄了。所以这波我想试试水，把 Docusaurus 学明白，然后也把 Vercle 之类的部署和发布工具学明白。

1. 坦白讲 Docusaurus 的中文文档比英文文档要差，既然我踩过坑，我就希望其他同行在碰到问题的时候能找到中文的文档来解决类似的问题，看英文文档确实会令人头大，特别是任务紧急的时候。我也有计划去参与 Docusaurus 的中文文档翻译，不过这至少是今年下半年的事情了。

1. 提交 commits、合并 PR、发布博客可以改善我的 GitHub 活跃度。

## 未来打算更新的内容

1. Docusaurus 踩坑指南。

    1. 当时简单记录在 Rancher wiki 里面的一些问题和解决这些问题的思路。

        1. [Algolia DocSearch 搜索框失效的排查及修复过程](https://github.com/cnrancher/docs-rancher2/wiki/Algolia-DocSearch-%E6%90%9C%E7%B4%A2%E6%A1%86%E5%A4%B1%E6%95%88%E7%9A%84%E6%8E%92%E6%9F%A5%E5%8F%8A%E4%BF%AE%E5%A4%8D%E8%BF%87%E7%A8%8B)

        1. [Algolia搜索框注意事项](Algolia搜索框注意事项)

        1. [master分支和preview分支构建失败详解](https://github.com/cnrancher/docs-rancher2/wiki/master%E5%88%86%E6%94%AF%E5%92%8Cpreview%E5%88%86%E6%94%AF%E6%9E%84%E5%BB%BA%E5%A4%B1%E8%B4%A5%E8%AF%A6%E8%A7%A3)

    1. 参与 Apache APISIX 中英文博客编辑时碰到的问题和解决思路：[Docusarus 的 i18n 工作机制和原理](https://github.com/facebook/docusaurus/issues/7041)。

1. 我的常用工具和选型思路：

    1. 为什么要用付费工具 [Dr.LinkCheck](www.drlinkcheck.com) 为开源网站进行服务？

    1. 为什么要从 Google Analytics 转到 百度统计？

1. 罗马不是一天建成的，开源文档也不是 -- 记录开源文档的养成阶段

    1. 从无到有。
    2. 从有到优。
    3. 聆听社区，积极回应。
    4. 让更多人看到你的文档。
    5. 学会取舍，聚焦用户在乎的文档。

1. 拓展 Apache APISIX 生态时碰到的故事和事故：

    1. 大无语事件，生态合作聊到一半，创始人离职了怎么办？-- 记录 Dapr 合作
    2. 都什么年代了，怎么还有人在用 AsciiDoc 建站？-- 记录 Keycloak 合作
    3. 你行你上，且看文档工程师怎么化腐朽为神奇 -- 记录 ClickHouse 合作
    4. 皆大欢喜，APISIX 登上 OPA 生态的过程 -- 记录 OPA 合作

1. 在 A+ 轮创业公司碰到的无语事件。

    1. 如何整治双标老板

    1. 如何带领无技术背景的文档同事入门和精通命令行

    1. 不要过度依赖线上预览环境，也许明天预算被砍了，环境就无了

    1. 出尔反尔之说好的远程办公不算数了？

    1. 假公济私之施加压力企图利用公司流程推动社区 PR 合并 but failed

1. 我报名参加 TCWorld 的议题，综合考虑到上海疫情可能会延期、我的议题不一定会被选上等因素，先做个 trailer 版本看看。

1. 从零开始建站过程中碰到的问题和解决方法。

1. 简单聊一聊开源项目文档工程师应该具备的基础和进阶技能吧：文字、翻译、测试思维、思考方式等。

1. 买一个域名。

1. 把简历也放上来。




