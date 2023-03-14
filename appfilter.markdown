---
layout: page
title: 应用过滤简介
permalink: /appfilter/
---

应用过滤是一款控制app联网的OpenWrt插件，支持抖音、斗鱼、王者荣耀、和平精英等几百款app过滤。

### 使用说明  
- 应用过滤和广告过滤、软硬件加速、多wan等模块冲突，请先关闭冲突模块使用，加速模块可在"网络-->网络加速(ACC)"菜单中关闭  
- 应用过滤依赖特征库，如果出现某些app不能过滤，请先更新特征库  
- 如果是高通AX系列产品，比如xiaomi AX3600、redmi AX6等，需要手动通过命令调整ecm慢速转发包个数，禁止硬件转发。 
  命令:  
  ```
  echo "1000000" > /sys/kernel/debug/ecm/ecm_classifier_default/accel_delay_pkts  
  ``` 

### 源码地址  
https://github.com/destan19/OpenAppFilter 


### 新官网地址  

www.openappfilter.com  

### 微信公众号（技术分享、资料、需求）  
公众号: OpenWrt  

### 应用过滤高级版(FROS)
基于OpenWrt开发了一套全新上网行为管理系统，包括应用过滤、网址过滤、上网记录、防沉迷等  
适合管理小孩上网行为，防止沉迷游戏，支持主流openwrt设备，比如红米AC2100、X86、k2p、r2s、r4s、k3等    
固件下载地址: www.fros.org.cn    


