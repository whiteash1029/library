# Smart Traffic Management System (STM)

This project is a modular, scalable starter for a next-generation AI-based Smart Traffic Management System.  
It features a Python backend (FastAPI), modular AI/simulation/vision services, a React dashboard, and Docker-based orchestration.

## Features

- **Real-time vehicle/pedestrian detection** (edge AI, YOLOv8-ready)
- **Adaptive RL-based traffic signal optimization** (SUMO integration)
- **Incident/event ingestion and alerts**
- **Live congestion heatmap and camera feeds**
- **Manual override and authority dashboard**
- **Analytics and offline simulation for planning**
- **Microservice, cloud/edge-first design**

---

## Architecture

```
Cameras/Sensors ──▶ [Python Edge AI] ──▶ [FastAPI Backend] ──▶ [React Dashboard]
           ▲                   │                     │
           │                   ▼                     ▼
      SUMO Simulator   RL/AI Modules        Analytics & Storage
```

---

## Getting Started

### Prerequisites

- Docker & Docker Compose
- Python 3.10+ (for local dev)
- Node.js 18+ (for React local dev)

### Quickstart (with Docker Compose)

```bash
git clone https://github.com/whiteash1029/library.git
cd library
docker-compose up --build
```

- Backend: http://localhost:8000
- Frontend: http://localhost:3000

### Manual Dev

**Backend:**
```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload
```

**Frontend:**
```bash
cd frontend
npm install
npm run dev
```

---

## Project Structure

```
/
├── backend/
│   ├── main.py              # FastAPI application
│   ├── requirements.txt
│   ├── ai/                  # RL/AI modules
│   ├── vision/              # Computer vision inference
│   ├── simulation/          # SUMO interface
│   ├── analytics/           # Historical/statistical analysis
│   └── data_pipeline/       # Kafka/MQTT, streaming, ingestion
├── frontend/
│   └── src/
│       ├── App.jsx
│       ├── index.js
│       └── components/
│           └── Dashboard.jsx
├── docker-compose.yml
└── README.md
```

---

## Next Steps

- Implement your AI/computer vision models in `backend/vision` and RL agents in `backend/ai`
- Connect SUMO or a real camera feed for simulation/testing
- Build out the React dashboard with real API hooks and visualization

---

## License

MIT (starter scaffold)
