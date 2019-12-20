---
layout: post
title:  "Bluetooth Security"
date:   2019-09-02 12:00:00 -0500
categories: Bluetooth
---
BLE Security:
  aster
  Slave
  GAP	  Central	Peripheral
  GATT	Client	Server
	      Initiator	Responder
	      Opens up	Advertiser


Bluetooth Low Energy Security can be a confusing, garbled mess even for the most astute of wireless developers.  As the saying goes, the “S” in “IOT” is for Security. In addition, none of the BLE security features are mandatory, meaning you could encounter any combination of the following features in the wild.  

In order to start a connection between two BLE devices, they must undergo a process called Pairing.  This involves sharing things like keys in order to allow security capabilities such as encryption to be used.  Paired devices can store this information for further use, making them bonded.
This process begins with a Pairing Feature Exchange:
		Initiator:  Sends SMP Pairing Request PDU to Responder
		Responder: Replies with SMP Pairing Response PDU
	This Tells each device:
		-LE Legacy or LE Secure Connections?
		-Device Authentication during pairing?  	what kind?
		-Which key types should be distributed and generated?
		-What key length should the LTK be?





The request and response PDU:
Name	Size	Function
IO Capability		What can the device do in terms of input/output.  Keyboard only, display only, button only, some combination, none
Bonding Flags		Whether or not the device wants to store the keys for later use
SC Flag	1 bit	Supports Secure Connections Pairing
MITM Flag	1 bit	Requests Authentication as MITM protection
OOB Data Flag		Sends data over a mechanism other than BLE
Maximum Encryption Key Size		7-16 octets (56 to 128 bits)  Picks the smaller of the two devices capabilities (must have same size)
Initiator Key Distribution		LTK, CSRK, and/or IRK
Responder Key Distribution 		LTK, CSRK, and/or IRK

If secure connections can be used, it must be


<b><u>The Big List of BLE Acronyms:</u></b>

ATT – Attribute Protocol

BLE – Bluetooth Low Energy

CRC – Cyclic Redundancy Check

(k)CSRK – Connection Signature Resolving Key – used in signing data sent over unencrypted link 	

DHKey – Diffie Hellman Key

GAP – Generic Access Profile

GATT – Generic Attribute Profile

HMAC – MAC function based upon a hash function

(k)IRK – Identity Resolving Key – used in Bluetooth Privacy feature

(k)LTK – Long Term Key – Used in link encryption

MAC – Message Authentication Codes (Same as MIC)

MIC – Message Integrity Codes (Same as MAC)

MITM – Man in the Middle

NIST – National Institute of Standards and Technology

OOB – Out of Band – Used to exchange keys over non-BLE protocol

PDU – Protocol Data Unit – Single nit of information transmitted

SC – Secure Connections

SMP – Security Manager Protocol

(k)TK – Temporary key – Used in Legacy LE Pairing
