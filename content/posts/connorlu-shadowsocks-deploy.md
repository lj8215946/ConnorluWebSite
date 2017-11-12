---
title: "Shadowsocks部署"
date: 2017-11-05T09:56:15+08:00
author: "Connor Lu"
---
# Shadowsocks部署步骤

## 安装

{{< highlight shell "linenos=table,linenostart=1" >}}
yum install python-setuptools && easy_install pip
pip install git+https://github.com/shadowsocks/shadowsocks.git@master
{{< / highlight >}}

## 启动服务器

{{< highlight shell "linenos=table,linenostart=1" >}}
sudo ssserver -p {端口号} -k {密码} -m aes-256-cfb --user nobody -d start
{{< / highlight >}}

## 关闭服务器

{{< highlight shell "linenos=table,linenostart=1" >}}
sudo ssserver -d stop
{{< / highlight >}}
