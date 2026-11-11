<img src="Calibrated_Sculk_Sensor.webp" alt="Sculk Sensor" width="90">

# Sculk Monitor
Minecraft server telemetry, log checker, and player stats dashboard

Getting Started
Prerequisites

    Backend: Go 1.22+

    Dashboard: Python 3.11+

1. Run the Go Backend
```bash
cd backend-go
export SCULK_API_KEY="dev-secret-key"
go run ./cmd/server
# Listening on http://localhost:8080
```

2. Run the Python Dashboard
```bash
cd dashboard-py
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
streamlit run app.py
```
