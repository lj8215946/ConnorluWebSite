---
title: "VN 数据测试服务使用说明"
date: 2017-11-08T21:13:15+08:00
author: "Connor Lu"
---
# VN 数据测试服务使用说明

## 代码仓库

<https://github.com/lj8215946/VNTestServer.git>

{{< figure src="/media/github-vntestserver-shortcut.png" title="VN Test Server Github Home Page" link="https://github.com/lj8215946/VNTestServer" >}}

## 代码获取及提交

1. 获取看代码

{{< highlight shell "linenostart=1" >}}
git clone https://github.com/lj8215946/VNTestServer.git
{{< / highlight >}}

{{< figure src="/media/vntestserver-main-folder.png" title="VN Test Server Main Folder" >}}

2. 添加文件

在/VNTestServer/public下面添加任何合法静态问题文件（HTML，CSS，JSON,JavaScript等）
例如：
{{< highlight javascript "linenostart=1" >}}
{
    "errCode": 0,
    "name": "connorlu",
    "datas": [
        {"text":"第一行字符串","index":0},
        {"text":"第二行字符串","index":2},
        {"text":"第三行字符串","index":3}
    ]
}
{{< / highlight >}}

{{< figure src="/media/vntestserver-static-files.png" title="VN Test Server Add Static Files" >}}

3. 提交文件

{{< highlight shell "linenostart=1" >}}
\# 将添加文件纳入版本控制
git add .
\# 在本地提交文件
git commit -a -m "提交的说明"
\# 更新服务器端代码
git pull origin master
\# 推送代码至服务器端
git push origin master
{{< / highlight >}}

4. 提交文件
查看静态文件，由于配置了自动部署功能。我们只需要等待1～5秒刷新网页即可看到修改效果。
服务部署在如下URL：
<http://connorlu.vip:3000/xxxxxx>  //xxxxxx代表具体服务的路径
例如：
<http://connorlu.vip:3000/test.json>
{{< figure src="/media/vntestserver-static-files-preview.png" title="VN Test Server Preview Static Files" >}}

## 其他说明

动态代码需要修改/VNTestServer/index.js
{{< figure src="/media/vntestserver-dymatic-files.png" title="VN Test Server Dynamic Files" >}}
