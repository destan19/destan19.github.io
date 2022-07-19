---
layout: page
title: 特征库
permalink: /feature/
---

可以直接在应用过滤插件页面升级特征库，升级后可实现列表中的app过滤。  
The feature library can be upgraded directly on the OpenAppFilter plugin page,
and the app filtering in the list can be realized after the upgrade.  

### 特征库列表(feature files)： 

{% assign feature_files = site.static_files | where: "open_feature", true %}
{% for feature in feature_files %}
 [{{feature.name}}]({{ feature.path }})
{% endfor %}


### 私有特征库购买   
维护了一套私有特征库，由于需要花大量时间分析，需要付费获取，一个app至少花10-30分钟。

#### 支持的APP列表：  

[点击下载app列表excel文件](http://175.178.71.82:88/fros/support_apps.xlsx)  

![](http://175.178.71.82:88/fros/feature1.png)  
![](http://175.178.71.82:88/fros/feature2.png)  


#### 购买方式
微信: linux4096 (备注：特征库购买)  
价格：    
39元 (长期更新)  

#### 注意事项
1. 购买前请确定应用过滤插件可以生效，可以先测试常用网址是否能过滤，如果不能过滤请检查环境，需要做主路由并且关闭加速、广告过滤等冲突模块。
2. 私有特征库中90%以上app都可以过滤，但不可避免存在误判或者失效的情况，出现不能过滤时可以把同一家公司的类似app都开启过滤，比如微信、视频号、微信直播等。



