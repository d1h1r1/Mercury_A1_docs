# 小案例

我们来写一个小案例，控制机械臂回零，并使一关节移动 30 度的位置，然后再回到零点。

通过这案例来学习如何使用 `myBlockly `来进行图形化编程；



**第一步：**首先点击 `3D视图` 按钮，打开3D视图，在这里可以看到 机械臂的仿真变化。



![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\1.png)

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\3d_view.png)



- 1：关闭三维视图面板：单击三维视图面板的“>>”按钮关闭三维视图。
- 2：点击四个按钮可以切换摄像头的位置。
- 3：未连接到机器时，机器人的角度和坐标信息默认设置为零，连接到机器后会自动获取数据。





**第二步：**开始编程

- 打开工具箱分类 `角度和坐标`，拖动`设置全角度`积木块到工作区；这个积木块用于设置机械臂的角度值，当角度值全为零时，代表控制机械臂回到零点；速度默认为 20；

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\3.png" style="zoom:150%;" />





  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\4.png" style="zoom:150%;" />



- 打开工具箱分类 `时间`，拖动`睡眠`积木块到工作区；并设置睡眠时间为 3 秒；



  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\5.png" style="zoom:150%;" />





  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\6.png" style="zoom:150%;" />







- 打开工具箱分类 `角度和坐标`，拖动`设置全角度`积木块到工作区；设置 J1 为 20；

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\7.png" style="zoom:150%;" />

- 打开工具箱分类 `时间`，拖动`睡眠`积木块到工作区；并设置睡眠时间为 3 秒；

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\8.png" style="zoom:150%;" />

- 打开工具箱分类 `角度和坐标`，拖动`设置全角度`积木块到工作区，不改变任何参数；

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\9.png" style="zoom:150%;" />



- 点击 运行 按钮，开始执行代码（观察3D模型的变化）


> 这段代码的意思是：
>
> - 控制机械臂回到零点
> - 等待 3 秒钟
> - 使 一关节（J1） 移动到30 度的位置
> - 等待 3 秒钟
> - 控制机械臂回到零点







**第三步：**保存 和 加载 文件（或者说保存加载工作区）



myBlockly 支持 工作区的保存和加载



- 点击`文件`按钮，出现一个下拉菜单

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\10.png" />



- 点击 `保存` 按钮后会出现一个弹窗，点击其中的`保存工作区`按钮

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\11.png" />



- 选择保存的路径，点击`保存`按钮，即可保存
  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\12.png" />







**第四步：** 新建工作区 操作（这个操作会清空工作区所有代码）



- 点击`文件`按钮，出现一个下拉菜单
  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\10.png" />



- 点击 `新建工作区` 按钮，会弹出一个警告框，点击`确认` 即可
  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\13.png" />



- 新建完成

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\14.png" />








**第五步：**加载工作区 操作，加载我们之前保存的文件

- 点击`文件`按钮，出现一个下拉菜单

- 点击 `打开文件` 按钮后，点击加载工作区

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\15.png" />



- 选择文件路径后，点击打开按钮

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\16.png" />



- 加载完成

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\littleCase\9.png" />

---

  [← Previous Page](./2-interface_description.md) | [Next Page →](./4-autofill.md)

