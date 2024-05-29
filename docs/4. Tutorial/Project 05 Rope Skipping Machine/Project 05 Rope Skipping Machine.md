# Project 05: Rope Skipping Machine

![5-1](media/5-1.png)

## 1. Overview
Rope skipping machine is used to replace the traditional rope skipping method, which frees our hands. It can not only realize forward and reverse jumps, but also change the speed of skipping ropes according to needs.



## 2. Components
|![Img](../media/kidsuno.png)|![Img](../media/Joystick.png)|![Img](../media/360°.png)| ![Img](../media/Buzzer.png)|
| :--: | :--: | :--: | :--: |
|Kidsuno Mainboard×1|Joystick Module×1|360°Servo×1|Passive Buzzer×1|
|![Img](../media/Connection.png)|![Img](../media/USB.png)|![Img](../media/Lego11.png)|  |
|Connection Wire×2|USB Cable×1| Lego Series×1 |  |
![Img](../media/5-2.png)

## 3. Installation 

Please refer to the following link：https://www.dropbox.com/scl/fo/dtu6zv41pd82c71yb65q8/h?rlkey=kzegu8g8jkjieaeqfjxif6kii&dl=0



## 4. Read the Value of Joystick Module
![Img](../media/5-3.png)

## 5. Programming Steps

#### Step1：Wiring Diagram

Connect the kidsuno mainboard and computer via a USB cable, and connect the joystick module to No.3 interface, passive buzzer to No.2 interface and the 360° servo to the G, V and D13 interface of the mainboard. The brown wire is connected to G, the red wire is connected to V and the orange wire is connected to D13.
![Img](../media/5-dd.png)

#### Step2：Add Joystick Module 

![Img](../media/xin55.png)
![Img](../media/12.png)
Diagram of the **Extension** Instruction Block

![Img](../media/551.png)
Add “**Joystick Module **” Instruction Block
![Img](../media/552.png)

#### Step3: Description of Building Blocks

![Img](../media/553.png)
This block is used to read the analog value of the X-axis of the joystick module (range: 0~1023).

![Img](../media/554.png)
This block is used to read the analog value of the Y-axis of the joystick module (range: 0~1023).

![Img](../media/555.png)
This block is used to read the button value of the joystick module (1/0).

![Img](../media/556.png)
This block is used to refresh the value of the joystick module.

#### Step4：Write the Program
① Drag the instruction block ![Img](../media/16.png)in the **Events** module to the script area.

![Img](../media/17.png)



② Drag the instruction block ![Img](../media/28.png)in the **Serial** module to the script area and take the baud rate 9600 as an example.

![Img](../media/29.png)



③ Drag the instruction block  ![Img](../media/558.png)in the **Control** module to the script area.

![Img](../media/557.png)

④ Drag the instruction block![Img](../media/556.png)in the **I2C Joystick Module ** module to the script area and place it into the block ![Img](../media/558.png).


![Img](../media/559.png)

⑤ Drag the instruction block![Img](../media/33.png) in the **Serial** module to the script area, then change “**Hello KidsBlock**” to “**X:**, **warp** to **no-warp**.
![Img](../media/560.png)

⑥ Drag the instruction block![Img](../media/33.png) in the **Serial** module to the script area and place it into the block ![Img](../media/558.png), then change **warp** to **no-warp**.


![Img](../media/561.png)

⑦ Drag the instruction block![Img](../media/555.png)in the **I2C Joystick Module ** module to the script area and place it into the block ![Img](../media/562.png), then change “**button” to  X**.


![Img](../media/563.png)

⑧ Copy block![Img](../media/564.png)twice，then change “**X：** ” to “ **Y：** and “ **btn_val：**”，and change “**X**” to “**Y**” and “**button”**，the  **no-warp**  behind “**Button” **to **warp**.
![Img](../media/565.png)

⑨ Drag the instruction block ![Img](../media/26.png)in the **Control** module to the script area and change the number 1 to 0.2.
![Img](../media/566.png)

⑩ Complete Program
![Img](../media/567.png)

#### Step5：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up,  then  click ![Img](../media/38.png) in the serial monitor area to set the baud rate to 9600, then the serial monitor will print the analog and digital values read by the joystick module.

In the original state, the read analog values of X and Y are about 512. When moving in the direction of the arrow, the value gradually increases, as the arrow moves in the opposite direction, the value decreases gradually. When the joystick module is not pressed, it is low level (0); when pressed, it is high level (1).
![Img](../media/568.png)
![Img](../media/570.png)

## 6. Joystick Module Controls Rope Skipping Machine
![Img](../media/5-4.png)

## 7. Programming Steps

#### Step1: Flow Chart

Set the 360° servo angle to 90°(won't rotate), then read values of the joystick module, if the X value is greater than 512, the rope skipping machine jumps from back to front and the speed changes, otherwise it jumps from front to back. Press the joystick module, passive buzzer will play music, otherwise it won't play music.
![Img](../media/d58.png)

#### Step2：Add Servo and Passive Buzzer
![Img](../media/569.png)

#### Step3：Write the Program

①  Find building blocks
（1）![Img](../media/43.png)
<br>         
（2）![Img](../media/44.png)
<br>
（3）![Img](../media/z44.png)
<br>
（4）![Img](../media/47.png)
<br>
（5）![Img](../media/46.png)
<br>
（6）![Img](../media/571.png)
<br>
（7）![Img](../media/z43.png)
<br>
（8）![Img](../media/D56.png)
<br>
② Complete Program
![Img](../media/572.png)

#### Step4：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, if the X value is greater than 512, the rope skipping machine jumps from back to front and the speed changes, otherwise it jumps from front to back. Press the joystick module, passive buzzer will play music, otherwise it won't play music.

![5-9](media/5-9.png)

## 8. Expansion Project
![Img](../media/5-7.png)

The sample code is below：
![Img](../media/5-8.png)





















