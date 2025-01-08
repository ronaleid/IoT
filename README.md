# Rona's IoT Documentation
This document includes information on Rona's IoT Project that involves Arduino, Atlas Scientific Sensors, and Node-Red. All code in the repositories are labeled accordingly. 


## General Notes

Atlas Scientific sensors and other sensors are used.
Sensors are coded using Arduino/C++.
Node-Red is used to manipulate data.

To use multiple Atlas Scientific Sensors, a Whitebox Labs Tentacle Shield is used. 
[Whitebox Website and Documentation](https://www.whiteboxes.ch/docs/tentacle/t1/#/)

## Notes for Code
**Circuit Channels**
### Current Order
1, 2, 3, 4, 5
"DO", "ORP", "PH", "EC", "CO2"
97, 98, 99, 100, 105

### Sensors To Add to Main Interlink
"FLOW"
104


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
5. Enjoy!
  - Note: When using Node-Red, Arduino software MUST BE CLOSED. Make sure using right COM in Node-Red, this depends on where the wire is plugged in.


## Update Log ♩¨̮(ง ˙˘˙ )ว♩¨̮
### 1/7/25
Added Flow Meter to separate interlink. Manually switched Flow Meter circuit by using shorting between TX and PRB method.
Humidity sensor may be faulty. Green wire is not properly connected to [female connector](https://www.molex.com/en-us/products/part-detail/0022012057).
Cannot see if RGB sensor switches between UART (green light) and I2C (blue light). Resin/water protection is black and not clear like CO2 sensor. 
Tried to use RGB sensor with interlink, but was not working. It worked directly connected to Arduino and using old RGB code from 2020, but it only printed LUX number.

### 1/2/25
CO2 sensor was added to interlink. Code is not yet uploaded to Github.
ORP sensor sensor is not calibrating properly 😞
- I let it sit in the calibration solution for almost an hour and readings were consistently printing out with values around 950-990. The sensor is supposed to be consistently reading 240.1 when stabilized.

### 12/27/24
All sensors (DO, EC, and pH) were transferred to the AtlasScientific i1InterLink and switched from UART mode to I2C mode.
The interlink only works in **i2c** mode

I2C vs UART
- I2C is best for connecting multiple devices over a shared bus and is ideal for short-range, low-speed communication in embedded systems.
- UART is simpler and often used for one-to-one communication, such as debugging or linking microcontrollers to external modules.

Since switching to i2c mode, numbers no long switch between sensors when readings are recorded and printed. 

Oxidation Reduction Potential (ORP) sensor was added to interlink. Code is not yet uploaded to GitHub.  
