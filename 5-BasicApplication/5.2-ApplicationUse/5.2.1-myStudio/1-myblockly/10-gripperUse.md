# Use of gripper

<i>Preparation before you start</i>

- Make sure the robotic arm is connected to the computer

- Make sure the machine is functioning properly

- Make sure the machine is powered on

Grippers include adaptive grippers, electric grippers and pneumatic grippers. Here we take the adaptive gripper as an example to explain how to use myBlockly to control the gripper.



### Learning content of this chapter

How to use myBlockly to control an adaptive gripper attached to a Mercury A1 robotic arm



#### API display

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\gripperUse\1.png" style="zoom: 67%;" />

We will use the following modules



- **Module 1**: `Set Gripper State`: Make the gripper enter the specified state (open or closed) at the specified speed

  * Parameter introduction:

     This module has two parameters that can be adjusted:

     * Clamp status parameters: closed state, open state

  * Speed parameter: indicates the speed of rotation, the value range is 0~100

     * Clamp type parameter: Select adaptive clamp here





- `Module 2`: `Set Gripper Value`: Make the gripper reach the specified position at the specified speed
  - Parameter introduction:
      - Claw value parameter: Indicates the position that the gripper will reach, and the value range is 0~100.
      - Speed parameter: represents the speed of rotation, the value range is 0~100.
      - Clamp type parameter: Select adaptive clamp here





* Module **3**: `Is Gripper Moving`: Determine whether the fixture is running






#### small case

The graphics code is as follows:

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\gripperUse\2.png" style="zoom: 80%;" />



* The execution effect of the code:

  - Control the adaptive gripper to open at a speed of 20

  - Wait three seconds

  - Control the adaptive gripper to reach the position with a value of 80 at a speed of 20

  - wait 0.1 seconds
  - Print out the detection value of `whether the gripper is moving`



**Notice**:

If you are unable to control the gripper from the example above, perhaps you need to set the gripper mode to passthrough mode

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\gripperUse\3.png"  />

After setting it up, then run the small case code again.








---

[← Previous Page](./7-program.md) | [Next Page →](./9-pumpUse.md)
