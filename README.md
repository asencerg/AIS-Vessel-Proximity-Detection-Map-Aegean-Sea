# 🛰️ Geospatial Modeling of Maritime Proximity Risk with Synthetic AIS Data 🌊🚢  
*A Geospatial intelligence project exploring near-collision vessel events using Python, synthetic AIS data, and lightweight risk modeling.*

---
![Maritime Collision Visualizer](images/screenshot_proximity_events.png)
---

## Overview

An interactive geospatial analytics project exploring synthetic vessel proximity (near-collision) events using AIS (Automatic Identification System) data modeled on real-world maritime behavior. The map visualizes vessel trajectories in the Aegean Sea and highlights simulated high-risk encounters based on spatial and temporal convergence.

By combining timestamped AIS tracks with proximity logic, it identifies and classifies near-collision risks using distance and timing thresholds. The output includes interactive maps, risk-ranked events, and spatial heatmaps, designed to support maritime situational awareness, safety, and analytics innovation.

As vessel traffic intensifies in constrained or geopolitically sensitive regions, proximity detection and maritime situational awareness have become critical topics in logistics safety, environmental risk, and regional stability. This project demonstrates how open synthetic AIS data and spatial visualization tools can be used to support exploratory analysis of maritime traffic patterns and potential collision scenarios.

Built using Python and Folium, the system combines lightweight geospatial mapping and risk modeling with timestamped proximity markers and animated replay of selected high-risk encounters.

---

## 📌 Features

- 🗺️ **Interactive folium map** displaying vessel paths across the Aegean Sea
- 🎨 **Randomized color-coded trajectories** for visual vessel separation
- 🔴 **Proximity events** marked with exclamation-triangle icons
- 🕒 **Timestamps** included for each vessel position (converted from UNIX epoch)
- ⚓ **Minimalistic base map** using CartoDB Positron tiles for clarity
- 💡 **Lightweight route dots** (not markers) for scalability and performance
- 📁 **All routes** exported to a single `HTML` map, fully interactive offline
- 🎞️ **Animated proximity event GIF** showing vessel trajectories, collision course, and timestamps

![Maritime Collision Visualizer](images/screenshot_proximity_event_1.png)

---

## 📊 Dataset Summary

### 📦 `vessel_positions.csv`

| Column     | Description                          |
|------------|--------------------------------------|
| vessel_id  | Unique identifier for vessel         |
| t          | UNIX timestamp in milliseconds       |
| lon        | Longitude                            |
| lat        | Latitude                             |
| heading    | Vessel heading                       |
| course     | Vessel course over ground            |
| speed      | Vessel speed in knots                |

~4600 AIS messages across 213 unique vessels

### 📦 `simulated_vessel_proximity_events.csv`

| Column       | Description                          |
|--------------|--------------------------------------|
| vessel_id1   | First vessel involved in the event   |
| vessel_id2   | Second vessel involved               |
| lat          | Latitude of proximity event          |
| lon          | Longitude of proximity event         |
| t            | Event timestamp (UNIX ms)            |

237 simulated unintended proximity events

![Maritime Collision Visualizer](images/vessels_11_12_proximity.gif)
---

## 📁 Project Structure

```plaintext
AIS-Vessel-Proximity-Detection-Map-Aegean-Sea/
│
├── data/                               # 📁 Raw synthetic datasets
│   ├── vessel_positions.csv                   # 📊 Vessel position data
│   └── simulated_vessel_proximity_events.csv  # 📊 Simulated proximity event data
│
├── images/                             # 📁 Screenshots and GIFs for visualizations
│   ├── screenshot_proximity_event_1.png  # 📸 Screenshot 1 of proximity event map
│   ├── screenshot_proximity_event_2.png  # 📸 Screenshot 2 of proximity event map
│   ├── screenshot_proximity_events.png   # 📸 Screenshot of multiple proximity events
│   └── vessels_11_12_proximity.gif       # 🎞️ GIF showing animated proximity events and vessel trajectories
│
├── notebooks/                          # 📁 Jupyter notebooks
│   ├── 01_maritime_collision_map.ipynb        # 📓 Initial map visualization with static data
│   └── 02_animated_proximity_event_map.ipynb  # 📓 Animated proximity event visualization with vessel trajectories and collision event
│
├── maritime_collision_visual_map.html  # 🌍 Standalone interactive map output
├── .gitignore                     # 🙈 Files to ignore in Git
├── LICENSE                        # 📄 Open source license
├── README.md                      # 📘 You are here!
└── requirements.txt               # 📦 Python dependencies for the project

```

---

## 🌐 Attribution

**Synthetic AIS Dataset of Vessel Proximity Events** provided by the CREXDATA – Critical Action Planning over Extreme-Scale Data Project, funded by the European Union’s Horizon Europe Programme (Grant agreement No. 101092749). 

Ilias Chamatidis, Giannis Spiliopoulos, Manolis Kaliorakis, Georgios Grigoropoulos, & Konstantina Bereta. (2023). Synthetic AIS Dataset of Vessel Proximity Events (1.0) [Data set]. Zenodo.  
🔗 DOI: [10.5281/zenodo.8358664](http://dx.doi.org/10.5281/zenodo.8358664)  
📍 Aegean Sea – Simulated collision trajectories for maritime safety modeling  
📊 213 vessels, 237 proximity events, ~4600 AIS messages  
📚 Mapping Libraries: Folium, CartoDB Positron Tiles  
📜 License: [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/legalcode)

---

## 📜 License

[MIT License](LICENSE)

