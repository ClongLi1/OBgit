---
cssclass:
  - cards
---
# 天气预报
```dataviewjs     
let setting = {};      
//在和风天气中创建的 Api key
setting.key = "e432e1a280d344cd89befe667f366400";
setting.city = "山阳";//城市名
setting.days = 7;//天气预报天数
setting.headerLevel = 1;//添加标题的等级
setting.addDesc = true;//是否添加描述
setting.onlyToday = false;//是否只在当天显示
setting.anotherCity = "内乡";//添加另外一个城市

//脚本文件 weatherView.js 所在路径
dv.view("100附件文件/1000附件/weatherView",setting)
```

# 动态天气

<iframe width="1400" height="1000" src="https://embed.windy.com/embed2.html?lat=29.344&lon=112.017&detailLat=25.040&detailLon=121.469&width=650&height=450&zoom=5&level=surface&overlay=wind&product=ecmwf&menu=&message=&marker=&calendar=now&pressure=&type=map&location=coordinates&detail=&metricWind=default&metricTemp=default&radarRange=-1" frameborder="0"></iframe>
