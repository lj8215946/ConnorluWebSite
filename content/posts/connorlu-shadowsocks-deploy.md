---
title: "Shadowsocks部署"
date: 2017-11-05T09:56:15+08:00
---
# Shadowsocks部署步骤

## 安装

{{< highlight shell >}}
yum install python-setuptools && easy_install pip
pip install git+https://github.com/shadowsocks/shadowsocks.git@master
{{< / highlight >}}

## 启动服务器

{{< highlight shell >}}
sudo ssserver -p 443 -k lj19881010 -m aes-256-cfb --user nobody -d start
{{< / highlight >}}

## 关闭服务器

{{< highlight shell >}}
sudo ssserver -d stop
{{< / highlight >}}
