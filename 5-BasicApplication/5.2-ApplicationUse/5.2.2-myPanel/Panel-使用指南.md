#Mercury Panel 使用指南

##1 Mercury Panel简介

Mercury Panel是一款通过触摸机械臂底座的cm4对水星机械臂进行控制的应用。它的功能有坐标控制、角度控制、拖动示教等），便于操作人员与大象机器人进行交互，正确使用大象机器人。


适用设备：

-Mercury A1

**使用之前请务必下载更新atom和basic固件**

##2 如何使用

在确保了你的机器已经配置panel的开机自启后，开机即运行panel。运行panel时，用户能直观的看到可以点击的按钮以及对应的注释，开机默认为上电状态（上电状态末端rbg灯会亮）。界面左上角的灰色三角为返回上一界面，右上角的×为关闭界面，

###2.1 拖动示教
点击主界面的拖动示教进入拖动示教界面。

![pic](./resources/case/main1.png)

进入拖动示教界面机械臂整体放松，移动到示教起点。

![pic](./resources/dragplay.png)

点击开始录制，录制时顶部会实时显示录制时长（录制时长不得超过60秒，否则有弹窗警告，需要退出拖动示教界面重新进入），拖动机械臂录制点位，点击结束录制，机械臂锁紧，录制完成。

![pic](./resources/case/dragplaybegin.png)
![pic](./resources/case/dragplayend.png)

录制过程中点击暂停录制后机械臂整体锁紧，继续录制点位点击继续录制。

![pic](./resources/case/dragplaypause.png)

点击单次执行，播放一次录制完成的动作；点击持续执行，循环播放录制动作，点击停止，执行完当前动作后停止播放。

![pic](./resources/case/dragplayrecord.png)
![pic](./resources/case/dragplaycontinue.png)


###2.2 运动控制

点击主界面的快速移动进入快速移动界面，进入快速移动界面选择角度控制或者坐标控制。

![pic](./resources/case/main2.png)

角度控制：选择要操作的关节，控制分为连续运动和步进运动。选择run下的持续，此时为连续运动，按下按钮后，直到释放按钮才会停止（达到限位后也会停止）；选择run下的1毫米/度或者5毫米/度（步进值），此时为步进运动，点击+增加对应的步进值，点击-减少对应的步进值，步进运动到达点位就会停止（比如关节1现在角度30，增量值50，按下减号这边按钮，那么机械臂运动到-20就会停止）。

![pic](./resources/case/quickmoveangle1.png)

坐标控制：在使用坐标控制之前，需要将机械臂调整到合适的姿态（例如关节4：-90°）。选择要操作的坐标轴，控制分为连续运动和步进运动。选择run下的持续，此时为连续运动，按下按钮后，直到释放按钮才会停止（达到限位后也会停止）；选择run下的1毫米/度或者5毫米/度（步进值），此时为步进运动，点击+增加对应的步进值，点击-减少对应的步进值，步进运动到达点位就会停止（比如X轴现在坐标30，增量值50，按下加号这边按钮，那么机械臂运动到80就会停止）。RA为冗余臂角。

![pic](./resources/case/quickmovecoord1.png)

自由移动：按下自由移动按钮进入自由移动模式，atom的rgb灯变色，持续按下末端的rgb按钮机械臂整体放松，可对机械臂整体进行自由移动，松开末端的rgb按钮机械臂整体锁紧。再次点击自由移动退出自由移动模式。

![pic](./resources/case/freemove.png)
![pic](./resources/case/freemove1.png)

###2.3 整机运行状态
点击主界面的电机状态进入电机状态界面，查看电机连接状态，通过全部锁紧和全部放松可以对机械臂整体进行放松和锁紧操作。

![pic](./resources/case/main3.png)
![pic](./resources/motorstatus.png)

点击主界面的设置进入设置界面。

![pic](./resources/case/main4.png)
![pic](./resources/settings1.png)

在此界面你可以点击IO状态查看atom和basic对应的IO状态。

![pic](./resources/case/io.png)
![pic](./resources/ioconnections.png)

IO状态界面设置引脚高低电平暂未开发。

![pic](./resources/case/ioset.png)

监听模式暂未开发。

![pic](./resources/case/settingsmonitor.png)

点击电源->开，上电，上电过程需等待7s；点击电源->关，掉电，掉电过程需等待3秒。

![pic](./resources/case/poweron.png)
![pic](./resources/case/poweroff.png)

点击快速测试->多动，机械臂开始一轮多个点位的运动；点击快速测试->老化，机械臂开始循环一组大幅度点位的运动，再次点击老化，机械臂进行完当前这轮动作后停止。

点击黄色小三角，翻页。

![pic](./resources/case/changepage1.png)
![pic](./resources/case/changepage2.png)

点击语言进入语言设置界面，可以选择应用程序的主题语言。

![pic](./resources/case/language.png)
![pic](./resources/setlanguage.png)

点击串口进入串口控制界面。点击串口连接->开，打开串口；串口连接->关，关闭串口。

![pic](./resources/case/serial.png)
![pic](./resources/serial.png)

点击校准进入校准界面。可以对每个电机进行灵位校准：点击掉电放松机械臂对应关节，拖动对应关节到达新的零位，点击校准对应关节锁紧，校准完成。

![pic](./resources/case/calibrate.png)
![pic](./resources/calibrate.png)

Log界面暂未开发。

![pic](./resources/case/settingsnextlog.png)

点击关于进入关于界面，查看应用版本。

![pic](./resources/case/about.png)
![pic](./resources/about.png)
