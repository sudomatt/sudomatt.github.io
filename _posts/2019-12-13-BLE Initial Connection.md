---
layout: post
title:  "Bluetooth Connections"
date:   2019-12-13 12:00:00 -0500
categories: Bluetooth
---

Bluetooth Low Energy (BLE) devices can securely connect to each other in one of three different ways:

PIN
Numeric Comparison
Out of Band (OOB) Pairing

<b>GAP:  Generic Access Profile</b> - How BLE devices discover each other, navigate a way to set up a secure communication channel

GAP Peripheral:  Advertises, accepts connections.  (i.e. a fitbit)

GAP Central: Scans for advertising packets, initiates connections (i.e. a smartphone)

GAP Broadcaster:  Advertises, does not accept connections (i.e. a beacon)

GAP Observer:  Scans for advertising packets, does not initiate connections (i.e. app looking for beacons)


<b>GATT:  Generic Attribute Table</b> - The framework for describing capabilities and descriptors of a BLE device.  Made up of Services, Characteristics, and descriptors

Services:  Top level, describes what the BLE device does; their primary feature (i.e. heart rate monitor)  Contain one or more characteristics.  BLE SIG has a long list of predefined services to use in design.

Characteristics:  Mid level, individual items of state data.  Have a name, a value, and support one or more operations (read/write)

Descriptors:  Low level, text description for characteristics regarding content and interaction
