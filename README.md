## About This Repository
This repository is a detailed example application how to use the [CHALET_XPlanar](https://github.com/Beckhoff-Switzerland/CHALET_XPlanar) framework

The following layout has been selected with 3 movers.


![image](https://github.com/user-attachments/assets/d8d6c46d-9b93-48af-81e2-3aab3ca74152)


- Easily configurable simulation mode to simulate a process and detect bottlenecks at an early stage
- Changing the mover dynamics on different sections of the track
- Configuration of the tracks either online from the PLC or offline in the track object

---
## Requirements
- [TE1000 | TwinCAT 3 Engineering](https://www.beckhoff.com/en-en/products/automation/twincat/texxxx-twincat-3-engineering/te1000.html)
- [TF5890 | TwinCAT 3 XPlanar](https://www.beckhoff.com/en-en/products/automation/twincat/tfxxxx-twincat-3-functions/tf5xxx-motion/tf5890.html)
- [TF5430 | TwinCAT 3 Planar Motion](https://www.beckhoff.com/en-en/products/automation/twincat/tfxxxx-twincat-3-functions/tf5xxx-motion/tf5430.html?)

---
## Quick Start
When the project is opened in TwinCat for the first time, certain PLC libraries are missing. These are stored in the project and can be installed using the following button.<br>
![image](https://github.com/Beckhoff-Switzerland/CHALET_XPlanar_Example/assets/143804651/2eaaeeea-066d-446c-9530-650616aed40e)<br>

Scan existing CPU cores and select an isolated one for code execution<br>
![image](https://github.com/Beckhoff-Switzerland/CHALET_XPlanar_Example/assets/143804651/2a9a3c79-fef8-45c8-b2de-12903479d375)<br>

Download and login to the PLC
Navigate to the main program. As soon as the system reports back that it has been initialized, bEnable can be toggled. The system starts, the movers begin to hover, line up on the track and drive to the first station.<br>
![image](https://github.com/Beckhoff-Switzerland/CHALET_XPlanar_Example/assets/143804651/1a7b1440-49a5-4328-9ecd-70057a2ea817)<br>

Start XPlanar configurator to get a live view<br>
![TcXaeShell_IaUgHow8R4](https://github.com/Beckhoff-Switzerland/CHALET_XPlanar_Example/assets/143804651/bcc88095-671b-43d6-94a4-7ca62dfb421a)<br>
