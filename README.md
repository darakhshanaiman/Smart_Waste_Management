Smart Waste Collection Management System (GIKI Campus)

**Project Overview**

This project is an Agent-Based Simulation (ABS) developed for the Ghulam Ishaq Khan Institute (GIKI) campus. It models an intelligent, IoT-enabled waste management system designed to replace traditional static collection routes.

The simulation demonstrates how "Smart Bins" equipped with fill-level sensors can communicate with a central fleet of autonomous garbage trucks to optimize routing, reduce fuel consumption, and prevent bin overflows.

Course: CE413 - Computer Communication and Networking
Institution: GIKI (Ghulam Ishaq Khan Institute of Engineering Sciences and Technology)

**Key Features**
1) GIS Integration: Built on a real-world OpenStreetMap layout of the GIKI Topi campus, featuring custom-defined routing for realistic truck movement.

2) IoT Smart Bins: Agents that stochastically generate waste and wirelessly trigger "pickup requests" only when a threshold (80%) is reached.

3) Autonomous Fleet: Garbage trucks that remain idle at the central depot (Auditorium) until dispatched, servicing specific requests and returning to base to conserve energy.

4) Real-Time Dashboard: A live analytics panel tracking:

Total Distance Traveled (Efficiency KPI)

CO2 Emissions (Sustainability KPI)

Live Waste Levels (Bar Chart)

 **Technologies Used**

Simulation Platform: AnyLogic (PLE Edition 8.9+)

Logic: Java (Statecharts, Events, Agent Communication)

Mapping: OpenStreetMap (GIS)

 **Installation & Usage**

Prerequisites

AnyLogic Software: Download and install the Personal Learning Edition (PLE) for free.

Internet Connection: Required for the GIS map to load map tiles during the first run.

How to Run

Clone this repository or download the source files.

git clone [https://github.com/yourusername/Smart-Waste-Management-GIKI.git](https://github.com/yourusername/Smart-Waste-Management-GIKI.git)


Open AnyLogic and select File > Open.

Navigate to the folder and select Smart_Waste_Management.alp.

In the Projects sidebar, click on Simulation: Main.

Click the Green Play button ▶ in the toolbar.

When the simulation window opens, click Run.

**Logic & Architecture**

1. The "Smart Bin" Agent

Waste Generation: Simulates student activity by increasing fill level by ~10% every simulation hour.

IoT Trigger: When fillLevel >= 80%, the bin enters a "Request State".

Retry Logic: If no trucks are available, the bin enters a "Nagging Loop," re-sending the request every 10 minutes until serviced.

2. The "Garbage Truck" Agent

Statechart Logic:

AtDepot: Idle state, waiting for messages.

DrivingToBin: Movement via GIS routes to the target hostel.

AtBin: Service state where bin fillLevel is reset to 0.

ReturningToDepot: Return logic to the auditorium.

Routing: Uses a custom GIS Route network (Blue Lines) to ensure trucks follow campus roads instead of straight-line paths.


This project is for educational purposes submitted to the Faculty of Computer Science and Engineering at GIKI.

Author: Aiman Darakhshan (2022076)
