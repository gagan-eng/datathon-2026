# 🚔 DRISHTI — AI-Powered Criminal Intelligence Platform

> **AI-powered criminal intelligence and investigation support platform for the Karnataka State Police Datathon 2026.**

DRISHTI is an AI-powered criminal intelligence platform designed to help police officers overcome the challenges of fragmented crime records and time-consuming manual investigations.

The platform enables officers to **search criminal histories, identify criminal connections, analyse crime patterns, visualize criminal networks, assess reoffending risk, and receive AI-assisted investigation support** through a centralized intelligence dashboard.

---

## 🚀 Key Features

### 🤖 AI Investigation Chatbot
- AI-powered investigation assistant using **Google Gemini**
- Natural-language interaction for investigation support
- Helps officers query available criminal and case information
- Provides intelligent analysis of investigation data

### 🔍 Smart Criminal Search
- Search criminals using names and aliases
- **Alias matching** using RapidFuzz
- Quickly retrieve criminal histories and associated cases
- Helps investigators identify potential matches despite variations in names

### 🕸️ Criminal Network Graph
- Interactive visualization of criminal relationships
- Displays connections between:
  - Criminals
  - Cases
  - Locations
  - Associates
- Built using **NetworkX and PyVis**
- Helps investigators discover hidden relationships

### 🔗 Case Connection Analysis
- Identifies relationships between different criminal cases
- Helps investigators discover potentially connected incidents
- Supports investigation through relationship-based analysis

### ⚠️ PRECOG — Reoffending Risk Prediction
- Machine Learning-based reoffending risk assessment
- Uses historical crime-related data
- Helps identify patterns associated with repeat offending
- Built using **Scikit-learn**

> **Note:** PRECOG is an analytical decision-support feature and should not be used as the sole basis for law-enforcement decisions.

### 📊 Crime Analytics Dashboard
- Interactive crime statistics
- Crime trends and distributions
- Data-driven visual analytics
- Interactive charts using **Plotly**

### 🕐 Crime Clock Analysis
- Analyses crime occurrence across different times of the day
- Identifies temporal patterns
- Helps understand when crimes are more frequently reported

### 🗺️ Crime Heatmap
- Geographical visualization of crime incidents
- Identifies high-crime areas
- Supports spatial crime analysis

### 📡 Live Intelligence Feed
- Centralized intelligence feed
- Displays recent crime-related information
- Helps officers monitor incoming intelligence

### 🏢 Station Command Overview
- Overview of station-level crime information
- Helps senior officers monitor operational intelligence
- Supports station-level decision making

### 👮 Role-Based Access Control

DRISHTI supports different levels of access based on the user's role:

| Role | Access |
|---|---|
| 👮 Constable | Basic investigation and search features |
| 👮‍♂️ Inspector | Investigation, analytics and case intelligence |
| 🧑‍✈️ DCP | Advanced analytics and station-level intelligence |
| 🔐 Admin | System administration and full access |

---

# 🧠 System Overview

```text
                    ┌─────────────────────┐
                    │      Police User    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   DRISHTI Login     │
                    │  Role-Based Access  │
                    └──────────┬──────────┘
                               │
                               ▼
                 ┌───────────────────────────┐
                 │    Intelligence Dashboard │
                 └─────────────┬─────────────┘
                               │
          ┌────────────────────┼────────────────────┐
          │                    │                    │
          ▼                    ▼                    ▼
   Criminal Search       Crime Analytics      AI Chatbot
          │                    │                    │
          ▼                    ▼                    ▼
   Alias Matching        Crime Patterns       Gemini AI
          │                    │                    │
          └──────────────┬─────┴────────────┬───────┘
                         │                  │
                         ▼                  ▼
                 Network Analysis      PRECOG ML
                         │                  │
                         ▼                  ▼
                Criminal Connections   Risk Analysis
```

---

# 🛠️ Technology Stack

## Frontend

- **Streamlit**
- Streamlit Option Menu
- Custom CSS

## Artificial Intelligence & Machine Learning

- **Google Gemini 1.5 Flash**
- **Scikit-learn**
- **RapidFuzz**

## Data Processing

- **Pandas**
- **NumPy**

## Data Visualization

- **Plotly**
- **NetworkX**
- **PyVis**

## Backend & Deployment

- **Python**
- **Zoho Catalyst AppSail**
- **Python-dotenv**

---

# 📂 Project Structure

```text
DRISHTI/
│
├── app.py
├── login.py
├── dashboard.py
├── chatbot.py
├── criminal_search.py
├── network_graph.py
├── case_connections.py
├── crime_clock.py
├── heatmap.py
├── precog.py
├── live_feed.py
├── all_stations.py
├── requirements.txt
│
├── data/
│   └── ...
│
└── README.md
```

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/Kunal-Nigewan/DRISHTI-KSP-Datathon-2026.git
```

## 2. Navigate to the Project Directory

```bash
cd DRISHTI-KSP-Datathon-2026
```

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 4. Configure Environment Variables

Create a `.env` file in the project root:

```env
GEMINI_API_KEY=YOUR_GEMINI_API_KEY
```

Replace `YOUR_GEMINI_API_KEY` with your Google Gemini API key.

## 5. Run the Application

```bash
streamlit run app.py
```

The application will start locally and can be accessed through the Streamlit URL displayed in the terminal.

---

# 🔐 Environment Variables

| Variable | Description |
|---|---|
| `GEMINI_API_KEY` | API key used to access Google Gemini |

Example:

```env
GEMINI_API_KEY=your_api_key_here
```

> **Security:** Never commit your `.env` file or API keys to GitHub.

Add the following to `.gitignore`:

```gitignore
.env
__pycache__/
*.pyc
.venv/
venv/
```

---

# 🎯 Problem Statement

Police departments often rely on **fragmented records and manual investigation processes**.

This can make it difficult and time-consuming to:

- Retrieve complete criminal histories
- Identify aliases and matching identities
- Discover relationships between criminals
- Connect related cases
- Analyse crime trends
- Identify crime hotspots
- Understand temporal crime patterns
- Assess potential reoffending patterns
- Make timely operational decisions

Traditional investigation workflows can therefore require significant manual effort and information gathering.

---

# 💡 Solution

**DRISHTI** brings these intelligence capabilities together into a centralized AI-powered platform.

The platform provides:

```text
Crime Data
    │
    ▼
Centralized Intelligence
    │
    ├──► Smart Criminal Search
    │
    ├──► Alias Matching
    │
    ├──► Criminal Network Analysis
    │
    ├──► Case Connection Analysis
    │
    ├──► Crime Analytics
    │
    ├──► Crime Clock
    │
    ├──► Crime Heatmap
    │
    ├──► PRECOG Risk Prediction
    │
    └──► AI Investigation Assistant
```

This allows officers to move from **raw records → connected intelligence → actionable investigative insights** through a single interface.

---

# 🤖 AI Investigation Workflow

A typical investigation workflow can be represented as:

```text
Officer
   │
   ▼
Search Criminal / Case
   │
   ▼
Retrieve Relevant Records
   │
   ▼
Alias Matching
   │
   ▼
Identify Related Cases
   │
   ▼
Generate Criminal Network
   │
   ▼
Analyse Crime Patterns
   │
   ▼
PRECOG Risk Analysis
   │
   ▼
AI-Assisted Investigation
```

---

# 📊 Intelligence Capabilities

| Capability | Technology |
|---|---|
| Criminal Search | Python + RapidFuzz |
| Alias Matching | RapidFuzz |
| AI Assistant | Google Gemini |
| Risk Prediction | Scikit-learn |
| Crime Analytics | Pandas + Plotly |
| Network Analysis | NetworkX |
| Network Visualization | PyVis |
| Dashboard | Streamlit |
| Deployment | Zoho Catalyst AppSail |

---

# 📸 Highlights

- 🤖 AI-powered investigation assistant
- 🔍 Intelligent criminal search
- 🏷️ Alias matching
- 🕸️ Interactive criminal network visualization
- 🔗 Case connection analysis
- ⚠️ ML-based PRECOG risk prediction
- 📊 Crime analytics dashboard
- 🕐 Crime clock and temporal analysis
- 🗺️ Crime heatmap
- 📡 Live intelligence feed
- 🏢 Station command overview
- 👮 Role-based access control

---

# 🚀 Future Scope

DRISHTI can be extended with additional capabilities such as:

### 🇮🇳 Karnataka Police Database Integration
Integration with authorized Karnataka Police databases to enable real-world operational intelligence.

### 🗣️ Kannada Voice Assistant
Integration with **Bhashini** to provide voice-based investigation assistance in Kannada.

### 📱 Mobile Application
A mobile application for field officers to access intelligence while working in the field.

### 🧠 Predictive Patrol Deployment
Use historical crime patterns to support intelligent patrol planning and resource allocation.

### 🌐 Real-Time Multi-Station Intelligence
Enable real-time intelligence sharing and coordination between multiple police stations.

### 🔍 Advanced Entity Resolution
Improve identification of individuals across fragmented records using advanced entity-resolution techniques.

---

# 👥 Team

## Team CrimeX

| Member |
|---|
| **Kunal Nigewan** |
| **Gagan HV** |
| **Lokrannjan ND** |

---

# 🎥 Demo

Watch the complete DRISHTI demonstration:

[DRISHTI Demo Video](https://drive.google.com/file/d/1Ky0CXyC0pNw7_l-fprAKGXodJUSBb7ex/view?usp=drivesdk&utm_source=chatgpt.com)

---

# 🏆 Karnataka State Police Datathon 2026

DRISHTI was developed as a solution for the **Karnataka State Police Datathon 2026**, with the goal of demonstrating how Artificial Intelligence, Machine Learning, data analytics, and graph-based intelligence can support modern criminal investigation workflows.

---

# ⚠️ Disclaimer

DRISHTI is developed for **educational, research, and demonstration purposes** as part of the Karnataka State Police Datathon 2026.

The platform is intended to assist authorized investigators and **should not replace professional investigation, legal procedures, or human decision-making**.

AI-generated insights and predictive outputs should be independently verified before being used in any operational context.

---

# 📄 License

This project was developed for the **Karnataka State Police Datathon 2026** for educational and demonstration purposes.

---
 
<p align="center">
  <b>DRISHTI — Turning Fragmented Crime Data into Connected Intelligence.</b>
</p>
