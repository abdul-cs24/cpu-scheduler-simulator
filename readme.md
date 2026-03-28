# CPU Scheduling Simulator

A fully interactive browser-based simulator for four classic CPU scheduling algorithms, featuring real-time animated Gantt charts and detailed performance metrics.

## 🚀 Live Demo
Open `index.html` in any modern browser — no installation required.

## 📋 Algorithms Implemented
| Algorithm | Type | Description |
|---|---|---|
| FCFS | Non-Preemptive | First Come First Served — processes executed in arrival order |
| SJF | Non-Preemptive | Shortest Job First — shortest burst time picked from ready queue |
| SRTF | Preemptive | Shortest Remaining Time First — preempts on shorter arrival |
| Round Robin | Preemptive | Time-sliced execution with configurable quantum |
| Priority (NP) | Non-Preemptive | Lower priority number = higher priority |
| Priority (P) | Preemptive | Preemptive variant of priority scheduling |

## 🗂️ Module Architecture

### Module 1 — Input & GUI Layer
- Dynamic process table (up to 10 processes)
- Fields: Arrival Time, Burst Time, Priority
- Algorithm switcher + Time Quantum control
- Simulation speed slider (1× – 10×)
- Input validation with error messages

### Module 2 — Scheduling Engine
- Pure JavaScript functions, no UI dependency
- Produces `timeline[]` of (pid, start, end) slices
- Computes per-process: Completion, Turnaround, Waiting, Response times
- Handles idle CPU gaps and preemption correctly

### Module 3 — Visualization & Metrics
- Animated Gantt chart with per-process colored rows
- Real-time ready queue state display
- Summary stat cards: Avg WT, Avg TAT, CPU Utilization, Throughput
- Per-process metrics table
- Compare mode: runs all 6 algorithms side-by-side

## 📊 Performance Metrics
- **Waiting Time** = Completion − Arrival − Burst
- **Turnaround Time** = Completion − Arrival
- **Response Time** = First CPU start − Arrival
- **CPU Utilization** = Total Burst / Total Span × 100%
- **Throughput** = Number of Processes / Total Time

## 🛠️ Technology Stack
- **Language**: JavaScript (Vanilla ES6+)
- **UI**: HTML5 + CSS3 (CSS Variables, Grid, Flexbox)
- **No external dependencies** — runs entirely in-browser
- **Version Control**: Git / GitHub

## 🗃️ Project Structure
```
cpu-scheduler-simulator/
├── OS_CA2+project.html       ← Complete single-file application
└── README.md        ← This file
```

## 📝 How to Use
1. Select a scheduling algorithm from the dropdown
2. Add processes using the table (or click **Load Sample**)
3. Set Time Quantum if using Round Robin
4. Adjust simulation speed with the slider
5. Click **▶ Run Simulation** to watch the Gantt chart animate
6. Switch to the **Compare All** tab to benchmark all algorithms

## 👨‍💻 CA2 — CSE-316
**Subject**: Operating Systems  
**Assignment**: CPU Scheduling Algorithm Simulator with Real-time Visualization

