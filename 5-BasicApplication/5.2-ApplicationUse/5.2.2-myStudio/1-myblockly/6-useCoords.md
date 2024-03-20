#Learn to use coordinate control

*before the start*

> *1. Make sure the machine is powered on*
>
> *2. Make sure the machine connection is normal*



This chapter learns how to use coordinates to control a robotic arm.



### Mainly involved APIs:

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\useCoords\send_coord.png" />

**Set single coordinate**

- **Prototype**: `send_coord(id,value,speed)`
- **Interface Description**: Set a single coordinate of the robotic arm
- **Parameters:**
   - id: 1-6 (X, Y, Z, RX, RY, RZ)
   - value: coordinate value
   - speed: speed value is 1-100





<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\useCoords\send_coords.png" />

**Set multiple coordinates**

- **Prototype**: `send_coords(values,speed)`
- **Interface Description**: Set multiple coordinates of the robotic arm
- **Parameters**:
   - values: [X,Y,Z,RX,RY,RZ]
   - speed: speed value is 1-100





### Small case

#### Before using coordinate movement for the first time, some operations need to be performed:

- Robot arm returns to zero
- Set the initial posture of the robot arm coordinate movement

As shown in the code below:

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\useCoords\init_position.png" />

Click to run code

>This code means:
>
>- Robotic arm returns to zero
>- wait 10 seconds
>- Set the 4 joints of the robotic arm to move to the -90 position.





#### Set the single-coordinate Z-axis movement of the robot arm

Set the Z-axis of the robot arm to move to the position of 300 with a speed of 20

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\useCoords\z_move.png" />

Click to run the code and observe the status of the robotic arm







#### Set up multi-coordinate movement of the robotic arm

<img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\useCoords\coords_move.png" />





#### Use quick move for coordinate movement






---

[← Previous Page](./5-quickMove.md) | [Next Page →](./7-chatGPT.md)