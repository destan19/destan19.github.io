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
维护了一套私有特征库，由于需要花大量时间分析，一个app至少花10-30分钟，所以需要打赏后获取，
特征库长期更新。

**私有特征库支持的APP列表**   

[点击下载app列表excel文件](http://175.178.71.82:88/docs/support_apps.xlsx)  

{% assign app_images = site.static_files | where: "app_images", true %}
{% for image in app_images %}
 ![{{image.name}}]({{ image.path }})
{% endfor %}


#### 购买方式
  
**一、支付宝打赏39元**   

 ![](assets/img/alipay.png)  

**二、关注OpenWrt微信公众号并按模板发送消息**  
 ![](assets/img/qrcode-openwrt.jpg)  

模板格式   

支付宝姓名的最后一个字，特征库购买，打赏的金额  

例子  
比如张*亮打赏了39元，则回复以下消息:
亮，特征库购买，39元

**三、等待回复**  
采用人工审核，一般审核时间在24小时内，通过后会回复特征库下载地址给您！  


#### 注意事项
一、确保路由器已经刷好OpenWrt系统并集成了应用过滤插件(OpenAppFilter)  
二、 购买前请确定应用过滤插件可以生效，可以先测试常用网址是否能过滤，如果不能过滤请检查环境，需要做主路由并且关闭加速、广告过滤等冲突模块，加速模块在网络菜单中可以关闭，fullcone nat在防火墙中关闭。  
三、私有特征库中90%以上app都可以过滤，但不可避免存在误判或者失效的情况，出现不能过滤时可以把同一家公司的类似app都开启过滤，比如微信、视频号、微信直播等，保证抖音、斗鱼、王者荣耀、和平精英、爱奇艺、腾讯视频、西瓜视频、哔哩哔哩、淘宝、京东、我的时间、微信小游戏、快手、芒果TV等常用app是可以过滤的。  



