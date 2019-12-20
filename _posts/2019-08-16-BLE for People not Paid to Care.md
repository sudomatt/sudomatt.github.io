---
layout: post
title:  "Bluetooth for People Not Paid to Care"
date:   2019-08-16 12:00:00 -0500
categories: Bluetooth
---

Bluetooth Low Energy (BLE) is a low power wireless protocol designed as a cable alternative.  It was designed
for ease of use and implementation of developers, so as a result can be a bit of a mess.

Bare Minimum:

<b>GAP:  Generic Access Profile</b> - How BLE devices discover each other, navigate a way to set up a secure communication channel

  GAP Peripheral:  Advertises, accepts connections.  (i.e. a fitbit)

  GAP Central: Scans for advertising packets, initiates connections (i.e. a smartphone)

There's also GAP Broadcasters, which advertise but do not accept connections (i.e. a beacon), as well
as GAP Observers, which scan for advertising packets, but do not initiate connections (i.e. app looking for beacons)


<b>GATT:  Generic Attribute Table</b> - The framework for describing capabilities and descriptors of a BLE device.  Made up of Services, Characteristics, and descriptors

Services:  Top level, describes what the BLE device does; their primary feature (i.e. heart rate monitor)  Contain one or more characteristics.  BLE SIG has a long list of predefined services to use in design.

Characteristics:  Mid level, individual items of state data.  Have a name, a value, and support one or more operations (read/write)

Descriptors:  Low level, text description for characteristics regarding content and interaction
