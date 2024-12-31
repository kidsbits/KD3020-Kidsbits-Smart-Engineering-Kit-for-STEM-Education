# Project 01: Seesaw

![Img](./media/1-1.jpg)


## 1. Overview

It is well known that seesaw is sought-after among children. Usually, two children sit on both ends of the seesaw and step on the ground in turn to make one end rise and the other fall. However, in this project, we will work to make a seesaw that can rise and fall automatically.



## 2. Components

|![Img](../media/kidsuno.png)|![Img](../media/360.png)|![Img](../media/USB.png)|![Img](../media/Lego11.png)|
| :--: | :--: | :--: | :--: | 
|Kidsuno Mainboard×1|360°Servo×1|USB Cable×1| Lego Series×1 |

![Img](../media/1-2.png)

## 3. Make A Seesaw

![Img](../media/1-3.png)

## 4. Installation 

**Preparation：**

![Img](./media/img-20241230140343.png)

**Step1:**

![Img](./media/img-20241230140506.png)

**Step2:**

![Img](./media/img-20241230140619.png)

**Step3:**

![Img](./media/img-20241230140645.png)

**Step4:**

![Img](./media/img-20241230140710.png)

**Step5:**

![Img](./media/img-20241230140752.png)

**Step6:**

![Img](./media/img-20241230140823.png)

**Step7:**

![Img](./media/img-20241230140856.png)

**Step8:**

![Img](./media/img-20241230140921.png)

**Step9:**

![Img](./media/img-20241230141245.png)

**Step10:**

![Img](./media/img-20241230141314.png)

**Step11:**

![Img](./media/img-20241230141358.png)

**Step12:**

![Img](./media/img-20241230141439.png)

**Step13:**

![Img](./media/img-20241230141506.png)

**Step14:**

![Img](./media/img-20241230141537.png)

**Step15:**

![Img](./media/img-20241230141607.png)

**Step16:**

![Img](./media/img-20241230141639.png)

**Complete:**

![Img](./media/img-20241230141702.png)


## 5. Programming Steps

#### Step1：Wiring Diagram

Connect the kidsuno mainboard and computer via a USB cable, and connect the 360° servo to the G, V and D13 interface of the mainboard. The brown wire is connected to G, the red wire is connected to V and the orange wire is connected to D13.

![Img](../media/1-DD.png)

#### Step2：Add Servo

![Img](../media/11.png)

![Img](../media/12.png)


Diagram of the **Extension** Instruction Block

![Img](../media/13.png)

Add **Servo** Instruction Block 

![Img](../media/14.png)

#### Step3: Description of Building Blocks

![Img](../media/15.png)

Set the angle value and delay to the specified pin. When the angle value is 90, the servo will stop rotating; if it is 0 ~ 90, the servo will rotate clockwise, the smaller the value, the faster the rotation speed;  if it is 90 ~ 180, the servo will rotate counterclockwise, the larger the value, the faster the rotation speed.

**Rotation of 180° Servo and 360° Servo ：**

![Img](../media/1-4.png)

#### Step4：Write the Program

① Drag the instruction block ![Img](../media/16.png)in the **Events** module to the script area.

![Img](../media/17.png)

② Drag the instruction block![Img](../media/15.png)in the **Servo** module to the script area. Since the servo is connected to the G, V and D13 interface of the mainboard(<span style="color: rgb(255, 76, 65);">The brown wire is connected to G, the red wire is connected to V and the orange wire is connected to D13</span>), then change the number 3 to 13 and angle to any value within the range of 0 ~ 90 or 90 ~ 180. To make the servo rotate slowly, the angle value entered here is 60.

![Img](../media/1-8.png)

③ Complete Program

![Img](../media/1-5.png)

#### Step5：Test Result

Click![Img](../media/19.png)to upload the complete program to the kidsuno mainboard and power up, then the seesaw can rise and fall automatically.

![1-9](./media/1-9.png)

## 6. Expansion Project

![Img](../media/1-6.png)

The sample code is below：

![Img](../media/1-7.png)





