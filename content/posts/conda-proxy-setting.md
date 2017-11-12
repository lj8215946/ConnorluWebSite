---
title: "各种代理设置"
date: 2017-11-12T19:56:15+08:00
author: "Connor Lu"
---
# 各种代理设置

## Adaconda 代理设置

### 创建配置文件

you need to create a .condarc file in you Windows user area:

C:\Users\<username>\
The file should contain:

### 配置文件内容

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

## CMD 和 Git 中的代理设置

### CMD 设置代理

在 cmd 环境下设置代理可能不是很常用，但是某些情况下还是可能会用到，比如公司的电脑只能通过设置代理访问外网，而你需要在 cmd 环境下使用 gem 命令更新文件时。

当然，如果你使用某些代理软件为所有通讯设置了代理，那就不需要这些设置了。

为 cmd 设置代理很简单，首先打开 cmd （win + R，输入 cmd，然后按 enter 键），然后输入如下命令：

set http_proxy=http://proxy.yourname.com:8080
其中 http://proxy.yourname.com 是你的代理服务器地址，而 8080 是端口号，如果有则设置。另外，如果你的代理服务器要求用户名和密码的话，那么还需要：

set http_proxy_user=
set http_proxy_pass=
设置完成后，就可以在 cmd 下正常使用网络了。

### Git 设置代理

Git 的代理设置也非常简单，一句话就搞定了：

git config --global http.proxy http://127.0.0.1:1080
如果需要用户名密码的话，则设置：

git config --global http.proxy http://user:password@http://10.10.10.10:8080 
其中 user 和 password 分别为你的用户名和密码。

设置完成后，可以通过如下命令来查看设置是否生效：

git config --get --global http.proxy
如果某一天你不喜欢她了，需要删除代理设置，那么可以使用：

git config --system (或 --global 或 --local) --unset http.proxy
来删除设置。