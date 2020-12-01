# CAN

### Introduction

CAN is an Serial communication technology used for data transmission between different electronic control units(ECU). It is an Event driven communication. It was developed by BOSCH as a multi-master message broadcast system. 


### ISO Specification
| ISO Spec | Name | Speed|
| ----- | ----- | -----|
| `ISO 11898 - 2` | CAN High speed | Up to 1Mbps |
| `ISO 11898 - 3` | CAN Low speed | Up to 125Kbps |

### Features of CAN Protocol
+ Simple and Low cost
+ Built-in Error detection
+ Message based protocol
+ Multi-master communication
+ Error detection and fault confinement feature
+ Maximum network extension of about 40 meters
+ Maximum number of CAN Nodes as 32

### Different types of messages on CAN bus
+ Data Frame
+ Remote Frame
+ Error Frame
+ Overload Frame

### Differential Signaling

CAN Physical signal transmission transmits voltage of different levels(Differential signaling). This effectively eliminates the interference of induced voltage from motor, ignition system and switch contacts.The transmission medium consists of two lines CAN High Line (CAN_H) and CAN Low Line (CAN_L). Pratically twisted pairs are used for signal transmission. 

![CAN Network](https://github.com/AasaiAlangaram/Automotive-Embedded-Questions/blob/main/1.Communication_Protocol/Images/can_physical%20.png)\
Source: *Vector E-Learning*

Differential signaling deploys two conductors in order to transmit one information signal. one will carry voltage signal and the other carries the inverted signal. The receiver
decodes information by finding the potential difference between inverted and non-inverted signal.

### Advantages of Differential Signaling
+ No Return Current
+ Resist Incoming EMI 
+ Outgoing EMI Reduction
+ Lower Voltage operation
+ High or Low state and Precise Timing

### Why Bus Termination is needed?

Termination resistors prevents reflections in a high-speed CAN network. Usually it is 120 Ohm.

### Bus Signal Level

CAN Bus level typically ranges between 1.5v (CAN_L during dominant bit) and 3.3v (CAN_H during recessive bit). However, the actual signal status, recessive or dominant is based on voltage difference Vdiff between CAN_H and CAN_L. 
`Vdiff = Vcan_h - Vcam_l`. ISO 11898-2 assigns logical “1” to a typical differential voltage of 0 Volt. The logical “0” is assigned with a typical differential voltage of 2 Volt. High speed CAN Transceivers interpret a differential voltage of more than 0.9v as dominant level within  common mode operation between 12v to -12v. Below 0.5v is interpreted as recessive level.

The dominant bus level corresponds to logical “0”. The recessive bus level corresponds to logical “1”.





