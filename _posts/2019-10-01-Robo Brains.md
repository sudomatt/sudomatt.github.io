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

Solution:  Open Source symbyotic board + goodwill toys!

Electronics design can be a daunting task even for professionals.  Every kid who watched
battlebots or robot wars as a kid will feel the pull to build their own mechanical monster
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

<b>H-Bridge</b>
<img align="center" src="/images/hbridge.jpg">
<i>fig 1</i>

An H bridge controls the direction a motor is turning.  If a positive voltage is applied to the + end of the motor, and ground
is connected to the - end, the motor will turn forward.  If those voltages are reversed, the motor will turn backwards.

Transistors (labeled NPN and PNP) are effectively electronically controlled light switches.  When Q1 and Q4 are connected, and Q2 and Q3 are disconnected, voltage flows from the + end of the motor to the - end running it in forward mode.  When Q2 and Q3 are connected, and Q1 and Q4 are disconnected, this runs the motor in reverse mode because voltage is flowing from the - end of the motor to the + end.  This means to control a motor we just need to 4 pins to control Q1 Q2 Q3 and Q4.


h-bridge



<u>BOM</u>

ESP32

H-Bridge
