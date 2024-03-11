# 学习使用坐标控制

*开始之前*

> *1、确保机器已上电*
>
> *2、确保机器连接正常*



本章学习如何使用坐标来控制机械臂。



### 主要涉及到的API：

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\useCoords\send_coord.png" />

**设置单坐标**

- **原型**：`send_coord(id,value,speed)`
- **接口说明**：设置机械臂单个坐标
- **参数：**
  - id：1-6（X，Y，Z，RX，RY，RZ）
  - value：坐标值
  - speed：速度 值为 1-100





<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\useCoords\send_coords.png" />

**设置多坐标**

- **原型**：`send_coords(values,speed)`
- **接口说明**：设置机械臂多坐标
- **参数**：
  - values：[X,Y,Z,RX,RY,RZ]
  - speed：速度 值为 1-100





### 小案例

#### 首次使用坐标移动前，需要执行的一些操作：

- 机械臂回零
- 设置机械臂坐标运动的初始姿态

如下图代码所示：

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\useCoords\init_position.png" />

点击运行代码

>这段代码的意思是：
>
>- 机械臂回零
>- 等待10秒
>- 设置机械臂4关节移动到 -90 的位置。





#### 设置机械臂单坐标 Z 轴移动

设置机械臂 Z 轴移动到 300 的位置，速度为 20

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\useCoords\z_move.png" />

点击运行代码，观察机械臂状态







#### 设置机械臂多坐标移动

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\useCoords\coords_move.png" />





#### 使用快速移动进行坐标运动






---

[← Previous Page](./5-quickMove.md) | [Next Page →](./7-chatGPT.md)