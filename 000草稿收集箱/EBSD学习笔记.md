---
等级: ⭐⭐⭐
---

# 1.EBSD菊池花样的算法
- % [直播回放丨EBSD菊池花样的算法_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1by41187Q7/?spm_id_from=333.788.player.switch&vd_source=d1167fc706d8bb4a356a82d19d9d3304)
## 1. EBSD菊池花样思考科学真相
![image.png|500](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125201712.png)

1. 交点、线、宽度
2. 同一个晶面族，线的宽度一样（同一个晶面族产生的衍射线）
3. 线与线的夹角与晶面之间的夹角，存在关联关系
4. 线与线之间的夹角（晶面与晶面之间相交，产生晶带轴）（晶带轴）
5. TEM光源是平行光源，只能看到一个轴的信息；但是EBSD能看到很多交点，是多个晶带轴的信息
6. [[高端人才]]培养的不是现成的知识，而是根据现象去分析未知信息，探索未知知识（**不要降低要求，去培养一个只会操作的劳动者，而是成为有创造力的高端人才**）
7. EBSD软件自动标识，自动计算
## 2.EBSD的原理
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125201958.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125202411.png)

1. θ角和晶面间距是有关系
## 3. EBSD菊池花样的算法
> [!note] EBSD菊池花样的算法
> - 1、菊池线的交点位置按==心射投影==的数学方法计算。
> - 2、按[[晶体衍射]][[消光规律]]把各交点连成线，就构成了计算的菊池花样 
> 	- a. 先标定晶带轴的位置
> 	- b. 根据[[晶体衍射]]和[[消光规律]]，把点连成线
> 	- c. 把线的宽度标定出来
> - 3、菊池线的交点指数（晶带轴)与晶面指数的必需满足晶带轴定律（相互垂直）。
### 1. 心射投影
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125203335.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125203516.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125203632.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125204033.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125204150.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125204712.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125204745.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125204803.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125204900.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125204918.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125205130.png)

![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125205032.png)
## 4. 算法的验证与实测菊池花样的解析
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125205550.png)
## 5. EBSD的应用
> [!tip] EBSD的应用
> 1. 1、一个菊池花样就能确定晶系、点阵、晶胞参数信息（值得重视）
> 2. 2、检测晶粒大小、微观晶粒取向及百分比、晶粒取向差信息、晶界信息。 
> 3. 3、检测缺陷区的位置、百分比，其中包括了位错信息。
> 4. 4、获得ODFs分布图，极图和反极图的信息（这些是数学计算）。
> 5. 5、建议重视实测菊池花样图，直接用实测菊池花样图取代由计算获得的极图、反极图和ODFs图。

# 2. EBSD——极图织构分析
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125210839.png)

## 1. 极图织构分析
![image.png|900](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125212155.png)
## 2. 极图的定义和物理含义
![image.png|1000](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125213005.png)
## 3. 极氏网和吴氏网
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125213136.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125213350.png)
## 4.实验极图的测量方法
![image.png|1200](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125214111.png)
## 5. 用织构模拟理论及图的方法
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125214555.png)

## 6. 实测极图分析方法总结
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125214929.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125215009.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125215035.png)
# 3. 晶体织构的形成规律
## 1. 丝织构的形成规律
![image.png|1000](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125221052.png)
![image.png|1000](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125221143.png)
![image.png|1000](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125221613.png)
![image.png|1000](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125221733.png)


---
## 2. 板织构的形成规律
![image.png|1000](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241125221916.png)


## 3. 取向因子的计算与各向异性的关联




