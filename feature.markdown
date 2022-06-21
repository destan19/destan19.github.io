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
维护了一套私有特征库，由于需要花大量时间分析，需要付费获取。  
支持的app列表可以访问以下地址查看：  
http://www.ifros.cn/index.php/feature/  

价格： 29元 