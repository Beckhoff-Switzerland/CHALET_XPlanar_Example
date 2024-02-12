## About This Repository
This repository is a detailed example application how to use the [CHALET_XPlanar](https://github.com/Beckhoff-Switzerland/CHALET_XPlanar) framework

The following layout has been selected with 3 movers.
Station "Infeed1" on the left-hand side requires several movers to start interacting with the process.
The two stations on the right-hand side "Outfeed1" and "Outfeed2" require one mover. They are redundant. If one of the two stations fails, the movers will automatically move to the other station.
![image](https://github.com/Beckhoff-Switzerland/CHALET_XPlanar_Example/blob/master/Layout.png)

- how the framework can be used to use the movers in the station to perform a simple clamp movement with the external setpoint generator.
- Changing the mover dynamics on different sections of the track
- Easily configurable simulation mode to simulate a process and detect bottlenecks at an early stage
- Configuration of the tracks either online from the PLC or offline in the track object

---
## Requirements
- [TE1000 | TwinCAT 3 Engineering](https://www.beckhoff.com/en-en/products/automation/twincat/texxxx-twincat-3-engineering/te1000.html)
- [TF5890 | TwinCAT 3 XPlanar](https://www.beckhoff.com/en-en/products/automation/twincat/tfxxxx-twincat-3-functions/tf5xxx-motion/tf5890.html)
- [TF5430 | TwinCAT 3 Planar Motion](https://www.beckhoff.com/en-en/products/automation/twincat/tfxxxx-twincat-3-functions/tf5xxx-motion/tf5430.html?)

---
## Quick Start
- 

