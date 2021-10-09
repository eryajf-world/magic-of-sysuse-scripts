很开心今天来分享运维外挂的2.0版本。

有了前边[1.0](https://github.com/eryajf/shellabout/blob/master/yunweiwaigua.sh "1.0")的基础，今天所见的2.0版本基本上就是水到渠成了。

最大的变化，就是从原来的单层选择菜单，丰富到了两层，以实现更丰富的功能需求。

## 1，架构图。

最新版本脚本架构如下所示：

![运维外挂2.0版本架构草图](https://raw.githubusercontent.com/eryajf/t/master/img20190517103350.jpg "运维外挂2.0版本架构草图")

`我这里提供的脚本以及内容都是提供出来一个思路，各位可以根据自己的实际需求，对脚本进行更改定制，从而符合自己的生产情况。`

## 2，详细说明。

### 内容介绍。

完成之后的内容所包含的功能如下：

- 总入口
 - 1，安装
   - 1，nginx-1.14.0
   - 2，jdk-1.8
   - 3，tomcat-8
   - 4，mysql-5.6
   - 5，node-10.6
   - 6，maven-3.3
   - 7，php-7.0
   - 8，zabbix-agent-3.4
   - 9，py-3.6
   - 10，redis-4.0.6
   - 11，trash-autotrash
   - 12，jdk-1.7
   - 13，暂时未定义
 - 2，初始化
   - 1，初始化模板克隆的虚拟机
   - 2，初始化全新的centos
   - 3，zabbix-agent-3.4
   - 4，安装配置vmtools
   - 5，更改主机IP。
   - 6，更改主机名。
   - 7，新购阿里云服务器初始化。
 - 3，优化
   - 1，暂未定义
   - 2，暂未定义
   - 3，暂未定义
 - 4，其他
   - 1，暂未定义
   - 2，暂未定义
   - 3，暂未定义

### 使用说明

首先将外挂脚本放置在nginx配置的目录下，然后根据文中对应的包，将对应的包放置到对应的位置，详细部署方案，[参考这里。](http://www.eryajf.net/1395.html "参考这里。")

> 只要是网络可达外挂服务的服务器，都可以通过`curl 192.168.10.10/a | sh`进行调用。
>
> 所有请求进来首先通过总入口进入，然后分出四个菜单供选择，接着在对应菜单中选择对应方法即可执行，若选择`<Cancel>`则再返回到总入口当中。

![](https://raw.githubusercontent.com/eryajf/t/master/img/GIF.gif)


## 3，对比1.0。

v2.0主脚本可[`点我`](https://github.com/eryajf/magic-of-sysuse-scripts/blob/master/a)跳转查看。

更新日志：

食用方法不变，主要是更新了内容并优化了相关脚本内容

### 更新内容如下
- 1，新增二级菜单选项，从而让功能更加清晰可控。
- 2，新增阿里云服务器初始化选项，新建一台阿里云服务器之后，一键执行，即可投入使用。
- 3，优化安装菜单中的各个安装方法。
- 4，更改原whiptail使用if判断为case判断，使阅读更加简洁。
- 5，增加输出颜色控制，使输出更加显眼。

## 星路历程

[![Stargazers over time](https://starchart.cc/eryajf/magic-of-sysuse-scripts.svg)](https://starchart.cc/eryajf/magic-of-sysuse-scripts)
