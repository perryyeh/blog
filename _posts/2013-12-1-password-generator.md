---
layout: post
title: 密码生成器passid.org
date: 2013-12-1 15:10:09 +0800
categories: 手
tags: 密码,密码生成器,在线密码生成器,passid.org,password-generator
---

一晃2个多月没写blog了，皆因我家叶子小盆友出生忙的人仰马翻，今天把之前挖的坑填上，带来个新鲜小工具第一版，[密码生成器](http://www.passid.org)，网址是[www.passid.org](http://www.passid.org)。

初衷：常用网站已有50+，管理密码越来越力不从心，之前我的密码策略见这篇[怎么尽可能避免泄漏网上隐私](http://blog.yeeh.org/post/2012/11/23/hide-secret.html)，给网站分组不同组使用不同级别的密码，然后还准备了个密码本记录了级别，直接的后果就是虽然密码减低为约10组，还是记不住，加上每隔半年需要换，这个过程非常痛苦，不要和我说有1password这样的工具，那个老贵了=_=。那么有没有根据用户名和网站就生成不同密码的呢？ 找了一圈没发现，于是有了是[www.passid.org](http://www.passid.org)。

填写用户名，选择在哪个网站使用，就生成好了密码。 对于要求高的用户，还可以自定义salt，选择密码级别，每个网站的密码都不一样，有效防止csdn这样的脱裤，呃是拖库。

faq：

1、架设在github，所有密码在浏览器生成，不提交任何数据到后端，欢迎右键

2、完全开源，代码托管在[github](https://github.com/passid/www.passid.org)，欢迎fork

3、算法采用公开算法的sha512和增加了字符的base64，生成方法为base64(sha512(用户名+网站域名+salt))，有效防止cmd5等网站的现有库^_^

4、base64增加的字符为-@#~,.[]()!%^*$&

ps：不支持低于ie9下的浏览器，如果侥幸浏览正常，实属意外。实际上我只测试过mac上的chrome，因为只忙了几小时...

ps2：第一版代码也比较丑...



