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

