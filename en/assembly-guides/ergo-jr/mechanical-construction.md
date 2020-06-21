
# Mechanical Assembly

## General advices and warnings

* **All orientations of all parts are very important**. Observe the pictures very carefully in order to reproduce the exact same assembly with the parts in the same orientation. If you make a mistake, you will realize it because your robot will perform motions different from what you'll ask. In that case do not worry, you will be able to unmount an remount your robot.

* You can pre-assembly all riverts you need before building your robot. Rivets are composed of 2 elements inserted into each other this way:

![OLLO Rivet Assembly](img/assembly/ollo_rivet.png)

* There are two kinds of rivets. The grey ones and the others. Grey rivets are longer to be able to be inserted in the motor axis, at the opposite side of the horn (black revolving circle).

<img src="img/assembly/ollo_rivets_size.jpg" alt="OLLO Rivet size" height="200">

* Use the OLLO Tool for putting and removing rivets easily.

<img src="img/assembly/ollo-tool.jpg" alt="OLLO Tool" height="200">


* Do not forget to put wires between motors while building the robot! Each motor, except the last, must have two wires; one connected to the previous motor and the other to the next (there is no importance on the connector choice).


* **Always align the horn with the motor before assembling them!** Otherwise your Poppy Ergo Jr will look all weird.

<img src="img/assembly/align-horn.jpg" alt="Align Horn" height="200">


* Every motor horns (black revolving circle) are **facing the left side of the robot**. It is a convention but it will define the orientation of your motors.

![Horns on left side](img/assembly/horns_on_left.jpg)

## Step-By-Step guide

### Motor configuration (for all steps)

You can configure your motors before, during or after the the mechanical assembly but **it is highly advised to configure each motor one by one in the construction order**:
* configure motor m1
* assemble the base and motor m1
* configure motor m2
* ...

> **Caution** To configure motors, you have to connect them separately one by one to the Raspberry Pi. If you try to configure a new motor wired to a previously configured motor, this will not work.


Please consult the [motor configuration section](motor-configuration.md) for more informations.

### Step 1 - motor 1
First, [configure one XL-320](motor-configuration.md) motor as "m1".

Mount the motor on the 3D printed base.

![step 1](img/assembly/steps/step_1-2.jpg)

To do so, prepare 8 small rivets. put the first part in the second part without putting them in the motor. Then, place the motor in the base, with the horn facing up and near the more open side.
Use the Ollo to grab a rivet between the first and the second part, then put the rivet in one the assembly holes. Once the rivet is in place, lock it by pushing the part 1 of the rivet in part 2.


### Step 2 - motor 2
Configure the second motor, its name is "m2", with the following command in a poppy terminal:
```bash
poppy-configure ergo-jr m2
```

Mount the *long_U* part. Be careful with the orientation of the U, the horn must be oriented in the left.
Mount the motor "m2" on top of the construction.

![step 2](img/assembly/steps/step_3-4.jpg)


### Step 3 - motor 3
Configure a third motor: "m3".

Mount *horn2horn* and *horn2side* parts on motor "m2", and mount "m3" on top of the construction.
![step 3](img/assembly/steps/step_5-6.jpg)


### Step 4 - motor 4

Configure the fourth motor: "m4".

Mount the *short_U* on it.
![step 4](img/assembly/steps/step_7-8.jpg)

Mount motor "m4" and the assembled *short_U* on top of the previous assembly. The nose of the motor should be on the other side of the base.
![step 4 bis](img/assembly/steps/step_9-10.jpg)

### Step 5 - motor 5

Configure the fifth motor: "m5".

Mount *horn2horn* and *horn2side* parts on motor "m4", and mount "m5" on top of the construction.

![step 5](img/assembly/steps/step_11-12-13.jpg)


### Step 6 - the tool of your choice
Configure the sixth motor: "m6".

To finish your Ergo Jr, you need to add a tool at its end. So first choose the tool you want depending on what you want to do.

> **Note** Tools they can be easily and quickly changed, so you can adapt it to the different activities.

#### Lampshade or pen holder
Mount *horn2horn* and *horn2side* parts on motor "m5", and mount "m6" on top of the construction.
![step 6](img/assembly/steps/step_14-16-17.jpg)

You can mount the pen holder or the lampshade on the motor "m6".
![step 6 bis](img/assembly/steps/step_18-19.jpg)

In the same way you mount the lampshade, you can also mount the pen holder.
<img src="img/assembly/steps/pen_holder.jpg" alt="step 6 pen" height="300">



#### Gripper
Mount the [*gripper-fixation*](https://github.com/poppy-project/poppy-ergo-jr/blob/master/hardware/STL/tools/gripper-fixation.stl) between motors "m5" and "m6".

Mount *gripper-fixed_part* and *gripper-rotative_part* on motor "m6".

There is two way to mount the gripper, vertically
![step gripper](img/assembly/steps/grip1.jpg)

Or Horizontally
![step gripper](img/assembly/steps/grip2.jpg)


### Step 7 - electronics
Mount the support_camera part on the base. Fix the Raspberry Pi camera on it and move the camera flex cable between motor "m1" and the base.
![step 7](img/assembly/steps/step_21-22.jpg)


**Camera flex wire**

To fix the flex cable of the camera on the Raspberry Pi:
* open the camera connector by pulling on the tab to the top
* make sure that connectors on the flex cable are facing away of the Ethernet port
* push the flex on the port, and push the plastic tab down to close it
![step 7](img/assembly/steps/camera.jpg)

**Motors wires:**

If it is not already done, you can plug every motors wires. Every motor has two connectors but there is no input or output: you just have to create a chain of motors. The first motor is linked to the pixl and the second motor; the last motor is linked only to the previous one, and every other motors are linked to the one above and ahead.

> **Info** Connectors of the motor "m1" (in the base) are a bit hard to link, you can use the OLLO tool to help yourself.


![step 7 bis](img/assembly/steps/step_24.jpg)

### Step 8 - fix you Ergo Jr to wood disk support
Mount your Ergo Jr to the wood *disk-support*.

Mount the Raspberry Pi to the disk support, and use 4 x M2.5x6mm screw to fix it.
<!-- TODO: picture of disk fixation -->


### Step 9 - test your Robot !
Congratulation, you achieve the robot assembly! Now, it is almost done, it is time to test it!

Go to your robot home page [http://poppy.local](http://poppy.local).

Click on *Reboot the robot* button to be sure that the robot software was started with all motors wired in.
<img src="img/IHM/home_page_reboot.png" alt="test installation" height="250">


You can go to the monitor, click on *Monitor and Control* button.
<img src="img/IHM/home_page_monitor.png" alt="test installation" height="250">


If the robot software is correctly started, you should see the green connection logo, otherwise it will be red.
<img src="img/IHM/monitor_full.png" alt="test installation">

You can start a pre-defined behavior by clicking on the play logo.

**If the connection logo is red**, you can see what is wrong by looking on messages in *What append?* page.
<img src="img/IHM/home_page_logs.png" alt="test installation" height="250">

Most of the time, it's because a wire is unplugged or because you forgot to configure a motor.


### Done

![image](img/assembly/ergo-tool-2.jpg)

Grab your [favorite drink](https://www.flickr.com/photos/poppy-project/16488256337/) and relax.
