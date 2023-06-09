# threejs版本的控制系统（前后端demo开源/效果可以看readme文件）


# demo ver1.0 

整理出了demo版本，不涉及公司的真实数据和核心算法逻辑。数据都是我随便生成的。

然后去除正式项目中的权限逻辑，自动生成地图逻辑，和自动生成定位点/入库点逻辑。更改复用逻辑。

添加后端demo（聊天示例，rmtp示例，table示例）

前端使用说明：

```

npm install 之后 
npm run serve
http://localhost:8080/#/apartmentArea


```

后端使用说明：

```

1. cd 进去behind
2. chat文件夹是聊天demo，ffmpeg文件夹是rmtp的demo，最后 table文件夹 是3d交互的逻辑demo和生成demo的demo。
3. 只有table文件夹有数据库

```


## demo ver0.33 

调用高德api在数据大屏界面增加查看当前区域拥堵情况
/data5

## demo ver0.32 

监控调参，不再有花屏的现象了。
对数据大屏的理解进行了改动。路径
/data2  /data3  /data4

## demo ver0.31 接入了监控系统，可以点击下面的select进行监控视角的切换。

新增后端 behind/ffmpeg后端转flv.rar 由于rmtp协议不能在web端直接进行呈现。因此在该后端在2000会暴露一个视频转接的url.

<img src="./readme/monitor.png" style="width:100%"/>

## demo ver0.3 新加了数据可视化大屏

路径：data
<img src="./readme/data.png" style="width:100%"/>

## demo ver0.2

新加上了移动端适配

<img src="./readme/移动端1.png" style="width:25%"/>
<img src="./readme/移动端3.png" style="width:27%"/>
<img src="./readme/移动端2.png" style="width:27%"/>

## demo ver0.1新加上了agv建模，和模拟取车的场景

<img src="./readme/agv.png" />

<img src="./readme/agv1.png" />

<img src="./readme/agv2.png" />


一些后端示例，像是聊天功能，table功能我放在behind文件夹下面




## 功能1：最简单的登录注册，表格方面增删改查


<img src="./readme/login.png" />

这里满足用户最基本的功能，复现桌面c++的基本功能

<img src="./readme/table.png" />
<br>

## 功能2：3d效果之停车时间标签，监控功能，dashboard表格，扫描视角，第一人称

<br>

<img src="./readme/标签.png" />

<br>

停车时间标签是为了更直观的看到各个车子停车的时间


<br>
<img src="./readme/监控录像.png" />

<br>

监控功能是桌面c++的功能，在这个web端的应用我也将其搬了过来

<br>

<img src="./readme/表格1.png" />
<br>

这里的dashboard提供可视化管理表格，这里是我随便用echarts做了一下，这里的样式优化空间是很大的.

<br>

<br>

扫描视角的想法我是在8.6号下午跟杨经理聊天的时候他提到的有一些报警和报错并不能很直观的显示出来，这里的扫描视角gif图片上虽然呈现的不多，但是我的源码上给样式等级设置了三个样式，根据传入的type级别分成info，warning，error等级。并且对应着3d场景的具体坐标

<br>
<img src="./readme/扫描1.png" />

<br>
第一人称功能的功能是锦上添花，在我的构思中他可以在扫描想法中出作用，也可以在等一下功能的聊天功能中发挥作用。（又：第一人称其实是在开高达）
<br>





## 功能3：切换楼层+以车作为第一人称的效果

当时构思的时候，我觉得如果把整个楼做一个出来会有臃肿的情况出现，并且楼层之间的显示不直观，因此我设计了一个右上角的gui按钮，点击右上角就可以切换楼层。楼层和楼层之间做了一些简单的效果用以区别不同的楼层



<br>

以车作为第一人称的效果说实话可能用处并不大，但是我觉得可以加上去，只属于锦上添花的内容吧，没准以后会有用

<br>

<br>

## 功能4：安全门控制+数据大屏

<br>

安全门功能是桌面c++的功能，直接把他搬了过来

<img src="./readme/安全门.png" />


<br>

数据大屏还是起到一个直观看数据的作用吧，里面是一个3d模型和一个vr数据，可以转着浏览内部的信息。并且给出一些直观数据

<img src="./readme/ar.png" />



## 功能5：实现聊天功能

<br/>
这部分我使用express合socket简单写了一个后端，做这个的原因是可以让登录该系统的管理员进行一个简单的沟通

<img src="./readme/聊天.png" />