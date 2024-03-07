# 程序的DEBUG

本章学习 通过 运行 面板来调试我们的代码，实现程序的暂停、单步执行、停止 功能



编辑一段控制 机械臂末端 LED 灯颜色变化的程序

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\7\1.png"  />





点击`运行按钮`，当运行面板弹出后，马上点击 `暂停按钮`，程序会在执行完第一条指令`time.sleep(5)` 后暂停

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\7\2.png"  />



程序已暂停。已出现下一条要执行的指令`mc.set_color(255,0,0)`

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\7\3.png"  />

此时：

- 如果点击`恢复`按钮，程序将会自动往下执行；

- 如果点击`单步执行`按钮，程序会执行下一条指令，即`mc.set_color(255,0,0)`；
- 如果点击`停止`按钮，程序会被终止；





至于接下来如何操作，由您自己决定吧！


---

[← Previous Page](./6-singleStep.md) | [Next Page →](./8-gripperUse.md)