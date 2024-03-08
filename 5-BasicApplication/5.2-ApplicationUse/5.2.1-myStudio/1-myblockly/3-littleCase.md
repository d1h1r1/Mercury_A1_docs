# Small case

Let's write a small case to control the robotic arm to return to zero, move a joint 30 degrees, and then return to zero.

Learn how to use `myBlockly` for graphical programming through this case;



**Step one:** First click the `3D view` button to open the 3D view, where you can see the simulation changes of the robotic arm.



![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\1.png)

![](..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\2.png)



Click the `->` button of the 3D view panel to close the 3D view panel.





**Step 2:** Start programming

- Open the toolbox category `MDI Control` and drag the `Send Angles` block to the workspace; this block is used to set the angle value of the robotic arm. When the angle values are all zero, it means controlling the robotic arm to return to the zero point. ;Speed defaults to 20;

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\3.png" style="zoom:150%;" />

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\4.png" style="zoom:150%;" />



- Open the toolbox category `Time`, drag the `Sleep` building block to the workspace; and set the sleep time to 10 seconds;
  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\5.png" style="zoom:150%;" />





  and Set Sleep time to 10 s

    <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\6.png" style="zoom:150%;" />







- Open the toolbox category `MDI Control`, drag the `Send Angles` building block to the workspace; set J1 to 20;

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\7.png" style="zoom:150%;" />

- Open the toolbox category `Time`, drag the `Sleep` building block to the workspace; and set the sleep time to 5 seconds;

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\8.png" style="zoom:150%;" />

- Open the toolbox category `MDI Control`, drag the `Send Angles` building block to the workspace without changing any parameters;

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\9.png" style="zoom:150%;" />



- Click the Run button to start executing the code (observe the changes in the 3D model)


> What this code means is:
>
> - Control the robotic arm to return to zero point
> - Wait 10 seconds
> - Move joint one (J1) to a position of 20 degrees
> - Wait 5 seconds
> - Control the robotic arm to return to zero point







**Step 3:** Save and load the file (or save and load the workspace)



myBlockly supports saving and loading workspaces



- Click the `File` button and a drop-down menu will appear.

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\10.png" />



- After clicking the `Save` button, a pop-up window will appear. Click the `Save Workspace` button in it.

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\11.png" />



- Select the save path and click the `Save` button to save.








**Step 4:** Create a new workspace operation (this operation will clear all codes in the workspace)



- Click the `File` button and a drop-down menu will appear.
  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\10.png" />



- Click the `Create` button, a warning box will pop up, click `Ok`.
  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\13.png" />



- Created

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\14.png" />







**Step 5:**Load workspace operation, load the file we saved before

- Click the `File` button and a drop-down menu will appear

- After clicking the `Open File` button, click Load Workspace
  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\15.png" />



- After selecting the file path, click the Open button


- Loaded

  <img src="..\..\..\..\resources\5-BasicApplication\5.2-ApplicationUse\5.2.1-mystudio\1-myblockly\images\3\9.png" />

---

  [← Previous Page](./2-interface_description.md) | [Next Page →](./4-quickMove.md)

