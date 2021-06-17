---
layout: page
title: 插件下载
permalink: /download-ipk/
---
### 说明
通过插件安装需要内核版本号相同或者相近，并且内核相关配置要一致  
插件基于lean的源码编译，没有修改任何内核配置。  
在安装之前务必确认版本号是否一致！  
如果内核版本相近，如5.4.105和5.4.95，小版本相差不大，可以强制安装  
详细安装说明在安装包中查看！

如果你是新手，不理解内核模块安装原理，建议不要折腾了，直接找别人发布的带应用过滤的固件，  
或者自己尝试编译固件。  



#### 7621系列
> 支持的设备 RM AC2100, Phicomm K2P, Newifi3, YouHua WR1200JS

{% assign ipks = site.static_files | where: "mt7621", true %}
{% for ipk in ipks %}
 [{{ipk.name}}]({{ ipk.path }})
{% endfor %}


#### X86-64

{% assign ipks = site.static_files | where: "x86-64", true %}
{% for ipk in ipks %}
 [{{ipk.name}}]({{ ipk.path }})

{% endfor %}

#### 斐讯N1盒子

{% assign ipks = site.static_files | where: "n1", true %}
{% for ipk in ipks %}
 [{{ipk.name}}]({{ ipk.path }})

{% endfor %}

#### 友善R2S

{% assign ipks = site.static_files | where: "r2s", true %}
{% for ipk in ipks %}
 [{{ipk.name}}]({{ ipk.path }})

{% endfor %}

#### 7620系列
> 支持的设备 极路由1S、y1、y1s等

{% assign ipks = site.static_files | where: "mt7620", true %}
{% for ipk in ipks %}
 [{{ipk.name}}]({{ ipk.path }})
{% endfor %}
