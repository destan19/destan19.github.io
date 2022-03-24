---
layout: page
title: 特征库
permalink: /feature/
---

### 特征库列表：

{% assign feature_files = site.static_files | where: "open_feature", true %}
{% for feature in feature_files %}
 [{{feature.name}}]({{ feature.path }})
{% endfor %}


