# 夹爪的使用

<i>开始前的准备工作</i>

- 确保机械臂已连接至电脑

- 确保机器正常

- 确保机器已通电

夹持器包括自适应夹持器、电动夹持器和气动夹持器。 这里我们以自适应抓手为例，讲解如何使用myBlockly来控制抓手。



### 本章学习内容

如何使用 myBlockly 控制连接到 Mercury A1 机械臂的自适应夹爪

#### API display

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\gripperUse\1.png" style="zoom: 67%;" />

我们将用到以下几个模块



- **1**: `设置夹爪状态`：使夹爪以指定的速度进入指定的状态（张开或闭合）

  * 参数介绍：

    该模块有两个可以调整的参数：

    * 夹爪状态参数：闭合状态，打开状态
  * 速度参数：表示旋转的速度，取值范围0~100
    * 夹具类型参数：此处选择自适应夹具





- 模块二 **2**: `设置夹爪值`：使夹具以指定的速度到达指定的位置



  参数介绍：

  该模块有两个可以调整的参数：

  * 夹爪值参数：表示夹爪要到达的位置，取值范围为 0~100。
  * 速度参数：表示旋转的速度，取值范围0~100。
  * 夹具类型参数：此处选择自适应夹具





* 模块 **3**: `夹爪是否在运动`：判断夹具是否正在运行






#### 小案例

图形代码如下：

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\gripperUse\2.png" style="zoom: 80%;" />



* 代码的执行效果：

  - 控制自适应夹爪以 20 的速度打开

  - 等待三秒

  - 控制自适应夹爪以 20 的速度 到达 值 为 80 的位置

  - 等待 0.1 秒
  - 打印输出 `夹爪是否在运动` 的检测值



**注意**:

如果您无法从上面的示例中控制夹爪，也许您需要将夹爪模式设置为 透传模式

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\gripperUse\3.png"  />

设置完后，然后再次运行小案例代码。








---

[← Previous Page](./9-program.md) | [Next Page →](./11-pumpUse.md)
