# AresNav: Martian EVA & Surface Operations Console 🚀

**Team Name:** Team XTerrestrial  
**Event:** NASA Space Apps Challenge 2026  
**Target Sector:** Jezero Crater, Mars (`18.4447°N, 77.4508°E`)

---

## 🌌 Overview

**AresNav** is an advanced interactive research prototype and mission-critical operations console designed to plan, simulate, and stress-test human Extravehicular Activities (EVAs) on Mars. Fusing authentic NASA orbital data, topographic Digital Elevation Models (DEMs), and closed-loop life-support physics, AresNav empowers astronauts and mission planners to investigate astrobiological targets while dynamically bypassing terrain traps and environmental hazards.

---

## ✨ Key Features

* **🧭 2D Physics A\* Pathfinding Engine:** Computes optimal multi-criteria traverse routes across four specialized modes:
  * *Optimal Safety & Low Energy:* Avoids modeled $>20^\circ$ MOLA cliff scarps and loose aeolian dust traps.
  * *Max Astrobiology Science Yield:* Prioritizes modeled CRISM-inspired carbonate and smectite clay targets.
  * *Shortest Euclidean Distance:* Direct point-to-point vector navigation (exposing steep terrain risks).
  * *Emergency Walk-Back Abort:* Calculates the fastest emergency return vector to the nearest safe haven or habitat.
* **🫁 Closed-Loop xEMU PLSS Life Support:** Real-time physiological modeling tracking metabolic rates, primary/reserve oxygen consumption, $\text{CO}_2$ amine scrubber capacity, suit battery drain, and cumulative radiation dose with a mandatory 60-minute walk-back contingency reserve.
* **⚡ NASA DONKI Space Weather & MEDA Integration:** Dynamic environmental anomaly injector simulating Solar Energetic Particle (SEP) storms and regional dust storms ($\tau = 2.1$), automatically triggering redline contingency routing.
* **📸 Multi-Instrument Click-to-Core Inspector:** Instantaneous multi-instrument fusion providing MOLA slope gradients, MRO CRISM mineralogy spectra, THEMIS thermal inertia traction, and live NASA Mars 2020 Perseverance Mastcam-Z ground-truth surface imagery by Sol.
* **🧪 Automated End-to-End Test Suite:** Built-in verification engine executing 6 rigorous test cases (`TC-01` through `TC-06`) validating geospatial bounds, telemetry failovers, cliff route failures, and PLSS redline alarms.

---

## 🛠️ Tech Stack

* **Frontend Framework:** HTML5, Tailwind CSS (v3.4), FontAwesome 6.4.0, Google Fonts (*Inter* & *JetBrains Mono*).
* **Mapping & Geospatial:** Leaflet.js (v1.9.4), custom HTML5 Canvas topographic contour relief layers, and NASA Mars Trek WMTS REST tile integration.
* **Logic & Computation:** Pure client-side JavaScript implementing custom A* pathfinding heuristics, geospatial coordinate parsers, and physics-based PLSS consumable equations.

---

## 🚀 Quick Start / Running the App

1. Clone or download this repository.
2. Ensure you have a modern web browser (Chrome, Firefox, Edge, or Safari).
3. Open `nasaapp.html` directly in your browser or serve locally:
   ```bash
   npx http-server
🔬 Automated Verification Test Suite
AresNav includes an embedded automated test suite to verify system resilience:

TC-01: Invalid Coordinate Bounds Parser

TC-02: API Outage & PDS Failover Engine

TC-03: Steep Cliff Route Failure & Scarp Avoidance

TC-04: PLSS 480-Min Redline Alarm

TC-05: DONKI SEP Radiation Storm Abort

TC-06: CRISM Mineral Verification Matrix

🛡️ Defensive Engineering & Data Provenance
AresNav is a research prototype for demonstration purposes. While integrating real NASA catalog references (Mars Trek, MRO HiRISE, MRO CRISM, Perseverance Traverse, and CCMC DONKI), local elevation profiles, mineral polygons, and life-support calculations utilize sampled datasets and illustrative modeling parameters. Always review data provenance and citations within the console before mission planning.

Explore Jezero. Return safely. — Team XTerrestrial


---

### **Immediate Execution Checklist**
1. Navigate to your GitHub repository (`xtraterrestrial`).
2. Click on the `README.md` file and select the **Edit** (pencil) icon.
3. Paste the Markdown text above into the editor.
4. Click **Commit changes** to update your repository public documentation.   
