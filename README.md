# Rona's IoT Documentation
This document includes information on Rona's IoT Project that involves Arduino, Atlas Scientific Sensors, and Node-Red. All code in the repositories are labeled accordingly. 


## General Notes

Atlas Scientific sensors and other sensors are used.
Sensors are coded using Arduino/C++.
Node-Red is used to manipulate data.

To use multiple Atlas Scientific Sensors, a Whitebox Labs Tentacle Shield is used. 
[Whitebox Website and Documentation](https://www.whiteboxes.ch/docs/tentacle/t1/#/)


## Atlas Scientific Sensors and Documentation
[Atlas Scientific Website](https://atlas-scientific.com/)

### Dissolved Oxygen
- [Dissolved Oxygen Kit](https://atlas-scientific.com/kits/dissolved-oxygen-kit/)
- Data Sheets
  - [EZO Circuit](https://files.atlas-scientific.com/DO_EZO_Datasheet.pdf)
     - Contains UART Commands
  - [Probe](https://files.atlas-scientific.com/LG_DO_probe.pdf)
     - How to store them, life expectancies, etc. 

### Electrical Conductivity (Probe K1.0)
- [Conductivity K 1.0 Kit](https://atlas-scientific.com/kits/conductivity-k-1-0-kit/)
- Data Sheets
  - [EZO Circuit](https://files.atlas-scientific.com/EC_EZO_Datasheet.pdf)
     - Contains UART Commands
  - [Probe](https://files.atlas-scientific.com/EC_K_1.0_probe.pdf)
     - How to store them, life expectancies, etc.

### pH
- [pH Kit](https://atlas-scientific.com/kits/ph-kit/)
- Data Sheets
  - [EZO Circuit](https://files.atlas-scientific.com/pH_EZO_Datasheet.pdf)
     - Contains UART Commands
  - [Probe](https://files.atlas-scientific.com/pH_probe.pdf)
     - How to store them, life expectancies, etc..

### Flow meter
- [1/2" Flow Meter Kit](https://atlas-scientific.com/kits/1-2-flow-meter-kit/)
- Data Sheets
  - [EZO Circuit](https://files.atlas-scientific.com/flow_EZO_Datasheet.pdf)
     - Contains UART Commands
  - [Flow Meter](https://files.atlas-scientific.com/1-2_flow_datasheet.pdf)
     - How to store them, life expectancies, etc.
- [Wiring Diagram](https://files.atlas-scientific.com/ezo-flow-wiringdiagram.pdf)
- [Arduino Uno Sample Code](https://files.atlas-scientific.com/Arduino-Uno-flow-sample-code.pdf)


## Node-Red
### Documentation & References
- [Running on Windows](https://nodered.org/docs/getting-started/windows#running-on-windows)
- [Creating your first flow](https://nodered.org/docs/tutorials/first-flow#next-steps)
- [Creating your second flow](https://nodered.org/docs/tutorials/second-flow)
- [Arduino and Node-Red](https://docs.arduino.cc/arduino-cloud/guides/node-red/)
   - How to use Node-Red with Arduino Cloud. Attempted but ran into issues when trying to install Arduino palette on Node-Red.  

### How to use Node-Red
1. Open Windows Powershell
2. Type "node-red"
3. Open Node-Red website: http://localhost:1880/#flow/427bda2db7b524f0
4. Enjoy!
