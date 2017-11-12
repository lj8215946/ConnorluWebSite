---
title: "Adaconda Proxy Settings"
date: 2017-11-12T19:56:15+08:00
author: "Connor Lu"
---
# Adaconda 代理设置

## 创建配置文件

you need to create a .condarc file in you Windows user area:

C:\Users\<username>\
The file should contain:

## 配置文件内容

{{< highlight python "linenos=table,linenostart=1" >}}
# channels:
- defaults

# Show channel URLs when displaying what is going to be downloaded and
# in 'conda list'. The default is False.
show_channel_urls: True
allow_other_channels: True

proxy_servers:
    http: http://proxy.yourorg.org:port
    https: http://proxy.yourorg.org:port

ssl_verify: False
{{< / highlight >}}