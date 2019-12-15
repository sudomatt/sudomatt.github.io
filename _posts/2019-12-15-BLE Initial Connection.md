---
layout: post
title:  "Bluetooth Connections"
date:   2019-12-15 12:00:00 -0500
categories: Bluetooth
---

Bluetooth Low Energy (BLE) devices can securely connect to each other in one of three different ways:

PIN
Numeric Comparison
Out of Band (OOB) Pairing

Generic Access Protocol (GAP) - How BLE devices discover each other, navigate a way to set up a secure communication
channel

GAP Peripheral:  Advertises, accepts connections.  (i.e. a fitbit)
GAP Central: Scans for advertising packets, initiates connections (i.e. a smartphone)

GAP Broadcaster:  Advertises, does not accept connections (i.e. a beacon)
GAP Observer:  Scans for advertising packets, does not initiate connections (i.e. app looking for beacons)
