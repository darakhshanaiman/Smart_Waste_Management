**1. Project Description**

This project is an Agent-Based Simulation built in AnyLogic to model an intelligent waste management system for the GIKI campus. It replaces the traditional "fixed schedule" garbage collection with a dynamic, demand-driven system using IoT-enabled Smart Bins.

**Core Innovation:**

Smart Bins: Located at Hostels 1, 5, and the Medical Center. They monitor their own fill levels and wirelessly request pickup only when 80% full.

Autonomous Trucks: A fleet of 2 trucks stationed at the Auditorium (Main Depot) that automatically dispatch to service requests and return to base to save fuel.

Real-Time Dashboard: Tracks KPIs including Total Distance Driven (km), CO2 Emissions (kg), and live waste levels.

**2. Features**

GIS Integration: Uses the real OpenStreetMap layout of GIKI Topi.

Dynamic Routing: Trucks follow custom-defined GIS routes along campus roads.

Logic Statecharts: Implements complex agent behavior (Wait -> Drive -> Collect -> Return).

Optimization: Prevents overflow while minimizing unnecessary truck trips.

3. How to Run the Simulation

Prerequisites

AnyLogic PLE (Personal Learning Edition) 8.9 or higher.

Internet connection (to load GIS map tiles).

Steps

Open AnyLogic.

Click File > Open and select Smart_Waste_Management.alp.

In the Projects sidebar, click on Simulation: Main.

Click the Green Play button ▶ in the toolbar.

When the window opens, click Run ▶.

User Controls

Speed Up: Click x10 or Max at the bottom to fast-forward time.

Watch the Map: Zoom in to see bins turning RED (Full) and Green (Emptied).

View Dashboard: The right side of the screen displays live statistics.

**4. Logic & Parameters
**
Parameter

Value

Description

Waste Generation

~10% / hour

Simulates daily trash accumulation.

Threshold

80%

Point at which bin triggers a pickup request.

Truck Fleet

2 Trucks

Located at Main Depot.

Service Time

Instant

Simplified for visual demonstration.

Retry Logic

10 Minutes

Frequency a full bin checks for available trucks.

© 2025 Aiman Darakhshan - GIKI
