---
layout: page
title: 特征库
permalink: /feature/
---

### 特征库列表：

#### 非开源版本(FROS)
更新日志：  
- 1101更新内容  
增加英雄联盟手游  

- 0920更新内容
增加迷你世界、自由幻想、天下手游、天龙八部、一梦江湖、金铲铲之战、我叫MT4、神都夜行录、uu加速器、腾讯加速器
优化快手视频


{% assign feature_files = site.static_files | where: "feature", true %}
{% for feature in feature_files %}
 [{{feature.name}}]({{ feature.path }})
{% endfor %}


#### 开源版本

{% assign feature_files = site.static_files | where: "open_feature", true %}
{% for feature in feature_files %}
 [{{feature.name}}]({{ feature.path }})
{% endfor %}


