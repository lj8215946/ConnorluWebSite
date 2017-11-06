---
title: "Hugo服务更新"
date: 2017-11-05T09:56:15+08:00
author: "Connor Lu"
---
# Hugo服务更新方法

## 进入网页目录

{{< highlight shell "linenostart=199" >}}
cd /root/go/src/github.com/gohugoio/hugo/connorlu
{{< / highlight >}}

## 更新代码

{{< highlight shell "linenostart=199" >}}
git pull origin master
{{< / highlight >}}

## 开启hugo

{{< highlight shell "linenostart=199" >}}
screen hugo server --watch --renderToDisk --bind="0.0.0.0" --port=80 --baseUrl="connorlu.vip"
{{< / highlight >}}
