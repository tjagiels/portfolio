# Tomasz Jagielski - portfolio
This repository contains some of my projects. Feel free to get introduced to it.

<br />

 ---
<br />

## 1. Inertial self-balancing cube and BLDC FOC controller
One dimensional flywheel balancing cube (2016). Purpose: for fun:) Inspired with Cubli 

[![Cubli 3D balancing cube](https://img.youtube.com/vi/n_6p-1J551Y/0.jpg)](https://www.youtube.com/watch?v=n_6p-1J551Y "Cubli 3D balancing cube")

Challenges:
<ol>
<li>Implement true Field Oriented Controller</li>
<li>Design and implement balancing algorithms</li>
</ol>

### Balancing tuning and operation
[![Balancing tuning and operation](https://img.youtube.com/vi/Khjhep73fQU/0.jpg)](https://youtu.be/Khjhep73fQU "Balancing tuning and operation")

### BLDC Field Oriented Control operation
[![BLDC Field Oriented Control operation](https://img.youtube.com/vi/U1Hw3HjGYGA/0.jpg)](https://youtu.be/U1Hw3HjGYGA "BLDC Field Oriented Control operation")

### BLDC control software overview
[![BLDC control software overview](https://img.youtube.com/vi/FGd0gnViqYI/0.jpg)](https://youtu.be/FGd0gnViqYI  "BLDC control software overview")


Hardware:
Adapted SToRM32-BGC camera gimbal controller. Gimbal motor drivers ware used as gate drivers for high amp driver. Controller board provided all necessary peripheral IOs connected to sockets. 

High amp driver was designed and created with home methods. Consist of 3 N-MOS / P-MOS half-bridges and hall effect current measurement circuit.
BLDC motor is a cheap RC plane motor.
Orientation sensor is a 3D gyroscope and accelerometer MPU6050.

Software:
   STM32: C++/C with GCC. MCU has 3 general task: Field oriented control of BLDC motor, communication and balancing algorithm. 
   PC: Qt 4.8. Is an interface providing debug information and sending controller configuration. 
 
<br />

 ---
<br />

  ## 2. Calliope - the drawing robot
 General purpose parallel kinematics handling robot (2013, 3 persons team). Adapted for drawing to take part in SketchBot Painting category during RoboGames Competition in San Francisco. 

[![BLDC control software overview](https://img.youtube.com/vi/pqL4TcPgwv8/0.jpg)](https://youtu.be/pqL4TcPgwv8  "Calliope - drawing robot")

Mechanics:
Typical delta robot design - based on 2 aluminium plates supported with structural profiles creating a cage within which operates an effector. Each profile has a linear guide bolted to it. Motion of guide blocks, through ball joints, aluminium rod and another ball joint, is transfer to an effector. Guide block are driven with timing belt, driven with stepper motor. 

All components were designed in Autodesk Inventor and ordered to perform.

Electronics (team mate's part):
Controlled based on STM32F4 Discovery board. Coded in C.

Matlab(team mate's part):
Implements image processing and inverse kinematics calculation.
