---
title: "Hugo服务更新"
date: 2017-11-05T09:56:15+08:00
---
# Hugo服务更新方法

## 进入网页目录

{{< highlight shell >}}
cd /root/go/src/github.com/gohugoio/hugo/connorlu
{{< / highlight >}}

## 更新代码

git pull origin master

## 开启hugo

screen hugo server --watch --renderToDisk --bind="0.0.0.0" --port=80 --baseUrl="connorlu.vip"
