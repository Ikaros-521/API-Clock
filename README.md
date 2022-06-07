# 前言

本项目基于Cordova开发，打包的apk支持Android9+，主要功能为 监听b站用户直播情况，开播进行闹钟提示

## 使用介绍

1、首次安装运行程序时会提示权限获取，如果没有给予相应权限则部分功能无法正常使用。（存储权限用于配置本地化，网络用于API请求）  
2、运行后，可以进行相应的设置（初次使用可以直接点击“配置初始化”，自动完成默认配置）。  
功能页：  
1）闹钟提醒的音频文件（正常mp3等格式），设置成功后，下方的音频控件会加载音频信息（如果没有加载，可能是文件格式或路径原因，请重新选择文件；另外记得调下音量）；
2）UID填写监听B站用户的UID，UID与UID直接用“空格”分隔；  
3）轮循间隔是循环调用API的时间差，设置时间越大，开播响应就越慢，流量消耗越少（虽然也要不了几个流量，但不建议太快，有可能会被禁IP）；  
设置页：  
1）可以修改背景图片；  
ps：由于音频和背景图片都是临时生成的加密url，软件重启后则无法正常定位到文件，所以重启后需要重新进行设置。  
3、相关配置完成后，回到“功能”页，点击“保存配置”就会写入配置到本地文件中“Documents/APIClock/baseInfo.json”。
4、所有配置完成后，点击“自启动运行”即可。程序会程序运行并输出必要的日志。  
5、当有设置的用户开播后，程序会“播放音乐”并不在监测此用户，如需继续监听此用户，可以重新点击“自启动运行”。
如需关闭程序可以点击“停止运行”或直接关闭程序。  
6、日志内容说明：日志有“红、绿、灰、橙”四种颜色，如果出现红色日志，则表示运行出了一些问题，常见的问题为基本是 权限授予问题和网络问题。
日志过多时可以点击“清空日志”或者“每分钟清空日志”来进行日志清理。  
  

## 效果图

## 已测机型

小米10  
vivo x23  


## 插件安装

cordova plugin add cordova-plugin-file  
cordova plugin add cordova-plugin-media  
cordova plugin add cordova-plugin-autostart@2.3.0  
cordova plugin add cordova-plugin-background-mode  
cordova plugin add cordova-plugin-android-permissions  
