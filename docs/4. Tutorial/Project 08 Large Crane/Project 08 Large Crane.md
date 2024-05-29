# Project 08：Large Crane

![8-1](media/8-1.png)

## 1. Overview
Crane is a machine that integrates loading, transportation and unloading, which is widely used in ports, workshops, electric power as well as construction sites. In this project, we will seek to make a large crane.



## 2. Components
|![Img](../media/kidsuno.png)|![Img](../media/Receiver.png)|![Img](../media/Remote.png)| 
| :--: | :--: | :--: |
|Kidsuno Mainboard×1|IR Receiver×1|IR Remote Control×1|
|![Img](../media/360°.png)|![Img](../media/270°.png)|![Img](../media/Connection.png)|
|360°Servo×1|270°Servo×1|Connection Wire×1|
|![Img](../media/USB.png)|![Img](../media/Lego11.png)|![Img](../media/Wire.png)|
|USB Cable×1| Lego Series×1 |Wire×1|
|![Img](../media/8-2.png)||||

## 3. Installation 

Please refer to the following link：https://www.dropbox.com/scl/fo/dtu6zv41pd82c71yb65q8/h?rlkey=kzegu8g8jkjieaeqfjxif6kii&dl=0



## 4. Read the Button Value of IR Remote Control
![Img](../media/8-3.png)

## 5. Programming Steps

#### Step1：Wiring Diagram

Connect the kidsuno mainboard and computer via a USB cable, connect the IR receiver module to the No. 2 interface of the mainboard. Then connect the 270° servo to the G, V and D12 interface, the brown wire is connected to G, the red wire is connected to V and the orange wire is connected to D12, the 360° servo to the G, V and D13 interface of the mainboard(brown wire: G, red wire: V , orange wire: D13).
![Img](../media/8-dd.png)

#### Step2：Add the  IR Receiver 
Tap the "Communication" module in the "Extension" , then select " ** IR Receiver ** " and click ![Img](../media/781.png)to return to the programming interface.

![Img](../media/12.png)



Diagram of the **Extension** Instruction Block

![Img](../media/c10.png)
Add “**IR Receiver **”
![Img](../media/c11.png)

#### Step2: Description of Building Blocks

![Img](../media/c12.png)
This block is used to initiate IR receiver to the specified pin.

![Img](../media/c13.png)
This block is used to receive data from the IR remote control.

![Img](../media/c14.png)
This block is used to read received IR data.

![Img](../media/c15.png)
This block is used to refresh the IR received data and receive the next value.



#### Step3：Write the Program
①  Drag the instruction block ![Img](../media/16.png)in the **Events** module to the script area.

![Img](../media/17.png)



② Drag the instruction block ![Img](../media/28.png)in the **Serial** module to the script area and take the baud rate 9600 as an example.

![Img](../media/29.png)



③ Drag the instruction block![Img](../media/c12.png)in the **IR Remote** module to the script area, since the IR receiver  module is connected to the D6 pin of the No. 2 interface on the mainboard, then change the number 2 to 6.
![Img](../media/c16.png)

④ Drag the instruction block ![Img](../media/27.png)in the **Control** module to the script area.
![Img](../media/c17.png)

⑤ Drag the instruction block  ![Img](../media/662.png)in the **Control** module to the script area.
![Img](../media/c18.png)

⑥ Drag the instruction block![Img](../media/c13.png)in the **IR Remote** module to the script area and place it into![Img](../media/662.png) .
![Img](../media/c19.png)

⑥ Drag the instruction block![Img](../media/33.png) in the **Serial** module to the script area, then change “**warp**” to “**HEX**”.
![Img](../media/c20.png)

⑥Drag the instruction block![Img](../media/c14.png)in the **IR Remote** module to the script area and place it into

![Img](../media/c21.png).
![Img](../media/c22.png)

Drag the instruction block![Img](../media/c15.png)in the **IR Remote** module to the script area.
![Img](../media/c23.png)

⑦ Drag the instruction block ![Img](../media/26.png)in the **Control** module to the script area and change the number 1 to 0.05.
![Img](../media/c24.png)

⑧ Complete Program

![Img](../media/c25.png)

#### Step3：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, pull out the transparent sheet at the bottom of the IR remote control, then pull out the button slot, and then put in the battery(“<span style="color: rgb(255, 76, 65);">**<span style="color: rgb(255, 76, 65); font-size: 24px;">+</span>**</span>”pole is downward )and insert into the slot.

<span style="color: rgb(255, 76, 0);"> Battery type：CR2025（provided by yourself）</span>.
![Img](../media/c26.png)

Then  click ![Img](../media/38.png) in the serial monitor area to set the baud rate to 9600. Point the IR remote control to the IR receiver module, press a button on the IR remote control, and you will see a coded value in the serial monitor. Press the same key multiple times to make sure the value is correct. If you see FFFFFFFF, ignore it.
![Img](../media/c27.png)

![Img](../media/c28.png)

## 6. IR Remote Controls Large Crane
![Img](../media/8-4.png)

## 7. Programming Steps

#### Step1: Flow Chart

|Setting|set 360° servo to 90°，270° servo rotates from 0° to180°（object raises）and OLED displays “![Img](../media/ss.jpg)”pattern|
| :--: | :--: |

| ![Img](../media/left.png) | Value：FF22DD | State |Crane turns left and OLED displays “←” pattern|
| :--: | :--: | :--: | :--: |
|![Img](../media/right.png)| Value：FFC23D | State |Crane turns right and OLED displays “→” pattern|
|![Img](../media/up.png) | Value：FF629D |State |Object raises and OLED displays“↑” pattern|
|![Img](../media/down.png) |Value：FFA8573 |State |Object lowers and OLED displays “↓” pattern|


![Img](../media/81213.png)

#### Step3：Add **Servo **

#### ![Img](../media/42.png)

#### Step4：Write the Program

①  Find building blocks
（1）![Img](../media/43.png)
<br>
（2）![Img](../media/771.png)
<br>
（3）![Img](../media/772.png)
<br>
（4）![Img](../media/c29.png)
<br>
（5）![Img](../media/778.png)
<br>
（6）![Img](../media/c30.png)
<br>
（7）![Img](../media/c31.png)
<br>
（8）![Img](../media/c32.png)
<br>
（8）![Img](../media/c33.png)
<br>

② Complete Program
![Img](../media/C34.png)
![Img](../media/C35.png)

#### Step5：Test Result
Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, the object raises and OLED displays“![Img](../media/SS.jpg)” pattern. Press ![Img](../media/left.png), crane turns left and OLED displays “←” pattern, press ![Img](../media/right.png), crane turns right and OLED displays “→” pattern, press ![Img](../media/up.png), object raises and OLED displays“↑” pattern, press ![Img](../media/down.png), object lowers and OLED displays “↓” pattern.

![8-7](media/8-7.png)











































