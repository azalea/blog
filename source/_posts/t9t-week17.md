---
title: 免费雇佣全球的开发者为你的开源项目做贡献 - 我的透明创业实验第十七周
description: 试用了 issuehunt.io 来帮助自己的开源项目成长
date: 2019-09-09
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第十七周的实验记录.

## 试试 issuehunt

很久之前就从群友 [EGOIST](https://github.com/egoist) 处听说过 [issuehunt](issuehunt.io) 这个项目. 简单来讲, issuehunt 就是一个 issue 资助平台, 开源项目使用者可以通过 issuehunt 给某个开源项目的 issue 注资. 解决这个 issue 的人就可以获得这笔钱(另一个基于区块链的类似产品 [gitcoin](https://gitcoin.co/)). 可能是 issuehunt 还比较早期的原因, 除了用户的注资之外, 你还可以申请 issuehunt 来注资. 因为 [chart.xkcd](https://github.com/timqian/chart.xkcd) 还算流行, 我也试了试申请.

申请了 4 个 issue, 三个成功被注资 $50, 有一个可能因为没有写描述没有通过. 注资之后第二天就收到了两个质量还可以的 PR, 让我十分惊喜. 之后如果开源项目需要帮助, 通过这个平台的注资可以给贡献者更多激励. 对于我来讲相当于可以免费雇佣全球的开发者来做贡献, 何乐而不为.

关于申请的成功率, 我只试过 [chart.xkcd](https://github.com/timqian/chart.xkcd) 这一个项目, 所以不是很清楚如果 star/用户数不多的项目是否也可以申请到他们的资助. 了解的朋友欢迎在评论区留言告知.

> Pro tip: 如果没人来解决注资后的 issue, 你还可以自己去解决它, 改进自己项目的同时还收获一笔小钱😂

## 其他

为 [tomato-pie](https://github.com/t9tio/tomato-pie) 增加了一些功能, 在产品中植入了自己的 [patron](https://www.patreon.com/timqian), 告诉大家 “我有更新的计划, 如果喜欢这个产品和计划中的更新请成为我的 [patron](https://www.patreon.com/timqian)”. 不过收效比较惨淡, 没有收到任何赞助.

实验已经进行了快 1/3, 目标完成度还不到 2%. 后面做产品需要注意增加付费渠道了.

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

### 平均每月被动收入($)(本周收入 / 7 * 30)
<svg id="incomeChart"></svg>

### 用户量
<svg id="userChart"></svg>

### github star 数
<svg id="starChart"></svg>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week17.md)

<script src="https://cdn.jsdelivr.net/npm/chart.xkcd@1.1.3/dist/chart.xkcd.min.js"></script>


<script>
var usersvg = document.getElementById('userChart');
var starsvg = document.getElementById('starChart');
var incomesvg = document.getElementById('incomeChart');

new chartXkcd.XY(usersvg, {
  xLabel: 'weeks',
  data: {
      datasets: [{
          label: 'wewe',
          data: [{x:3,y:0},{x:4,y:60},{x:5,y:80},{x:6,y:91},{x:7,y:95},{x:8,y:95},{x:9,y:103},{x:10,y:103},{x:11,y:103},{x:12,y:103},{x:13,y:103},{x:14,y:103},{x:15,y:103},{x:16,y:108}]
      },{
          label: 'open source jobs',
          data: [{x:0,y:39},{x:1,y:60},{x:2,y:62},{x:3,y:80},{x:4,y:101},{x:5,y:105},{x:6,y:109},{x:7,y:111},{x:8,y:113},{x:9,y:114},{x:10,y:119},{x:11,y:121},{x:12,y:122},{x:13,y:123},{x:14,y:123},{x:15,y:127},{x:16,y:131}]
      },{
          label: 'tomato-pie',
          data: [{x:0,y:653},{x:1,y:673},{x:2,y:722},{x:3,y:634},{x:4,y:647},{x:5,y:705},{x:6,y:681},{x:7,y:714},{x:8,y:712},{x:9,y:733},{x:10,y:774},{x:11,y:779},{x:12,y:801},{x:13,y:821},{x:14,y:898},{x:15,y:911},{x:16,y:981}]
      },{
          label: 'star-history',
          data: [{x:0,y:21},{x:1,y:21},{x:2,y:28},{x:3,y:33},{x:4,y:33},{x:5,y:34},{x:6,y:39},{x:7,y:38},{x:8,y:40},{x:9,y:47},{x:10,y:48},{x:11,y:50},{x:12,y:61},{x:13,y:58},{x:14,y:55},{x:15,y:57},{x:16,y:58}]
      }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});

new chartXkcd.XY(starsvg, {
  xLabel: 'weeks',
  data: {
    datasets: [{
        label: 'wewe',
        data: [{x:4,y:0},{x:5,y:11},{x:6,y:33},{x:7,y:57},{x:8,y:70},{x:9,y:77},{x:10,y:78},{x:11,y:102},{x:12,y:103},{x:13,y:108},{x:14,y:111},{x:15,y:114},{x:16,y:211}]
    },{
        label: 'open source jobs',
        data: [{x:0,y:731},{x:1,y:764},{x:2,y:763},{x:3,y:821},{x:4,y:872},{x:5,y:891},{x:6,y:898},{x:7,y:903},{x:8,y:934},{x:9,y:940},{x:10,y:956},{x:11,y:962},{x:12,y:966},{x:13,y:967},{x:14,y:976},{x:15,y:980},{x:16,y:994}]
    },{
        label: 'tomato-pie',
        data: [{x:0,y:107},{x:1,y:113},{x:2,y:117},{x:3,y:118},{x:4,y:125},{x:5,y:126},{x:6,y:128},{x:7,y:129},{x:8,y:134},{x:9,y:134},{x:10,y:136},{x:11,y:136},{x:12,y:139},{x:13,y:139},{x:14,y:141},{x:15,y:148},{x:16,y:155}]
    },{
        label: 'star-history',
        data: [{x:0,y:921},{x:1,y:998},{x:2,y:1110},{x:3,y:1129},{x:4,y:1154},{x:5,y:1178},{x:6,y:1190},{x:7,y:1216},{x:8,y:1238},{x:9,y:1246},{x:10,y:1276},{x:11,y:1291},{x:12,y:1299},{x:13,y:1308},{x:14,y:1328},{x:15,y:1343},{x:16,y:1361}]
    }, {
        label: 'chart.xkcd',
        data: [{x:12,y:3},{x:13,y:500},{x:14,y:3069},{x:15,y:3764},{x:16,y:4308}]
    }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});

new chartXkcd.XY(incomesvg, {
  xLabel: 'weeks',
  data: {
    datasets: [{
        label: 'star-history',
        data: [{x:0,y:0.69},{x:1,y:0},{x:2,y:25.7},{x:3,y:12.8},{x:4,y:0},{x:5,y:8.571428571428571},{x:6,y:4.285714285714286},{x:7,y:4.285714285714286},{x:8,y:8.571428571428571},{x:9,y:8.571428571428571},{x:10,y:4.285714285714286},{x:11,y:17.142857142857142},{x:12,y:8.571428571428571},{x:13,y:3/7*30},{x:14,y:1/7*30},{x:15,y:3/7*30},{x:16,y:2/7*30}]
    }, {
        label: 'patron',
        data: [{x:10,y:0},{x:11,y:1},{x:12,y:1},{x:13,y:2},{x:14,y:8},{x:15,y:8},{x:16,y:9}]
    }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  },
});

</script>

