# 机械臂使用场景案例

本章通过经典机械臂使用案例，展示产品在代表性场景中的应用，涵盖机械臂在不同领域的典型应用，凸显产品的通用性和适用性，让用户通过这些案例深入了解机械臂在实际应用中的灵活性和性能，为在具体场景中的应用提供参考。

## 1.绘画案例：

```python
from pymycobot.mycobot import MyCobot
import time
import math

#创建MyCobot实例，指定串口和波特率
mc = MyCobot('COM3',115200)

#发送目标坐标点，使机械臂移动到指定位置
mc.send_coords([52.9, -64.4, 409.7, -91.23, -0.25, -89.81], 50, 0)
#暂停2秒
time.sleep(2)

#发送目标坐标点，使机械臂移动到另一指定位置
mc.send_coords([21.5, 145.5, 233.6, -89.72, 19.19, 13.45], 50, 0)
#暂停2秒
time.sleep(2)

#循环发送目标坐标点，使机械臂做圆形轨迹运动
for i in range(1, 361):
x = 21.5 + 30 * math.cos(i / 180.0 * math.pi)
y = 145.5 + 30 * math.sin(i / 180.0 * math.pi)
mc.send_coords([x, y, 233.6, -89.72, 19.19, 13.45], 100, 0)
#暂停0.7秒
time.sleep(0.7)

#发送目标坐标点，使机械臂回到初始位置
mc.send_coords([52.9, -64.4, 409.7, -91.23, -0.25, -89.81], 50, 0)
```

## 2. 跳舞案例：

```python
from pymycobot.mycobot import MyCobot
import time

if __name__ == '__main__':
#创建MyCobot实例，指定串口和波特率
mc = MyCobot('COM3',115200)

#设置开始时间
start = time.time()
#让机械臂到达指定位置
mc.send_angles([-1.49, 115, -153.45, 30, -33.42, 137.9], 80)
#判断是否到达指定位置
while not mc.is_in_position([-1.49, 115, -153.45, 30, -33.42, 137.9], 0):
#让机械臂恢复运动
mc.resume()
#让机械臂运动0.5s
time.sleep(0.5)
# 暂停机械臂运动
mc.pause()
# 判断移动是否超时
if time.time() - start > 3:
break
# 设置开始时间
start = time.time()
# 让运动持续30秒
while time.time() - start < 30:
# 让机械臂快速到达位置
mc.send_angles([-1.49, 115, -153.45, 30, -33.42, 137.9], 80)
# 设置灯光的颜色为[0,0,50]
mc.set_color(0, 0, 50)
time.sleep(0.7)
# 让机械臂快速到达位置
mc.send_angles([-1.49, 55, -153.45, 80, 33.42, 137.9], 80)
# 将灯光颜色设置为 [0,50,0]
mc.set_color(0, 50, 0)
time.sleep(0.7)
```

## 3. 木块运输案例：

```python
from pymycobot import PI_PORT, PI_BAUD
import time
def gripper_test(mc):
Print("开始检查api的IO部分\n")
# 检测夹钳是否在移动
flag = mc.is_gripper_moving()
Print("夹钳是否在移动：{}".format(flag))
time.sleep(1)

# 将当前位置设置为(2048)。
​ # 确定需要时再使用。
# 夹钳初始化时间长，一般不需要改方法。
# mc.set_gripper_ini()
# 设置关节点1，让其旋转到2048位置
mc.set_encoder(1, 2048)
time.sleep(2)
# 设置六个关节位置，让机械臂以20的速度旋转到此位置

mc.set_encoders([1024, 1024, 1024, 1024, 1024, 1024], 20)
# mc.set_encoders([2048, 2900, 2048, 2048, 2048, 2048], 20)
# mc.set_encoders([2048, 3000,3000, 3000, 2048, 2048], 50)
time.sleep(3)
# 获取关节点的位置信息1
Print(mc.get_encoder(1))
#设置夹爪旋转到2048位置
mc.set_encoder(7, 2048)
time.sleep(3)
#设置夹爪旋转到1300位置
mc.set_encoder(7, 1300)
time.sleep(3)

#让夹爪以70的速度达到2048状态，2048会报错，所以改成255。
mc.set_gripper_value(255, 70)
time.sleep(3)
#让夹爪以70的速度达到1500状态，1500会报错，所以改成255
mc.set_gripper_value(255, 70)
time.sleep(3)
​
num=5
while num>0:
# 设置夹爪状态，让其以70的速度快速张爪
mc.set_gripper_state(0, 70)
time.sleep(3)
​ ​ #设置夹爪状态，让其以70的速度快速合爪
mc.set_gripper_state(1, 70)
time.sleep(3)
num-=1

# 获取夹爪的值
Print("")
Print(mc.get_gripper_value())
# mc.release_all_servos()

if __name__ == "__main__":
# 创建MyCobot实例，并指定串口和波特率
mc = MyCobot('COM3',115200)

mc.set_encoders([2048, 2048, 2048, 2048, 2048, 2048], 20)
time.sleep(3)
gripper_test(mc)

```