# Fallout Index: Geopolitical Crisis Simulator
**A Real-time Strategic Impact Analysis Dashboard**

## 🌐 Overview
The Fallout Index is a full-stack simulation tool designed to analyze and visualize the potential global consequences of geopolitical conflicts. By integrating live news feeds with Generative AI analysis, the dashboard provides dynamic "Situation Reports" (SitReps) and a visual fallout overlay on an interactive world map.

## 🛠️ Tech Stack
- **Frontend:** HTML5, Tailwind CSS, Leaflet.js (Geospatial Mapping)
- **Backend Automation:** n8n (Workflow Orchestration)
- **AI Engine:** OpenRouter (GPT-4 / Claude-3 / DeepSeek)
- **Deployment:** Vercel (Frontend) & Render (Backend/Docker)

## 🏗️ Architecture
1. **Trigger:** User inputs an Aggressor and Victim nation on the dashboard.
2. **Data Acquisition:** n8n scrapes real-time RSS news feeds for current context.
3. **Reasoning:** The AI engine processes the context and predicts fallout for neighboring regions in structured JSON.
4. **Visualization:** The frontend parses the JSON to apply a custom-styled overlay and populates an interactive intelligence panel.

## 🚀 Deployment Instructions

### Backend (Render)
1. Deploy the `/backend` folder as a **Docker Web Service**.
2. Set Environment Variables:
   - `N8N_ENCRYPTION_KEY`: [Your Secret Key]
   - `WEBHOOK_URL`: [Your Render URL]
3. Import the `workflow.json` into your n8n instance.

### Frontend (Vercel)
1. Deploy the `/frontend` folder to Vercel.
2. Update the `fetch()` URL in `index.html` to point to your Render production webhook.

## 📂 Project Structure
- `/frontend`: Dashboard UI and Map Logic.
- `/backend`: Docker configuration and n8n workflow backup.

---
**Author:** Cache-22
**Institution:** CMR Institute of Technology, Bengaluru
---

Output of Workflow's Successful Execution:
<img width="1917" height="907" alt="image" src="https://github.com/user-attachments/assets/f05d5091-40e2-4eae-9cca-8c8123bf8d12" />
