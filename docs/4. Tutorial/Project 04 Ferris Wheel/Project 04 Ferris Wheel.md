# Project 04: Ferris Wheel

![4-1](media/4-1.png)

## 1. Overview

When it comes to the Ferris wheel, we must be familiar with it. Sitting on the Ferris wheel, we are able to overlook the surrounding scenery from a height. Thus, in this project, we will work to make a Ferris wheel that can be viewed in the rain.



## 2. Components
|![Img](../media/kidsuno.png)|![Img](../media/Steam.png)|![Img](../media/Buzzer.png)|![Img](../media/360°.png)|
| :--: | :--: | :--: | :--: |
|Kidsuno Mainboard|Steam Sensor×1|Passive Buzzer×1|360°Servo×1|
|![Img](../media/Connection.png)|![Img](../media/USB.png)|![Img](../media/Lego11.png)| |
|Connection Wire×2|USB  Cable×1| Lego Series×1 | |
|![Img](../media/4-2.png)||||

## 3. Installation 

Please refer to the following link：https://www.dropbox.com/scl/fo/dtu6zv41pd82c71yb65q8/h?rlkey=kzegu8g8jkjieaeqfjxif6kii&dl=0



## 4. Play Music
![Img](../media/4-3.png)

## 5. Programming Steps

#### Step1：Wiring Diagram

Connect the kidsuno mainboard and computer via a USB cable, and connect the steam sensor to No.7 interface, passive buzzer to No.6 interface and the 360° servo to the G, V and D13 interface of the mainboard. The brown wire is connected to G, the red wire is connected to V and the orange wire is connected to D13.
![Img](../media/4-DD.png)



#### Step2: Write《Twinkle, twinkle, little star!》
![Img](../media/4-4.png)

#### Step3：Add Passive Buzzer Command Module
![Img](../media/D41.png)
![Img](../media/12.png)

Diagram of the **Extension** Instruction Block

![Img](../media/D42.png)
Add “**Passive Buzzer**” Instruction Block

![Img](../media/D43.png)

#### Step4: Description of Building Blocks
![Img](../media/D44.png)
Set the play frequency of the passive buzzer to the specified pin.

![Img](../media/D45.png)
Set the play frequency and beat of the passive buzzer to the specified pin.

![Img](../media/D46.png)
Set the passive buzzer to play specific music to the specified pin.

![Img](../media/D47.png)
Set the passive buzzer to the specified pin without sound.



#### Step 5：Write the Program
① Drag the instruction block ![Img](../media/16.png)in the **Events** module to the script area.

![Img](../media/17.png)



② Drag the instruction block![Img](../media/D48.png)in the **Passive Buzzer** module to the script area. Since the interface of the passive buzzer module is connected to the D4 pin of the No. 6 interface on the mainboard, change the number 2 to number 4. This module can play different notes via the parameter "NOTE_C4", and the parameter "1/4" can be used to adjust beat. (C4 refers to playing in the midrange state, where 4 represents the pitch of the note, and it can also be replaced by D4, G4 and A4 )
![Img](../media/D49.png)

③ Duplicate![Img](../media/4-11.png)13 times, then change NOTE_C4 and 1/4, as shown below:
![Img](../media/4-12.png)

④Drag the instruction block![Img](../media/4-13.png)in the **Passive Buzzer** module to the script area, then change the number 2 to number 4.
![Img](../media/4-14.png)

⑤ Complete Program
![Img](../media/4-15.png)

#### Step 6：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, then passive buzzer will play music.




## 6. Steam Sensor Detects Water
![Img](../media/4-17.png)

## 7. Programming Steps

#### Step1: Write the Program

① Drag the instruction block ![Img](../media/16.png)in the **Events** module to the script area.

![Img](../media/17.png)

② Drag the instruction block ![Img](../media/28.png)in the **Serial** module to the script area and take the baud rate 9600 as an example.

![Img](../media/29.png)

③ Drag the instruction block![Img](../media/30.png)
in the **Pins** module to the script area. Since the steam sensor is connected to A0 of No.7 interface on the mainboard, then change the number 0 to A0 .

![Img](../media/Z31.png)

④ Drag the instruction block  ![Img](../media/27.png))in the **Control** module to the script area.

![Img](../media/Z32.png)



⑤ Drag the instruction block![Img](../media/33.png) in the **Serial** module to the script area.

![Img](../media/Z33.png)



⑥ Drag the instruction block ![Img](../media/Z34.png)in the **Pins** module to the script area and put it into the block ![Img](../media/33.png).

![Img](../media/Z35.png)



⑦ Drag the instruction block ![Img](../media/26.png)in the **Control** module to the script area and change the number 1 to 0.3.

![Img](../media/Z36.png)

⑧ Complete Program
![Img](../media/Z37.png)

#### Step2：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, then  click ![Img](../media/38.png) in the serial monitor area to set the baud rate to 9600. Then the serial monitor will print the value read by the steam sensor.

Touch the metal detection area on the sensor with a moistened finger, the larger the area, the greater the value!
![Img](../media/Z38999.png)

## 8. Steam Sensor Controls Servo and Buzzer
![Img](../media/4-18.png)

## 9. Programming Steps

#### Step1: Flow Chart

Set the 360° servo angle to 90°, then read the analog value of the steam sensor. When the analog value is greater than 500, the servo and Ferris wheel will rotate, and the buzzer will play music; otherwise, the the servo and Ferris wheel will not rotate, and the buzzer does not sound.

![Img](../media/D57.png)

#### Step2：Add **Servo **Instruction Block 

![Img](../media/42.png)



#### Step3：Write the Program
①  Find building blocks

（1）![Img](../media/43.png)
<br>   
（2）![Img](../media/44.png)
<br>   
（3）![Img](../media/Z42.png)
<br>
（4）![Img](../media/47.png)
<br>
（5）![Img](../media/D55.png)
<br>
（6）![Img](../media/D56.png)
<br>
（7）![Img](../media/48.png)
<br>

② Complete Program
![Img](../media/4-19.png)

#### Step4：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, then drop water on the metal detection area of the sensor. When the analog value is greater than 500, the servo and Ferris wheel will rotate, and the buzzer will play music; otherwise, the the servo and Ferris wheel will not rotate, and the buzzer does not sound.

![4-23](media/4-23.png)

## 10. Expansion Project
![Img](../media/4-21.png)

The sample code is below：
![Img](../media/4-22.png)

