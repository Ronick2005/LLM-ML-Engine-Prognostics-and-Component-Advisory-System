# LLM ML Engine Prognostics and Component Advisory System

![Python](https://img.shields.io/badge/Python-3.9-blue)
![React](https://img.shields.io/badge/Frontend-React-blue)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A full stack AI powered system for predictive aircraft engine health monitoring and component failure advisory.  
Combines advanced ML techniques (Tsfresh, HMM, Autoencoders) with LLM backed logic and per engine memory to detect, score, and visualize anomalies with React + Tailwind dashboard.

---

## Features

- Real-world aircraft sensor dataset (NASA C-MAPSS)
- Fault state modeling using Hidden Markov Models
- Anomaly detection with Autoencoder reconstructions
- Tail-number based aircraft memory
- Feature-rich dashboard with cluster IDs and state plots
- LLM-ready memory and summarization logic per engine
- Time-series feature extraction using tsfresh
- Extendable with DTW, AutoKeras, Survival Analysis, and more

---

## Folder Structure

```
LLM-Engine-Prognostics/
├── backend/                  # Flask API + ML pipeline
│   ├── app.py
│   ├── static/
│   │   └── dashboard_anomaly_plot.png
│   └── data/
│       └── processed/
│           └── sensor_log.csv
├── frontend/                 # React + Tailwind dashboard
│   ├── src/
│   └── public/
├── data/                     # NASA C-MAPSS raw files
├── requirements.txt
└── README.md
```

---

## ML Pipeline

1. **tsfresh** – Extracts robust time-series features
2. **HMM** – Predicts hidden health states of engines
3. **Autoencoder** – Detects anomalies from reconstruction loss
4. **Memory Layer** – Per-aircraft sensor history by `engine_id`
5. **Dashboard** – Tail-number selection, health states, plots

---

## API Endpoints

| Route | Description |
|-------|-------------|
| `/api/health_summary` | Full anomaly + state + features |
| `/api/engines` | List of all aircraft (tail numbers) |
| `/api/engine/<id>` | Logs of specific aircraft |

---

## Dataset Used

**NASA C-MAPSS** — Jet engine degradation simulator  
Source: [Kaggle](https://www.kaggle.com/datasets/behrad3d/nasa-cmaps)

---

## Future Work

- AutoKeras integration for neural search
- DTW-based time-series clustering
- Genetic Algorithms for fault optimization
- LLM response augmentation with memory
- Real-time alerting via WebSocket
- GCP/AWS deployment with Vector DB memory

---

## License

This project is licensed under the MIT License.

---

## Acknowledgments

- NASA for the C-MAPSS dataset
- Contributors behind tsfresh, hmmlearn, TensorFlow, React

---
