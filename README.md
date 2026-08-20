# 🛰️ RescueMap AI: Autonomous Disaster Triage & Relief Logistics

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=for-the-badge&logo=github)](https://anshuu-01.github.io/rescuemap-ai/)
[![AI Engine](https://img.shields.io/badge/AI%20Vision-Gemini%201.5%20%2F%20GPT--4o-emerald?style=for-the-badge&logo=google)](https://aistudio.google.com/)
[![GIS Engine](https://img.shields.io/badge/GIS%20Satellite-ESRI%20%26%20CartoDB-amber?style=for-the-badge)](https://leafletjs.com/)
[![Hackathon](https://img.shields.io/badge/Hackathon%20Project-Disaster%20Response%20AI-red?style=for-the-badge)](https://github.com/anshuu-01/rescuemap-ai)

> **Autonomous Multimodal AI Vision, High-Resolution GIS Satellite Reconnaissance, and Real-Time Disaster Resource Allocation for Emergency Operations Centers (NDRF / ODRAF / OSDMA).**

---

## 📌 Problem Statement
During severe climate disasters (cyclones, flash floods, storm surges), ground communication infrastructure collapses, leaving emergency coordinators with unverified information and critical 24–48 hour reconnaissance delays. Disaster response teams struggle to identify where structural collapse is most severe and where relief resources (drinking water, medical kits, life rafts) are urgently needed.

---

## 💡 Solution: RescueMap AI
**RescueMap AI** ingests aerial drone imagery and ground camera feeds to instantly:
1. **Detect & Quantify Damage:** Autonomously classifies flood inundation, structural load-bearing collapse, and blocked transit corridors using Multimodal Vision AI.
2. **AI Image Deblurring & Super-Resolution:** Sharpens shaky, rain-fogged, low-light disaster imagery for enhanced damage verification.
3. **Dynamic Priority Scoring:** Computes a normalized mathematical triage priority score ($0 - 100$ pts) across four weighted dimensions.
4. **Real-Time Resource Allocation:** Dynamically calculates clean drinking water 💧, emergency medical packets 💊, and temporary shelter units ⛺ based on live site severity.
5. **Interactive Rescue Team Dispatch:** Dispatches NDRF, ODRAF, and Fire Services to precise coordinates with live 1-click citizen callback channels.

---

## 🧮 Mathematical Priority Scoring Formulation

The emergency priority ranking score $P \in [0, 100]$ for each incident site $i$ is determined by:

$$P_i = 100 \times \left( w_d \cdot D_i + w_v \cdot V_i + w_a \cdot A_i + w_c \cdot C_i \right)$$

Where:
* **$D_i \in [0, 1]$ (Structural Damage Factor):** Derived from AI vision damage segmentation (`minor`: $0.2$, `major`: $0.6$, `destroyed`: $1.0$).
* **$V_i \in [0, 1]$ (Demographic Vulnerability Index):** Population density, children/elderly count, and critical facility proximity.
* **$A_i \in [0, 1]$ (Road Transit Accessibility Score):** Penalty based on roadway blockages and flood water levels.
* **$C_i \in [0, 1]$ (AI Confidence Factor):** Multimodal visual confidence score.
* **Weights:** Default calibration: $w_d = 0.40, w_v = 0.30, w_a = 0.20, w_c = 0.10$ ($\sum w = 1.0$).

---

## 🚀 Key Features

* **🛰️ Multi-Source GIS Satellite & Street Map:** High-resolution ESRI World Imagery and CartoDB Voyager vector streets requiring zero API keys.
* **📸 Real-Time Drone & Ground Upload:** Upload any aerial photo with instant global location geocoding.
* **✨ AI Image Deblur & Super-Resolution:** In-browser spatial convolution filter restoring motion-blurred disaster feeds with an interactive before/after split slider.
* **📊 100% Dynamic Reactive Charts:** Grouped bar charts and doughnut charts update in real-time as imagery is ingested.
* **👷 Tactical Rescue Team Dispatch:** Assign, reassign, and deploy NDRF / ODRAF task forces to specific disaster sectors.
* **📞 Ground Citizen & SOS Callback:** 1-click direct phone call and WhatsApp contact integration for field rescue coordinators.
* **📑 SITREP & Technical Whitepaper:** 1-click GeoJSON / JSON situation report generator and judge's technical documentation dossier.

---

## 🛠️ Technology Stack

| Layer | Technology |
|---|---|
| **Frontend Framework** | React 18 (Standalone Zero-Build Architecture) |
| **Styling & UI** | Tailwind CSS with responsive glassmorphism |
| **GIS & Mapping** | Leaflet GIS with ESRI Satellite World Imagery & CartoDB Vector Tiles |
| **Data Visualization** | Chart.js with responsive dynamic data bindings |
| **AI Vision Engine** | Google Gemini 1.5 Flash Vision / OpenAI GPT-4o-mini & High-Pass Laplacian Preprocessor |
| **Geocoding Engine** | Open-Meteo & Photon Komoot Open CORS Geocoder |

---

## 💻 Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/anshuu-01/rescuemap-ai.git
   cd rescuemap-ai
   ```
2. Open `index.html` directly in any modern web browser, or serve with Python:
   ```bash
   python -m http.server 3000
   ```
3. Open `http://localhost:3000/index.html` in your browser.

---

## 👥 Authors & Team
* **Lead Developer / Disaster AI Coordinator:** [@anshuu-01](https://github.com/anshuu-01)
* **Project:** RescueMap AI — Autonomous Disaster Relief & Triage Intelligence
