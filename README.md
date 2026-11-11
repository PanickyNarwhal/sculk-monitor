<img src="Calibrated_Sculk_Sensor.webp" alt="Sculk Sensor" width="90">

# Sculk Monitor
Multi-language Minecraft server telemetry, log checker, and player stats dashboard

Getting Started
Prerequisites

    Agent: CMake 3.16+ and a C++17 compiler (g++, clang++, or MSVC)

    Backend: Go 1.22+

    Dashboard: Python 3.11+

1. Run the Go Backend
```bash
cd backend-go
export SCULK_API_KEY="dev-secret-key"
go run ./cmd/server
# Listening on http://localhost:8080
```
2. Run the C++ Agent
```bash
cd agent-cpp
cmake -B build && cmake --build build
./build/sculk-agent --mc-dir "/path/to/minecraft" --api "http://localhost:8080/api/ingest" --key "dev-secret-key"
```
3. Run the Python Dashboard
```bash
cd dashboard-py
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
streamlit run app.py
```
