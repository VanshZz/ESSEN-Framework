# ESSEN Framework: Overview

Welcome to the **ESSEN Framework**, a distributed 4-tier system designed for remote telemetry, system monitoring, and real-time command execution.



## 📁 System Components

This project is divided into three specialized repositories to maintain a clean separation of concerns and a modular architecture:

### 1. [ESSEN-Midman-Server](https://github.com/VanshZz/essen)
**The Logic Tier:** A Flask-based middleware API that manages the communication between the dashboard and the agents.
* Handles **Server-Sent Events (SSE)** for real-time tasking.
* Manages data persistence with **MongoDB**.

### 2. [ESSEN-Control-Dashboard](https://github.com/VanshZz/Stealthpoint-dashboard)
**The Presentation Tier:** A Streamlit-powered command center for administrators.
* Real-time "Live Agent" tracking and search filters.
* Integrated command console and screenshot viewer.

### 3. [ESSEN-Agent](https://github.com/VanshZz/midmanserv)
**The Client Tier:** The Windows-native monitoring agent.
* Features **Caps-Lock aware** keylogging and clipboard monitoring.
* Implements persistence via **Windows Registry** and **Task Scheduler**.

---

## 🏗 Architecture Diagram

1. **Agent (Client)** → Beacons to Midman via REST/SSE.
2. **Midman (Logic)** → Authenticates agent and stores telemetry in **MongoDB**.
3. **Dashboard (UI)** → Fetches live data and pushes commands through Midman.

## 🛠 Tech Stack
* **Languages:** Python
* **Frameworks:** Flask, Streamlit
* **Database:** MongoDB Atlas

---
*Developed for educational purposes focusing on distributed systems and cybersecurity monitoring.*
