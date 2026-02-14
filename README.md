PWM-Generator
Repository navigation
Code
Pull requests
Actions
This repository focuses on how to design a PWM Generator with variable Duty cycle

License
 MIT license
 0 stars
 2 forks
 0 watching
 1 Branch
 0 Tags
 Activity
Public repository · Forked from GSBhatta/PWM-Generator
pulipatisravani284-prog/PWM-Generator
This branch is up to date with GSBhatta/PWM-Generator:main.
Name	
GSBhatta
GSBhatta
3 years ago
LICENSE
3 years ago
README.md
3 years ago
Variable_PWM.v
3 years ago
Variable_PWM_tb.v
3 years ago
Repository files navigation
README
License
PWM Generator
What is PWM?
Pulse Width Modulation is a technique of controlling the average voltage. It is a stream of voltage pulses that reduces the electric power supplied by the electrical signal. It is a square wave signal, which is represented as:

image

This implies that PWM has only 2 outputs i.e.,

HIGH (LOGIC 1).
LOW (LOGIC 0). The duty cycle of the rectangular pulse is shown as follows:
image

where,

to is the time period for which the signal is LOGIC 1.
tc is the total time period of the signal.
For example, let us assume that our output signal is having a timeperiod of 20ns,

0% Duty cycle implies that the signal is HIGH for 0ns and LOW for 20ns.
25% Duty cycle implies that the signal is HIGH for 5ns and LOW for 15ns.
50% Duty cycle implies that the signal is HIGH for 10ns and LOW for 10ns.
75% Duty cycle implies that the signal is HIGH for 15ns and LOW for 5ns.
100% Duty cycle implies that the signal is HIGH for 20ns and LOW for 0ns.
image

Applications
Voltage regulation
Audio signal generation
Pump Hydraulics
Servo motor
CPU fan speed control
Encoding in Telecommunication
Motor speed controller
PWM Generator using Verilog-HDL
PWM generator was designed in Verilog-HDL using Xilinx Vivado 2022.2. There are few changes that has to be done in the Simulation time.

How to create a project in Xilinx Vivado 2022.2?
Step 1: Open Vivado 2022.2 on your system.
Untitled

Step 2: Create a new project as follows: create project --> Next --> Project name: ____ --> Next --> check RTL Project --> Next --> click on Create File --> a dialog bx pops up prompting you to give the File name: ______ and click on Next --> Next.

Step 3: Select an FPGA board Category: General Purpose --> Family: Atrix-7 --> Package: csg324 --> Speed: -1 --> select xc7a100tcsg324-1 --> Next --> Finish.

Step 4: I/O Constraints (optional) can proceed even without giving the constraints just by clicking on Finish/Next as it can be defined in the module later.

How to change Simulation time?
As soon as you open your project click on settings icon provided in the tool bar as shown below.

Untitled1

This will pop up another Dialog box as shown below.

Untitled3

Follow the numbers (from 1 - 4)
The simulation time will be set to 1000ns by default. It can be changed according to our requirements.

Now copy paste the codes Variable_PWM.v and Variable_PWM_tb.v file one below the other and click on Run Simulation --> Run Behavioral Simulation to see the output waveform.
Schematic
Untitled5

Waveform
Untitled4

Useful links
https://www.javatpoint.com/arduino-pwm
https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/vivado-design-tools/2022-2.html
https://www.chipverify.com/verilog/verilog-tutorial

