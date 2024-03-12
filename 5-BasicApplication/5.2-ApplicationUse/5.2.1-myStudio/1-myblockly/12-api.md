# API Introduction



## System Status

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\system\1.png)



**Get End Firmware Info**

- **Prototype**：`get_atom_version()`

- **Interface Description**：Get End Firmware Info

- **Return**：Return hte End Firmware Info



**Get Master Control Info**

- **Prototype**：`get_system_version()`

- **Interface Description**：get system version

- **Return**：system version









## Basic

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\basic\1.png)



**Set basic pin**

- **Prototype**：`set_basic_output(id,state)`
- **Interface Description**：set basic output
- **Params**：

    - `id`：pin
    - `state`：output state



**Get basic pin**

- **Prototype**：`get_basic_output(id)`
- **Interface Description**：get basic output
- **Params**：
    - `id`： pin
- **Return**：
    - state







## Atom IO

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\atom\1.png)

**Set Color**

- **Prototype**：`set_color(red=0,green=0,blue=0)`
- **Interface Description**：set led color
- **Params**

* `red`: 0 - 255
    * `green`: 0 -255
* `blue`: （0- 255）



**setting PWM console value**

- **Prototype**：`set_pwm_output(v1=0,v2=0,v3=0)`
- **Interface Description**：set PWM
- **Params**
    * **v1** (_int_)

    * **v2** (_int_)

    * **v3** (_int_)



**set pinmode value**

- **Prototype**：`set_pin_mode(id,state)`
- **Interface Description**：set pinmode
- **Params**
    * `id`：pin
    * `state`：state



**setting IO value**

- **Prototype**：`set_digital_output(id,state)`
- **Interface Description**：set io
- **Params**
    * `id`：io

    * `state`：0 | 1



**Get IO value**

- **Prototype**：`get_digital_input(id)`
- **Interface Description**：get io value
- **Params**
    * `id`：io id







## Status

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\status\1.png)



**Power On**

- **Prototype**：`power_on()`
- **Interface Description**：Atom open communication



**Power Off**

- **Prototype**：`power_off()`
- **Interface Description**：Atom close communication



**Obtain the host computer error status**

- **Prototype**：`get_robot_status()`

- **Interface Description**：Obtain the error safety status of the host computer

- **Return**：

  - status information



**Is Power On**

- **Prototype**：`is_power_on()`
- **Interface Description**：Check whether the robot arm is powered on

- **Return**：

    - `1`: power on
    - `0`：power off
    - `-1`: error



**Is the end LED button pressed**

- **Prototype**：`is_power_on()`
- **Interface Description**：Check if the end LED button is pressed

- **Return**：
  - `1`: pressed
  - `0`：unpressed



**Release All Servos**

- **Prototype**：`release_all_servos()`

- **Interface Description**：release all servos



**Focus all servos**

- **Prototype**：`focus_all_servos()`
- **Interface Description**：focus all servos



**Restore All Servos**

- **Prototype**：`servo_restore(254)`
- **Interface Description**：resotre all servos



**Restore Joint Servo**

- **Prototype**：`servo_restore(id)`
- **Interface Description**：restore joint servo
- **Params**
  * `id`：joint id（1 - 7）



**Is Controller Connected**

- **Prototype**：`is_controller_connected()`
- **Interface Description**：check atom
- **Return**：
    - `0`：unconnected
    - `1`：connected











## MDI Control

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\mid\1.png)

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\mid\2.png)

**Get Angles**

- **Prototype**：`get_angles()`
- **Interface Description**：get all angles
- **Return**：

    - angles



**Get Coords**

- **Prototype**：`get_coords()`

- **Interface Description**：

  - coords



**Set Joint**

- **Prototype**：`send_angle(id, degree, speed)`

- **Interface Description**：Robot single joint angle control

- **Params**

   - `id`：joint ID：1-7

   - `degree`：degree

   - `speed`：speed



**Send Coord**

- **Prototype**：`send_coord(id, value, speed)`
- **Interface Description**：Robot single coordinate control

- **Params**
   - `id`：coords:1-6 correspond to x, y, z, rx, ry, rz respectively
   - `value`：data
   - `speed`：1-100



**Angles is in position**

- **Prototype**：`is_in_position([j1,j2,j3,j4,j5,j6,j7],0)`

- **Interface Description**：Check whether the machine angle reaches the specified position

- **Params**：
  - `j1`
  - `j2`
  - `j3`
  - `j4`
  - `j5`
  - `j6`
  - `j7`



- **Return**：
  - 0：Did not reach the specified location
  - 1：Arrive at designated location





**Coords is in position**

- **Prototype**：`is_in_position([x,y,z,rx,ry,rz],1)`

- **Interface Description**：Check whether the machine angle reaches the specified position

- **Params**：
  - x

  - y

  - z

  - rx

  - ry

  - rz



- **Return**：

  - 0：is in position
  - 1：is not in position





**Is Moving**

- **Prototype**：`is_moving(id, value, speed)`
- **Interface Description**：check robot is moving?
- **Return**：
   - 0：is not moving
   - 1：is moving



**Send Angles**

- **Prototype**：`send_angles(angles,speed)`
- **Interface Description**：send all angles

- **Params**
   - `angles`：angles（`List[float]`）
   - `速度`: (`int`) 0 ~ 100



**Set Coord**

- **Prototype**：`send_coords（coords,speed）`

- **Interface Description**：set coords

- **Params**
- `coords`：coord（`List[float]`）
   - `speed`: (`int`) 0 ~ 100







## JOG Control

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\jog\1.png)





**Jog Angle**

- **Prototype**：`jog_angle（joint_id,direction,speed）`

- **Interface Description**：jog angle control

- **Params**

   - `joint_id`: (`int`) 1 ~ 7

   - `direction`: `0` - reduce，`1` - increase

   - `speed`: 0 ~ 100




**Jog Absolute**

   - **Prototype**：`jog_absolue（coord_id,direction,speed）`

   - **Interface Description**：Jog Absolute

   - **Params**

     - `coord_id`: (`int`) 1 ~ 6
     - `direction`：
     - `speed`: 0 ~ 100



**Jog Coord**

- **Prototype**：`jog_coord（coord_id,direction,speed）`
- **Interface Description**：Jog control coordinates

- **Params**
- `coord_id`: (`int`) 1 ~ 6
   - `direction`: `0` - reduce，`1` - Increase
   - `speed`: 0 ~ 100





**Jog Increment**

- **Prototype**：`jog_increment（coord_id,direction,speed）`

- **Interface Description**：step mode

- **Params**

   - `coord_id`: (`int`) 1 ~ 6
   - `方向`：
   - `速度`: 0 ~ 100



**Set Servo encoder**

- **Prototype**：`set_encoder（joint_id,encoder）`

- **Interface Description**：Set Servo encoder

- **Params**

  - `joint_id`: (`int`) 1 ~ 7

  - `encoder`: 0 ~ 4096



**Get Servo encoder**

- **Prototype**：`get_encoder(joint_id)`
- **Interface Description**：Get Servo encoder
- **Params**: `joint_id`: (`int`) 1 ~ 6
- **Return**：
  - `编码器`：0 ~ 4096





**Pause**

- **Prototype**：`pause()`
- **Interface Description**：pause



 **Resume**

- **Prototype**：`resume()`
- **Interface Description**：resume



**Stop**

- **Prototype**：`jog_stop()`
- **Interface Description**：stop





## CCADA

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\ccada\1.png)





**Get the value of deflection angle in null space**

- **Prototype**：`get_solution_angles()`
- **Interface Description**：Get the zero space deflection angle value
- **Return值**：
  - `J1_angle_low`：-90  ~ +90
  - `J1_angle_high`：-90  ~ +90



**Set the value of deflection angle in null space**

- **Prototype**：`set_solution_angles(J1_angle,speed)`
- **Interface Description**：Set the zero space deflection angle value
- **Params**：
  - `J1_angle`：-90  ~ +90
  - `speed`：1-100







## Setting

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\setting\1.png)



**Get Joint Min angle**

- **Prototype**：`get_joint_min_angle(joint_id)`
- **Interface Description**：Get Joint Min angle
- **Params**：`joint_id`：(`int`)
- **Return**：value（`float`）



**Get Joint Max angle**

- **Prototype**：`get_joint_max_angle(joint_id)`

- **Interface Description**：Get Joint Max angle

- **Params**：`joint_id`：(`int`)

- **Return**：value（`float`）



**Set Joint Min Angle**

- **Prototype**：`set_joint_min(id, angle)`
- **Interface Description**：Set Joint Min Angle

- **Params**：
   - `id`

   - `angle`



**Set Joint Max Angle**

- **Prototype**：`set_joint_max(id, angle)`
- **Interface Description**：Set Joint Max Angle

- **Params**：
   - `id`
   - `angle`





## Servo

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\servos\1.png)



**Is Servo Enable**

- **Prototype**：`is_servo_enable(servo_id)`

- **Interface Description**：Is Servo Enable

- **Params**：`servo_id` (`int`) 1 ~ 7

- **Return**：
   - `0`：off

   - `1`: on

   - `-1`: error



**Is All Servo Enable**

- **Prototype**：`is_all_servo_enable()`

- **Interface Description**：Is All Servo Enable?

- **Return**：

   - `0`：off
   - `1`: on
   - `-1`: error



**Set Servo data**

- **Prototype**：`set_servo_data(servo_no, data_id, value)`
- **Interface Description**：Set Servo data

- **Params**：
   - `servo_no`：1 - 7。
   - `data_id`：address。
   - `value`：0 - 4096



**Get Servo data**

- **Prototype**：`get_servo_data(servo_no, data_id)`
- **Interface Description**：Read the data Params of the specified address of the servo.
- **Params**：

   - `servo_no`：，1 - 7。
   - `data_id`：data address
- **Return**：
- `值`：0 - 4096




**Set Servo Calibration Servo**

- **Prototype**：`set_servo_calibration(servo_no)`
- **Interface Description**：The current position of the calibration joint actuator is the angle zero point, and the corresponding potential value is 2048.

- **Params**：
   - `servo_no`：1 - 7。



**Joint Brake**

- **Prototype**：`joint_brake(servo_id)`
- **Interface Description**：Joint Brake
- **Params**：`servo_id`：1 ~ 7





**Release Servo**

- **Prototype**：`release_servo(servo_id)`
- **Interface Description**：Power off the designated servo
- **Params**：`servo_id`：1 ~ 7



**Foucs Servo**

- **Prototype**：`focus_servo(servo_id)`
- **Interface Description**：Power on the designated servo
- **Params**：`servo_id`：1 ~ 7





## Gripper

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\gripper\1.png)



**Set Pro Adaptive Gripper**

- **Prototype**：`set_gripper_enabled(flag)`
- **Interface Description**：Set Pro Adaptive gripper
- **Params**：`flag`：1  |  0





**Set Gripper Calibration**

- **Prototype**：`set_gripper_calibration()`
- **Interface Description**：Set the current position to zero and set the current position value to `2048`.





**Set Gripper State**

- **Prototype**：`set_gripper_state(flag, speed, mode)`

- **Interface Description**：set gripper state

- **Params**

   - `flag` (`int`)：0 - open，1 - close
   - `speed` (`int`): 0 ~ 100
   - `mode`：gripper type



**Set Gripper Value**

- **Prototype**：`set_gripper_value(value，speed，mode)`

- **Interface Description**：Set gripper value

- **Params**

   - `value`（int）：0 ~ 100
   - `speed`（int）：0 ~ 100
   - `mode`：gripper type



**Get Gripper Value**

- **Prototype**：`get_gripper_value(mode)`
- **Interface Description**：get gripper value
- **Return**：value（int）





**Is Gripper Moving**

- **Prototype**：`is_gripper_moving()`

- **Interface Description**：Determine whether the fixture is moving

- **Return**：

    - `0`: No movement
    - `1`: moving
    - `-1`: wrong data





**Set Gripper Mode**

- **Prototype**：`set_gripper_mode(status)`
- **Interface Description**：Set Gripper Mode
- **Params**
- `status` (`int`): 0 - Transparent Transmission。 1 - Port Mode。





**Get Gripper Mode**

- **Prototype**：`get_gripper_mode()`

- **Interface Description**：Get Gripper Mode

- **Return**
- `status` (`int`): 0 - Transparent Transmission。 1 - Port Mode。





## Coord Control

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\coords\1.png)



**Get Tool coordinate system**

- **Prototype**：`get_tool_reference()`
- **Interface Description**：Get Tool coordinate system
- **Return**：`list` [x，y，z，rx，ry，rz]





**Set Tool Coord**

- **Prototype**：`set_tool_reference(coords)`

- **Interface Description**：set tool reference

- **Params**：
   - `coords`: (`list`) [x, y, z, rx, ry, rz]。



**Get World coordinate system**

- **Prototype**：`get_world_reference()`
- **Interface Description**：get world reference
- **Return**：`list` [x，y，z，rx，ry，rz]。





**Set World Coord**

- **Prototype**：`set_world_reference(coords)`

- **Interface Description**：Set World Reference

- **Params**：
   - `coords`: (`list`) [x, y, z, rx, ry, rz]。



**Get Reference Frame**

- **Prototype**：`get_reference_frame()`
- **Interface Description**：get reference frame。
- **Return**：
  - 0 - base
  - 1 - tool。



**Set Reference Frame**

- **Prototype**：`set_reference_frame(rftype)`

- **Interface Description**：Set Reference Frame

- **Params**：
   - `rftype`：0 - base 1 - tool



**Get Movement Typye**

- **Prototype**：`get_movement_type()`
- **Interface Description**：Get Movement Typye
- **Return**：1 - movel，0 - moveJ。



**Set Movement Typye**

- **Prototype**：`set_movement_type(move_type)`

- **Interface Description**：Set Movement Typye

- **Params**：
   - `move_type`：1 - movel，0 - moveJ。



**Get End Coord**

- **Prototype**：`get_end_type()`
- **Interface Description**：Get End Coord Reference
- **Return**：0 - flange，1 - tool。



**Set End Coord**

- **Prototype**：`set_end_type(end)`

- **Interface Description**：Set End Coord

- **Params**：
   - `end`：0 - flange，1 - Tool。







## Servo Status

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\servos_status\1.png)





**Get Joint Velocity**

- **Prototype**：`get_servo_speeds()`

- **Interface Description**：get speed



**Get The State of Each Joint**

- **Prototype**：`get_servo_status()`

- **Interface Description**：Get The State of Each Joint




**Get Servo Currents**

- **Prototype**：`get_servo_currents()`
- **Interface Description**：Get Servo Currents





## 485

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\api\485\1.png)





**485 Restore factory settings**

- **Prototype**：`tool_serial_restore()`

- **Interface Description**：485 restore





**Set up communication**

- **Prototype**：`tool_serial_ready()`
- **Interface Description**：485 communication
- **Return**：
  - 0：unsuccess
  - 1：success





**Read 485 buffer length**

- **Prototype**：`tool_serial_available()`
- **Interface Description**：Read 485 buffer length
- **Return**：
  - data





**Readfixed length data**

- **Prototype**：`tool_serial_read_data(id)`
- **Interface Description**：read fixed length data
- **Params**：
  - `id`:1-45
- **Return**：
  - data





**Send data**

- **Prototype**：`tool_serial_write_data(data)`
- **Interface Description**：send data
- **Params：**
  - data
- **Return**：
  - data length





**Clear buffer**

- **Prototype**：`tool_serial_peek()`

- **Interface Description**：Clear buffer







**View the first data in the buffer**

- **Prototype**：`get_servo_speeds()`
- **Interface Description**：view the first data in the buffer
- **Return**：data







**Set 485 baud rate**

- **Prototype**：`tool_serial_set_baud(baud)`
- **Interface Description**：set baud
- **Params**：
  - `baud`：baud





**Set 485 timeout**

- **Prototype**：`tool_serial_set_timeout(timeout)`
- **Interface Description**：Set 485 timeout
- **Params**：
  - `timeout`：timeout




---

[← Previous Page](.\9-pumpUse.md) | [Next Page →](.\11-Q%26A.md)