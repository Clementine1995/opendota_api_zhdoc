# OpenDotaAPI 中文文档

当前版本v17.6.1，本文档会随官方文档同步更新（尽量）。

----
## API 总览
+ 介绍
通过调用OpenDota API可以获得Dota2相关数据，这些数据是从录像中提取出的高级数据。请求时最好保持约1/s。
从2018年4月22日开始，OpenDota API可每月免费调用50,000次。如果想要不限调用次数和更高请求率的服务的话，就要花点钱喽。查看[API页面](https://www.opendota.com/api-keys)可以购买一个key，带着这个key请求即可。

+ 认证
也就是api_key，带着这个key请求，不限调用次数，同时请求率也可以更高。
使用方式`Usage example: https://api.opendota.com/api/matches/271145478?api_key=YOUR-API-KEY`

安全方案类型|API KEY
请求参数名|api_key

+ [比赛](https://github.com/Clementine1995/opendota_api_zhdoc/blob/origin/dev/src/matches.md)

+ [玩家](https://github.com/Clementine1995/opendota_api_zhdoc/blob/origin/dev/src/players.md)

+ [职业选手](https://github.com/Clementine1995/opendota_api_zhdoc/blob/origin/dev/src/proPlayers.md)

+ [职业比赛](https://github.com/Clementine1995/opendota_api_zhdoc/blob/origin/dev/src/proMatches.md)

+ [公开比赛](https://github.com/Clementine1995/opendota_api_zhdoc/blob/origin/dev/src/pubMatches.md)

Explorer

元数据

分布

搜索

排名

基准

状态

安全

请求

英雄

英雄统计

联赛

队伍

录像

记录

直播

出装方案

架构