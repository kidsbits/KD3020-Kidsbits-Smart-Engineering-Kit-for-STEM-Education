# Project 03: Windmill

![3-1](media/3-1.png)

## 1. Overview
In this project, we are going to make a mini windmill.


## 2. Components
|![Img](../media/kidsuno.png)|![Img](../media/Rotary.png)|![Img](../media/360°.png)|
| :--: | :--: | :--: |
|Kidsuno Mainboard×1|Rotary Potentiometer×1|360°Servo×1|
|![Img](../media/Connection.png)|![Img](../media/USB.png)|![Img](../media/Lego11.png)| 
|Connection Wire×1|USB Cable×1| Lego Series×1 | 
![Img](../media/3-2.png)

## 3. Installation 
Please refer to the following link：https://www.dropbox.com/scl/fo/dtu6zv41pd82c71yb65q8/h?rlkey=kzegu8g8jkjieaeqfjxif6kii&dl=0



## 4. Read the Value of Rotary Potentiometer
![Img](../media/3-17.png)

## 5. Programming Steps

#### Step 1：Wiring Diagram

Connect the kidsuno mainboard and computer via a USB cable, and connect the rotary potentiometer to the No.7 interface, the 360° servo to the G, V and D13 interface of the mainboard. The brown wire is connected to G, the red wire is connected to V and the orange wire is connected to D13.
![Img](../media/3-DD.png)

#### Step 2: Description of Building Blocks

![Img](../media/Z34.png)
This block is used to read analog value of the specified pin (range: 0~1023).

#### Step 3：Write the Program
① Drag the instruction block ![Img](../media/16.png)in the **Events** module to the script area.

![Img](../media/17.png)



② Drag the instruction block ![Img](../media/28.png)in the **Serial** module to the script area and take the baud rate 9600 as an example.

![Img](../media/29.png)

③ Drag the instruction block![Img](../media/30.png)
in the **Pins** module to the script area. Since the rotary potentiometer is connected to A0 of No.7 interface on the mainboard, then change the number 0 to A0.
![Img](../media/Z31.png)

④ Drag the instruction block  ![Img](../media/27.png)in the **Control** module to the script area.
![Img](../media/Z32.png)

⑤ Drag the instruction block![Img](../media/33.png) in the **Serial** module to the script area.
![Img](../media/Z33.png)

⑥ Drag the instruction block ![Img](../media/Z34.png)in the **Pins** module to the script area and put it into the block ![Img](../media/33.png).
![Img](../media/Z35.png)

⑦ Drag the instruction block ![Img](../media/26.png)in the **Control** module to the script area and change the number 1 to 0.3.
![Img](../media/Z36.png)

⑧ Complete Program
![Img](../media/Z37.png)

#### Step 4：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, then  click ![Img](../media/38.png) in the serial monitor area to set the baud rate to 9600. Then the serial monitor will print the value read by the rotary potentiometer. When the knob on the potentiometer is rotated in one direction, the analog value will gradually increase; otherwise, it will decrease.
![Img](../media/Z38.png)

## 6. Rotary Potentiometer Controls Windmill to Rotate
![Img](../media/3-18.png)

## 7. Programming Steps

#### Step1: Description of Building Blocks

![Img](../media/Z39.png)
This block is a mapping block, and mapping is a way of mapping each element (called a "key") in one data set to a unique element (called a "value") in another set. This correspondence can be represented in the form of a key-value pair, where each key corresponds to a value.

For example: how does the analog value of the rotary potentiometer correspond to the rotation angle of the 360° servo?
Here you need to use "<span style="color: rgb(255, 169, 0);">mapping module</span>" to map the analog value (0 ~ 1023) to the rotation angle of the 360° servo (90 °~180°). After mapping, when the analog value is 0, the angle of the servo is 90°(won't rotate), and when the analog value is 1023, the angle of the servo is 180° ( the servo speed is maximum), as shown below.
![Img](../media/3-19.jpg)

#### Step2：Flow Chart
Set the 360° servo angle to 90°. When the knob on the potentiometer is rotated, the analog value of the potentiometer is mapped to the angle of the servo to control its speed.
![Img](../media/Z40.png)

#### Step3：Add **Servo **Instruction Block 
![Img](../media/42.png)

#### Step4：Write the Program
①  Find building blocks
（1）![Img](../media/43.png)
<br>         
（2）![Img](../media/44.png)
<br>
（3）![Img](../media/Z42.png)
<br>
（4）![Img](../media/z43.png)
<br>
（5）![Img](../media/z44.png)
<br>
（6）![Img](../media/Z41.png)
<br>

② Complete Program
![Img](../media/z45.png)

#### Step5：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, then rotate the knob on the potentiometer by hand, and the speed of the windmill will gradually increase.

![Img](../media/3-23.png)

## 8. Expansion Project
![Img](../media/3-21.png)

The sample code is below：
![Img](../media/z46.png)



