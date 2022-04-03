---
title: 用爱发电的小服务
date: 2022-01-26 21:07:33
top_img: /img/1261652.webp
aside: false
comments: false
---

## 公告
**接口路由**： https://api.hengy1.top
所有的接口都在这个下面了～

{% note red 'fas fa-bullhorn' flat %}

因为现在主要是Golang后端，在冲大厂ing
前端的话我准备大二暑假陆陆续续写出来～
所以大家想调用服务器直接怼接口就好了。
因为是用爱发电的，尽量别攻击，没啥意思。

{% endnote %}

##  谈谈安全
1. 接口走的Cloudfare，~~你随便Ping下就能发现~~
2. 你打DDOS,CC的话基本过不来，~~别浪费钱~~
3. 接口下面是有Waf的，~~别注入啦～~~ 
4. 如果你真能打进来～ 联系我QAQ
5. 相互多多交流吧，共勉

##  服务一：宿舍水费预警/充值系统
1. 每天的总请求量为1000
2. 每个IP总请求为50
3. 查询后余额结果缓存时效为10分钟
4. 查询后消费记录缓存时效为6分钟
5. 邮件激活后开始工作
6. 邮件取消/申请为同一接口
7. 激活邮件发送间隔存在一定限制
8. 充值金额不超过30元，仅为紧急充值
9. 充值服务每20秒提供一次有效服务

点击查看文档：{% btn '/service/JnuWater.html',这里啦～,far fa-hand-point-right,green outline %}

##  服务二：学校教务服务
1. 仅需要账号密码
2. 本系统不会保存您的账号密码，若建议勿使用
3. 请务必保管好自己的账号密码，作者不负责
4. 为保护下游服务器防止解析失败，限每5秒调用一次
5. 特此说明：本系统针对教务服务不会存在任何记录账号密码，即用即消
6. 连续多次错误会导致校园网账号锁死
7. 现在加入了错误4次在一小时内不会提供服务

点击查看文档：{% btn '/service/school.html',这里啦～,far fa-hand-point-right,green outline %}

## 敬请期待