---
layout: page
title: 特征库
permalink: /feature/
---
### 特征库简介
特征库用于描述app协议特征，通过更新特征库可以修复某些app失效问题

### 特征库列表  

{% assign feature_files = site.static_files | where: "open_feature", true %}
{% for feature in feature_files %}
 [{{feature.name}}]({{ feature.path }})
{% endfor %}

### 私有特征库获取   
www.openappfilter.com  
 


