# 🌱 Mehrano Agri Farms: Smart IoT Irrigation & Monitoring System

## 📖 Project Overview
This repository contains a comprehensive, IoT-based smart irrigation and environmental monitoring system developed for Mehrano Agri Farms. Designed as a solution for modern agricultural challenges, this project tackles the critical issue of ineffective irrigation management caused by manual monitoring and fixed watering schedules. 

By integrating simulated edge devices, cloud analytics, and business intelligence, this project demonstrates a complete, end-to-end data value chain—transforming raw environmental metrics into automated actions and actionable insights.

## 🎯 Key Objectives
* **Automated Irrigation Control:** Activate water pumps dynamically based on real-time soil moisture thresholds to prevent water wastage and ensure consistent crop growth.
* **Real-Time Environmental Monitoring:** Continuously track soil moisture (%), temperature (°C), humidity (%), and wind speed (km/h).
* **Data Processing & Integration:** Create a seamless, low-latency pipeline from edge sensors to cloud storage using lightweight communication protocols.
* **Advanced Data Visualisation:** Provide clear, predictive insights through interactive dashboards to aid farm managers in long-term decision-making.

## 🛠️ Technology Stack
This project utilizes a hybrid IoT architecture, leveraging both edge and cloud processing layers:
* **Simulation & Hardware:** Cisco Packet Tracer (ESP8266 Microcontrollers, Environmental Sensors, IoT Gateway)
* **Communication Protocol:** MQTT for low-latency, lightweight data transmission
* **Middleware & Integration:** Node-RED for workflow automation, logic implementation, and real-time UI dashboarding
* **Cloud Platform:** ThingSpeak for data storage, MATLAB-based visualisations, and REST API endpoints
* **Business Intelligence:** Microsoft Power BI (integrated via Power Query) for historical trend analysis and KPI tracking

## 🏗️ System Architecture
The system follows a structured, layered IoT approach:
1. **Perception Layer:** Simulated environmental sensors gather physical data from the farm.
2. **Network Layer:** An MQTT broker handles secure, real-time message transmission between the field devices and the gateway.
3. **Integration Layer (Node-RED):** Fetches MQTT data, applies automation logic (e.g., calculating vascular tension index and heat stress), formats the payload, and pushes it to the cloud.
4. **Application Layer (ThingSpeak & Power BI):** Stores distinct data fields and visualises environmental conditions, pump status, and system safety alerts for end-users.

---

## 🔄 Iterative Development Process
This system was built using a structured Software Development Life Cycle (SDLC), evolving from a basic data pipeline into a fully automated, visually rich management system. 

### Phase 1: Base Implementation & Data Processing
* **Focus:** Hardware simulation, cloud connectivity, and data cleanliness.
* **Execution:** Simulated the ESP8266 and sensors in Cisco Packet Tracer. Established MQTT communication to push raw data to ThingSpeak. Applied data cleaning techniques to ensure consistency and built initial MATLAB visualizations (e.g., wind speed gauges, pump status indicators). 
* **Deliverable:** `Iteration 0.pbix` (Baseline Power BI dashboard).

### Phase 2: Middleware Integration & Real-Time Workflows
* **Focus:** System coordination, logic application, and real-time monitoring.
* **Execution:** Introduced **Node-RED** as the central processing layer. Developed workflows to fetch data from the MQTT broker, apply threshold logic (e.g., triggering irrigation when soil moisture drops below 30%), and format the payload for ThingSpeak. Built the first iteration of a live monitoring UI.
* **Deliverables:** `Node-RED Workflow.json`, `Iteration 2.pbix`.

### Phase 3: Advanced Visualisation & User-Centric Optimisation
* **Focus:** Usability, advanced analytics, and automated reporting.
* **Execution:** Completely overhauled the Node-RED dashboard using advanced HTML/CSS template nodes to create highly visual, professional widgets (e.g., Hydraulic Stress Engine, Atmospheric Friction indices). Enriched the Power BI dashboard with complex KPIs, pie charts for soil condition distribution, and configured automated daily refresh schedules via the Web REST API.
* **Deliverables:** `Power Query.json`, `Iteration 3.pbix`.

---

## 📂 Repository Structure
The repository is organized to reflect the files generated throughout the iterative development lifecycle, alongside the final project documentation.
```
mehrano-agri-farms-iot/
├── docs/
│   ├── ThingSpeak Reference Document.docx
│   └── Unit20-AB1-Sahil Faraz (TG 36346).pdf
├── cisco-simulation/
│   └── Mehrano_IoT_Simulation.pkt
├── node-red/
│   ├── Node-RED Workflow.json
│   └── Power Query.json
├── power-bi/
│   ├── Iteration 0.pbix
│   ├── Iteration 2.pbix
│   └── Iteration 3.pbix
└── README.md
