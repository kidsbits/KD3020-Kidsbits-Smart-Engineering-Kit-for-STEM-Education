# Project 02: Mixer

![2-1](media/2-1.png)

## 1. Overview

Mixer is a kind of construction engineering machinery, which is mainly used for mixing some building materials such as cement, sand and gravel. In this project, we will seek to design a mixer.



## 2. Components
|![Img](../media/kidsuno.png)|![Img](../media/Capacitive.png)|![Img](../media/360°.png)|
| :--: | :--: | :--: |
|Kidsuno Mainboard×1|Digital Capacitive Touch Sensor×1|360°Servo×1|
|![Img](../media/Connection.png)|![Img](../media/USB.png)|![Img](../media/Lego11.png)|
|Connection Wire×1|USB Cable×1| Lego Series×1 |
![Img](../media/2-2.png)

## 3. Installation 
Please refer to the following link：https://www.dropbox.com/scl/fo/dtu6zv41pd82c71yb65q8/h?rlkey=kzegu8g8jkjieaeqfjxif6kii&dl=0

## 4. Read the Value of Digital Capacitive Touch Sensor
![Img](../media/2-3.png)

## 5. Programming Steps

#### Step 1：Wiring Diagram
Connect the kidsuno mainboard and computer via a USB cable, and connect the digital capacitive touch sensor to the No.2 interface, the 360° servo to the G, V and D13 interface of the mainboard. The brown wire is connected to G, the red wire is connected to V and the orange wire is connected to D13.
![Img](../media/2-DD.png)

#### Step 2: Description of Building Blocks

![Img](../media/21.png)
The block is used to set serial baud rate(generally, the baud rate 9600 is taken as an example)

![Img](../media/22.png)
This block is used to set print mode for the serial port. **warp** means line feed printing, **no-warp** means no line feed printing, **HEX** means hexadecimal printing.

![Img](../media/23.png)
It is used to read the digital signal(0 or 1) of the specified pin

![Img](../media/24.png)
This is a command block used to set "**input**" or "**output**" to the specified pin.  "**input**" means input mode;  "**output**" represents output mode;  "**input-pullup**" means setting input mode for the pin and making the pin become high level (1).

![Img](../media/25.png)
This is a command block used to set "**high**" or "**low**" to the specified pin. "**high**" means high level(1)，LED will light up, "**low**" means low level(0)，LED will light off.

![Img](../media/26.png)
It is a delay module and 1 can be altered.

![Img](../media/27.png)
It is a forever module, it will execute one code forever.

#### Step 3：Write the Program
① Drag the instruction block ![Img](../media/16.png)in the **Events** module to the script area.
![Img](../media/17.png)

② Drag the instruction block ![Img](../media/28.png)in the **Serial** module to the script area and take the baud rate 9600 as an example.

![Img](../media/29.png)

③ Drag the instruction block![Img](../media/30.png)
in the **Pins** module to the script area. Since the digital capacitive touch sensor is connected to D6 of No.2 interface on the mainboard, then change the number 0 to 6.
![Img](../media/31.png)

④ Drag the instruction block  ![Img](../media/27.png)in the **Control** module to the script area.
![Img](../media/32.png)

⑤Drag the instruction block![Img](../media/33.png) in the **Serial** module to the script area.
![Img](../media/34.png)

⑥ Drag the instruction block ![Img](../media/23.png)in the **Pins** module to the script area and put it into the block ![Img](../media/33.png), then change the number 0 to 6.
![Img](../media/35.png)

⑦ Drag the instruction block ![Img](../media/26.png)in the **Control** module to the script area and change the number 1 to 0.2.
![Img](../media/36.png)

⑧ Complete Program
![Img](../media/37.png)

#### Step 4：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, then  click ![Img](../media/38.png) in the serial monitor area to set the baud rate to 9600. Then the serial monitor will print the value read by the digital capacitive touch sensor. 

When your finger touches the plum-shaped metal sensing area on the sensor, it will output a high level (1); when released, it will output a low level (0).
![Img](../media/3777.png)

## 6. Digital Capacitive Touch Sensor Controls Mixer to Rotate
![Img](../media/2-4.png)

## 7. Programming Steps

#### Step1: Description of Building Blocks
![Img](../media/3888.png)
It is a conditional statement code executing **if-then-else ** function: If the logical judgment statement in ![Img](../media/39.png) is satisfied, the code statement below **then** is executed, otherwise, the code below **else** is executed.



#### Step2：Flow Chart
Set the 360° servo angle to 90°. When you press (or touch) the metal sensing area on the sensor with your finger, the servo and the mixer will rotate, otherwise they won't rotate.
![Img](../media/40.png)

#### Step3：Add **Servo **Instruction Block 
![Img](../media/42.png)

#### Step4：Write the Program


① Find building blocks
（1）![Img](../media/43.png)
<br>   
（2）![Img](../media/44.png)
<br>   
（3）![Img](../media/45.png)
<br>
（4）![Img](../media/46.png)
<br>
（5）![Img](../media/47.png)
<br>
（6）![Img](../media/48.png)
<br>

② Complete Program
![Img](../media/49.png)

#### Step5：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up. When you press (or touch) the metal sensing area on the sensor with your finger, the servo and the mixer will rotate, otherwise they won't rotate.

![2-9](media/2-9.png)

## 10. Expansion Project
![Img](../media/2-7.png)

The sample code is below：
![Img](../media/50.png)

