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

[点击下载app列表excel文件](http://175.178.71.82:88/docs/support_apps.xlsx)  

{% assign app_images = site.static_files | where: "app_images", true %}
{% for image in app_images %}
 ![{{image.name}}]({{ image.path }})
{% endfor %}


#### 购买方式
  
1. 支付宝打赏39元   

 ![](assets/img/alipay.png)  

2. 关注OpenWrt微信公众号并按模板发送消息  

##### 模板格式如下  

支付宝姓名的最后一个字，特征库购买，打赏的金额  

##### 例子  
比如张*亮打赏了39元，则回复以下消息:

亮，特征库购买，39元

3. 等待回复  
采用人工审核，一般审核时间在24小时内，通过后会回复特征库下载地址给您！  


#### 注意事项
1. 购买前请确定应用过滤插件可以生效，可以先测试常用网址是否能过滤，如果不能过滤请检查环境，需要做主路由并且关闭加速、广告过滤等冲突模块。
2. 私有特征库中90%以上app都可以过滤，但不可避免存在误判或者失效的情况，出现不能过滤时可以把同一家公司的类似app都开启过滤，比如微信、视频号、微信直播等。



