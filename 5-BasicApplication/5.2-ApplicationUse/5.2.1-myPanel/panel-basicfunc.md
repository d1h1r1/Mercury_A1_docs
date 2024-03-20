# 1 Move quickly
Joint and coordinate control in the **QuickMove** page, through the selection of coordinate control and Angle control to enter the interface control, control the movement of the robot arm can be divided into **continuous motion**, **step motion**, continuous motion press the button until the button is released, the robot arm will not stop moving; Stepping movement, set up incremental, robotic arm to reach the point will stop. <br>

## 1.1 Angle control

Angles are joint control, Joint1-7 corresponds to joint 1-7 respectively <br>
Function Description: <br>
Run place choose continuous or 1/5 step value. Angles of each joint has a button to add and subtract Angle, decrease the Angle by the side of the minus sign button, button Angle according to the plus sign here. Continuous motion, after pressing the button, it will not stop until the release button (it will also stop after reaching the limit), and the stepping movement will stop when it reaches the point (for example, joint 1 is at an Angle of 30 with an incremental value of 50, press the button on the side of the minus sign, then the robot arm will stop when it moves to -20). <br>

## 1.2 Coord control

**Note:** Before using coordinate control, it is necessary to make the robot arm reach a certain attitude through Angle control, otherwise coordinate control cannot be performed. <br>

Coords for coordinate control < br >
Function description: < br >
Select a continuous or step value of 1/5 at run. Each coordinate axis of Coords can be selected, and the corresponding coordinate is reduced by pressing the button on the minus side and increased by pressing the button on the plus side. Continuous movement, after pressing the button, it will not stop until the release button (it will stop after reaching the limit), and the stepping movement will stop when it reaches the point (for example, the X-axis is now coordinate 30, the increment value is 50, press the button on the side of the plus sign, then the robot arm will stop when it moves to 80). <br>

## 1.3 free to move
Press the free move button to enter the free move mode, and the rgb light of atom will change color. By continuously pressing the rgb button at the end of the robot arm, the overall movement of the robot arm will be relaxed, and the overall locking of the rgb button at the end will be released. Click Free Move again to exit Free Move mode.

# 2 Drag & Play

## 2.1 recorded 
After entering the drag teaching interface, the robot arm will relax as a whole. After clicking the recording button, the following actions will be recorded. After clicking the recording button again, the robot arm will be locked as a whole and the recorded actions can be played after the recording is completed. Can click the pause button in the process of recording, suspended track record, the mechanical arm as a whole will lock, click continue to record the mechanical arm can relax, at this time into the recording state, continue the previous recorded track record.

## 2.2 execute
The recorded actions can be played continuously or once. The "Continue" button plays the recorded actions in a loop. The "Once" button plays only one action.

# 3 motor state

## 3.1 Condition monitoring

The motor status interface will refresh the motor connection status in real time.

## 3.2 Motor control

Can through motor state interface of two buttons (focus motors, release motors), respectively, for the whole mechanical arm lock and relaxed operation.

# 4 settings

## 4.1 IO Connections
IO interface can be real-time refresh atom and state the basic state of IO v.

## 4.2 Power On
Click the power on button to power on the robot arm, and the power-on process is close to 7 seconds.

## 4.3 Power Off
Button, click on electricity to mechanical arm off electricity, close to the electrical process for 3 seconds.

## 4.4 Mobility Test
Hyperactivity test, multiple levels of mechanical arm of each joint movement.

## 4.5 Aging Test
Aging test, mechanical arm movement, a group of the larger point again before clicking this button will not stop, click again after the execution of the current action to stop.

## 4.6 language Settings
Set the application language.

## 4.7 serial port
Serial interface to connect and disconnect the communication serial port operation, a serial port is the connection state by default.

## 4.8 Calibration
Calibration interface can click on the power button on the corresponding mechanical arm joints to relax, moved to the new zero point, click on the calibration, zero update lock and joints.

## 4.9 About
Information about interface has a version number.