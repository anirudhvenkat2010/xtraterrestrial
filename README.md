# AresNav: Martian EVA & Surface Operations Console 🚀

**Team Name:** Team XTerrestrial  
**Event:** NASA Space Apps Challenge 2026  
**Target Mission Sector:** Jezero Crater, Mars (`18.4447°N, 77.4508°E`)  
**Prototype Version:** v12.0 (Measured Jezero Terrain & Multi-Mission Surface Operations)

---

## 🌌 Mission Overview

**AresNav** is a high-impact, web-based mission control console engineered to plan, simulate, and stress-test human Extravehicular Activities (EVAs) on Mars. Designed specifically for the NASA Space Apps Challenge, AresNav fuses authentic NASA orbital data, topographic Digital Elevation Models (DEMs), and closed-loop life-support physics. It empowers astronauts and mission operators to investigate astrobiological targets while dynamically identifying and bypassing terrain traps and environmental hazards.

---

## ✨ Core Features & Capabilities

* **🧭 2D Physics A\* Pathfinding Engine:** 
  * Computes optimal multi-criteria traverse routes across four specialized modes:
    1. *Optimal Safety & Low Energy:* Automatically detours around modeled $>20^\circ$ MOLA cliff scarps and loose thermal-inertia dust traps.
    2. *Max Astrobiology Science Yield:* Pulls trajectories through high-priority CRISM-inspired carbonate and smectite clay units.
    3. *Shortest Euclidean Distance:* Direct point-to-point vector navigation (exposing steep terrain fall hazards).
    4. *Emergency Walk-Back Abort:* Computes the minimum-energy return vector to the nearest safe haven or habitat.
  * Includes a real-time **Route Strategy Trade-off Analysis** table comparing distance, max slope, $\text{O}_2$ burn, and science points.

* **🫁 Closed-Loop xEMU PLSS Life Support:**
  * Real-time physiological telemetry calculator tracking metabolic rates ($\dot{Q}_{\text{met}}$), primary and reserve oxygen consumption ($1.65\text{ kg}$ capacity), $\text{CO}_2$ amine scrubber margins, suit Li-Ion battery drain ($2,100\text{ Wh}$), and cumulative radiation dose.
  * Built-in mandatory **60-minute walk-back contingency reserve** enforcing a $420$-minute safe duration cap.

* **⚡ NASA DONKI Space Weather & MEDA Integration:**
  * Dynamic environmental anomaly injector to stress-test crew survivability against live CCMC DONKI Solar Energetic Particle (SEP) storms and regional dust storms ($\tau = 2.1$).
  * Automatically triggers redline alarms and emergency abort routing upon solar flux spikes.

* **📸 Multi-Instrument "Click-to-Core" Inspector:**
  * Instantaneous multi-instrument fusion allowing operators to click any location on Jezero Crater to inspect MOLA slopes, MRO CRISM mineral spectra, THEMIS thermal inertia traction, and live NASA Mars 2020 Perseverance Mastcam-Z ground-truth surface imagery by Sol.

---

## 🛠️ Technology Stack

* **Frontend Framework:** HTML5, Tailwind CSS (v3.4), FontAwesome 6.4.0, Google Fonts (*Inter* & *JetBrains Mono*).
* **Mapping & Geospatial Layers:** Leaflet.js (v1.9.4), custom HTML5 Canvas topographic contour relief layers, and NASA Mars Trek WMTS REST tile integration.
* **Logic & Computation:** Pure client-side JavaScript implementing custom A* pathfinding heuristics, grid matrix transformers, and physics-based PLSS consumable equations.

---

## 🚀 Quick Start / Local Deployment

1. Clone or download this repository.
2. Ensure you have a modern web browser (Chrome, Firefox, Edge, or Safari).
3. Open `nasaapp.html` directly in your browser, or serve it locally via a static server:
   ```bash
   npx http-server
   ```
4. Dismiss the mission welcome briefing and begin exploring Jezero Crater!

---

## 🔬 Automated Verification Test Suite

The built-in test runner verifies core system resilience across 6 key scenarios:
* **TC-01:** Invalid Coordinate Bounds Parser
* **TC-02:** API Outage & PDS Failover Engine
* **TC-03:** Steep Cliff Route Failure & Scarp Avoidance
* **TC-04:** PLSS 480-Min Redline Alarm
* **TC-05:** DONKI SEP Radiation Storm Abort
* **TC-06:** CRISM Mineral Verification Matrix

---

## 🛡️ Defensive Engineering & Data Provenance

*AresNav is a research prototype built for demonstration and educational exploration.* While integrating authentic NASA mission references (Mars Trek, MRO HiRISE, MRO CRISM, Perseverance Traverse, and CCMC DONKI), local elevation profiles, mineral polygons, and life-support calculations utilize sampled datasets and illustrative modeling parameters. Always review data provenance and citations within the console before mission planning.

---

*Explore Jezero. Return safely.* — **Team XTerrestrial**
