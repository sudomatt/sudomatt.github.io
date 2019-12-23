---
layout: post
title:  "Robotic Brains"
date:   2019-10-01 12:00:00 -0500
categories: Robots
---
<img align="left" src="/images/mrburns.jpg">

Dammit Smithers this isn't Rocket Science it's Brain Surgery!

Robots are cool.

Killer robots are cooler.

Fighting bar robots built by underserved groups are coolest.  


Problem:  The literal cost of admission is prohibitively highlight

Solution:  Open Source symbiotic board + goodwill toys!

Electronics design can be a daunting task even for professionals.  Every kid who watched
BattleBots or robot wars as a kid will feel the pull to build their own mechanical monster
capable of destroying everything in its path.  They approach with excitement and curiosity and the passion
only a child possesses.  Dipping a toe in the water can lead to being intimidated at a library worth
of engineering textbooks that seem necessary to even get 'hello world' and 'blink' working.  The solution,
much like in the professional engineering world, is to take baby steps.  Iteratively moving forward from the
very basics to the more advanced is the best way to learn.

The leechbot is a simple, low-cost BLE based motor controller meant to be integrated
with a 9-12V motor based childrens toys. It was designed to lower the barrier to entry into
the world of robotics.  It consists of three basic subsystems :


<b>Microcontroller</b>

A Microcontroller is the brains of the operation.  It effectively is a means to control electronic switches called pins.  These pins can be set in either High (1), or Low (0) based on commands received.  For example, with the right command, the pin controlling the motor will switch from low to high and the motor will begin running.

When the pin controlling the motor is held at high, the motor will run full speed.  When the motor pin is held at low, it will stop.  What if we want something inbetween full speed and immobile?  Motor speed is controlled with something called Pulse Width Modulation (PWM).  This is effectively flipping the pin from high to low very quickly.  By going on off on off on off, with an equal time with the pin held in each level, the motor will run at about half speed.  By contolling the ratio of high to low, we can get very fine grained control of speed.

<b>Radio</b>

The commands to turn the motor pins off and on are controlled via a COM port, sent over electrical signal.  A radio (bluetooth low energy in this case), is a wireless means of sending those commands.  How Bluetooth Low Energy Works at a lower level is covered  <a href="https://mattguenette.com/bluetooth/2019/08/16/BLE-for-People-not-Paid-to-Care.html">here</a>


<b>H-Bridge</b>
<img align="center" src="/images/hbridge.jpg">
<i>fig 1</i>

An H bridge controls the direction a motor is turning.  If a positive voltage is applied to the + end of the motor, and ground
is connected to the - end, the motor will turn forward.  If those voltages are reversed, the motor will turn backwards.

Transistors (labeled NPN and PNP) are effectively electronically controlled light switches.  When Q1 and Q4 are connected, and Q2 and Q3 are disconnected, voltage flows from the + end of the motor to the - end running it in forward mode.  When Q2 and Q3 are connected, and Q1 and Q4 are disconnected, this runs the motor in reverse mode because voltage is flowing from the - end of the motor to the + end.  This means to control a motor we just need to 4 pins to control Q1 Q2 Q3 and Q4.

The leechbot board comes preloaded with an Arduino Bootloader, preprogrammed, and ready for controlling the weird bot of your dreams slash nightmares.  For $40, you too can hook up to a furby and have your own little demon running around in $20 minutes.

<b><u>Installation</u></b>
1.  Plug the provided lithium ion battery into the board at the terminal labled BAT.

2.  Turn on the bluefruit app and look for the device labeled leechbot followed by some number.  Click connect.

3.  Verify the device connects and the LEDs on the board turn on.  Disconnect the battery.

4.  Find the two wires connected to the motor of your RC car or other device.  There should be two wires, 1 red for VCC, and 1 black for GND.

5.  Snip those two wires as far from the motors as possible.  Strip the last quarter inch of those wires.

6.  Attach those wires through the holes in the screw terminals labeled MOTOR-L and MOTOR-R.  Screw down.

7.  Plug the battery back in, and connect to the leechbot device.  Select joypad for control.  You're good to go!

<u>BOM</u>

ESP32

H-Bridge

PCB

Lithium Ion battery
