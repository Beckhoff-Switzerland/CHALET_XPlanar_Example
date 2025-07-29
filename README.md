
# CHALET Framework for Beckhoff XPlanar


---

The **CHALET Framework** is a powerful and intuitive software library designed to simplify the control and management of **Beckhoff XPlanar** systems. It abstracts the complexities of direct mover control, allowing developers and engineers to focus entirely on defining and optimizing their material flow processes.

![image](https://github.com/user-attachments/assets/cdabc5ef-70da-4cc3-823f-08bfe2f041ff)
---

## Why CHALET?

* **Simplified Process Definition:** Define your XPlanar workflow using intuitive "stations" rather than complex individual mover commands.
* **Enhanced Efficiency:** Optimize your processes with intelligent mover distribution and flexible motion control.
* **Robust Development:** Utilize a powerful simulation mode for early testing and bottleneck detection.
* **Reduced Development Time:** Focus on your application logic, not the intricacies of low-level XPlanar control.

---

## Key Features

### 1. Intuitive Station-Based Control

The core of the CHALET Framework revolves around the concept of **Stations**. You simply define key points on your XPlanar track where products need to be processed or transferred. Each station offers configurable parameters for precise control:

* **Queue Size:** Specify how many movers a station can hold before it becomes blocked, enabling buffer management.
* **Ready for Acceptance:** A flag to signal whether the station is prepared to receive new movers, allowing for external process synchronization.
* **Station Name:** A unique identifier for clear identification and monitoring within your PLC code.
* **Group Affiliation:** Group multiple stations performing identical processing steps, enhancing flexibility and throughput by distributing workload.

The framework intelligently manages mover routing and movement between these defined stations.

### 2. Powerful Simulation Mode

A standout feature of the CHALET Framework is its **easily configurable simulation mode**. This allows you to virtualize and test your entire process flow before deploying to the physical hardware, offering immense benefits:

* **Early Bottleneck Detection:** Proactively identify and resolve potential bottlenecks or inefficiencies in your process design.
* **Collision Detection:** Reliably detect and prevent potential collisions between movers or with stationary elements within the simulated environment, ensuring a safe and optimized layout.
* **Process Optimization:** Experiment with various station layouts, queue sizes, and processing sequences to find the optimal configuration for maximum efficiency and throughput.

### 3. Flexible Motion Dynamics & Track Configuration

The CHALET Framework provides comprehensive control over mover behavior:

* **Adjustable Dynamics:** Precisely tune the **motion dynamics** (e.g., speed and acceleration) on different segments of the track. This allows for rapid transport in certain areas and highly precise, gentle positioning at critical processing points.
* **Online/Offline Configuration:** Configure your XPlanar track and its parameters flexibly. You can do this **online via the PLC** for dynamic adjustments during live operation, or **offline within the track object** for a static, reproducible, and version-controlled setup.

### 4. Dynamic Mover Routing & Optimization

Once a processing step is completed, any mover can be **commanded to any desired station** on the XPlanar layout. The CHALET Framework intelligently handles the pathfinding:

* **Optimal Path Selection:** The mover automatically calculates and navigates the **optimal path** using the **A\* algorithm**, ensuring efficient and collision-free movement across the entire track.
* **Detailed Network Control with Zones:** For even more granular control over the network, you can define **zones**. These zones can be configured to be entered only by movers with a **selected destination station**, allowing you to implement sophisticated routing strategies, manage traffic flow, and prevent undesirable pathing in complex layouts.


---
## Requirements

### Build 3.1.4026

Worklaods:
- TwinCAT.Standard.XAE
- TF5890.XPlanar.XAE
- TF5400.AdvancedMotionPack.XAE
  
Packages to use Usermode-Runtime:
- TwinCAT.XARUM.NCPTP
- TwinCAT.XARUM.AdvancedMotion


### Build 3.1.4024
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
