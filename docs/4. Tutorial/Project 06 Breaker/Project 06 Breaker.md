# Project 06: Breaker

![6-1](media/6-1.png)

## 1. Overview
Breaker is a machine that can level out uneven pavement. In this project, we will make one together!



## 2. Components
|![Img](../media/kidsuno.png)|![Img](../media/Button.png)|![Img](../media/270°.png)|![Img](../media/Connection.png)|
| :--: | :--: | :--: |:--: |
|Kidsuno Mainboard×1|Button Module×1|270° Servo×1|Connection Wire×1|
|![Img](../media/wheel.png)|![Img](../media/USB.png)|![Img](../media/Lego11.png)| |
|Wheel×4|USB Cable×1| Lego Series×1 | |
|![Img](../media/6-2.png)|||

## 3. Installation 

Please refer to the following link：https://www.dropbox.com/scl/fo/dtu6zv41pd82c71yb65q8/h?rlkey=kzegu8g8jkjieaeqfjxif6kii&dl=0



## 4. Read the Button Value
![Img](../media/6-3.png)

## 5. Programming Steps

#### Step1：Wiring Diagram

Connect the kidsuno mainboard and computer via a USB cable, and connect the button module to No.2 interface and the 270° servo to the G, V and D13 interface of the mainboard. The brown wire is connected to G, the red wire is connected to V and the orange wire is connected to D13.
![Img](../media/6-DD.png)

#### Step2: Description of Building Blocks
Please refer to Project 02: Mixer

#### Step3：Write the Program
① Drag the instruction block ![Img](../media/16.png)in the **Events** module to the script area.

![Img](../media/17.png)



②  Drag the instruction block ![Img](../media/28.png)in the **Serial** module to the script area and take the baud rate 9600 as an example.

![Img](../media/29.png)



③ Drag the instruction block![Img](../media/30.png)
in the **Pins** module to the script area. Since the button module is connected to D6 of No.2 interface on the mainboard, then change the number 0 to 6 .

![Img](../media/31.png)

④ Drag the instruction block  ![Img](../media/27.png)in the **Control** module to the script area.

![Img](../media/32.png)



⑤ Drag the instruction block![Img](../media/33.png) in the **Serial** module to the script area.

![Img](../media/34.png)

⑥ Drag the instruction block ![Img](../media/23.png)in the **Pins** module to the script area and put it into the block ![Img](../media/33.png), then change the number 0 to 6.

![Img](../media/35.png)

⑦ Drag the instruction block ![Img](../media/26.png)in the **Control** module to the script area and change the number 1 to 0.2.

![Img](../media/36.png)



⑧ Complete Program

![Img](../media/37.png)



#### Step4：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, then  click ![Img](../media/38.png) in the serial monitor area to set the baud rate to 9600. The serial monitor will print the value read by the button module, when you press the button on the module, it will output a low level (0); when you release it, it will output a high level (1).

![Img](../media/3777.png)




## 6. Button Controls Breaker
![Img](../media/6-4.png)

## 7. Programming Steps

#### Step1: Description of Building Blocks

Variable block:
![Img](../media/661.png)

![Img](../media/662.png)
It is a conditional statement code executing **if-then ** function: If the logical judgment statement in ![Img](../media/39.png) is satisfied, the code statement below **then** is executed.

![Img](../media/663.png)
It is a conditional loop statement, it will loop forever if the condition in ![Img](../media/39.png) is satisfied.



#### Step2: Flow Chart

Set the 270° servo to 95°. When the button on the module is pressed, the long arm of the breaker will be raised; when released, it will be lowered. (press the button and then release it will complete a beat.) 
![Img](../media/DD66.png)

#### Step3：Add **Servo **
![Img](../media/42.png)

#### Step4：Write the Program
①  Find building blocks
（1）![Img](../media/43.png)
<br>
（2）![Img](../media/664.png)
<br>
（3）![Img](../media/665.png)
<br>
（4）![Img](../media/666.png)
<br>
（5）![Img](../media/667.png)
<br>
（6）![Img](../media/668.png)
<br>
（7）![Img](../media/669.png)
<br>
（8）![Img](../media/670.png)
<br>
② Complete Program

![Img](../media/Z1213.png)
![Img](../media/678.png)

#### Step5：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up. When the button on the module is pressed, the long arm of the breaker will be raised; when released, it will be lowered. (press the button and then release it will complete a beat.) 

![6-7](media/6-7.png)















