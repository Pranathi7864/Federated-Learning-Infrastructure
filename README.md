# Federated-Learning-Infrastructure

# 🛡️ FedFraud  
### Privacy-Preserving Federated Fraud Detection Platform

**FedFraud** is a full-stack, decentralized financial intelligence system designed to detect fraudulent activities across multiple banking institutions **without sharing raw customer data**.

It combines a modern **Secure Insight Dashboard (Frontend)** with a **Federated, Privacy-Preserving AI Backend**, enabling collaborative fraud detection while maintaining strict data privacy, sovereignty, and regulatory compliance.

---

## 🧠 Core Concept

> **“The model travels to the data — not the data to the model.”**

Banks collaboratively train a global fraud detection model using **Federated Learning**, while **Differential Privacy** ensures that no individual transaction or customer record can ever be reconstructed.

---

## 📁 Project Structure

FedFraud/
│
├── frontend/ # Secure Insight Dashboard (UI)
│ ├── src/
│ │ ├── components/ # Reusable UI components (Modal, Charts, etc.)
│ │ ├── pages/
│ │ ├── App.tsx
│ │ ├── main.tsx
│ │ └── index.css
│ ├── index.html
│ ├── package.json
│ └── vite.config.ts
│
├── backend/ # Federated Learning Backend
│ ├── server.py # Global Federated Orchestrator
│ ├── client.py # Bank-side Training Node
│ ├── model_utils.py # Shared FinancialBrain Model
│ ├── cleaned_DATA.csv # Local bank data (never shared)
│ └── requirements.txt
│
├── README.md # Combined Documentation
└── .gitignore


---

## 🚀 Key Features

### 🔐 Backend (Federated AI Engine)

- **Federated Learning (Flower)**
  - Collaborative model training without data sharing
  - Full data sovereignty for participating banks

- **Differential Privacy (Opacus – DP-SGD)**
  - Noise added to gradients to prevent inversion attacks
  - Guarantees mathematical privacy protection

- **FedProx Optimization**
  - Handles data and system heterogeneity
  - Ensures stable training across unequal clients

- **Zero-Trust Architecture**
  - No centralized data storage
  - Server only sees anonymized mathematical updates

---

### 🖥️ Frontend (Secure Insight Dashboard)

- Built with **React + Vite + TypeScript**
- Styled using **Tailwind CSS & shadcn/ui**
- Interactive fraud analytics dashboard
- Modal-based UI for alerts and insights
- Fully removed Lovable branding
- Ready for real-time backend integration

---

## 🏗️ System Architecture

### Federated Learning Flow

Bank A (Client) ─┐
Bank B (Client) ─┼──► Global Server (FedProx Aggregation)
Bank C (Client) ─┘
▲
│
Raw data never leaves the bank


### Full Stack Flow

Frontend Dashboard ──► Backend API ──► Federated Learning Engine


---

## 🛠️ Technology Stack

### Frontend
- React
- Vite
- TypeScript
- Tailwind CSS
- shadcn/ui

### Backend
- Python 3.10+
- Flower (flwr)
- PyTorch
- Opacus (Differential Privacy)
- Pandas

---

## ⚙️ Setup & Installation

### 1️⃣ Prerequisites

- Node.js **18+**
- Python **3.10+**
- All backend clients connected to the same network

---

## 🖥️ Frontend Setup

```bash
cd frontend
npm install
npm run dev
Access the dashboard at:

http://localhost:8080
🧠 Backend Setup (Federated Learning)
Install Dependencies
cd backend
pip install flwr torch pandas opacus
Network Configuration
Find the Server IPv4 Address

Windows: ipconfig

Linux / macOS: ifconfig

Update the server IP in client.py:

SERVER_IP = "192.168.x.x"
Ensure port 8888 is allowed through the firewall.

🚦 Execution Guide
Step 1: Start the Global Server
python server.py
Acts as the global federated coordinator

Waits until a minimum of 3 clients connect

Step 2: Start Bank Clients
Run on each participating bank machine:

python client.py
✔ Each bank:

Trains locally on its private dataset

Shares only privacy-preserving updates

Never exposes raw transaction data

📊 Technical Specifications
Component	Details
Framework	Flower (flwr)
Privacy Engine	Opacus (DP-SGD)
Model	FinancialBrain Neural Network
Loss Function	Mean Squared Error (MSE)
Optimizer	Adam with FedProx
Privacy Budget	ε = 1.1, δ = 10⁻⁵
Aggregation	FedProx
🛡️ Security & Privacy Disclaimer
No raw transaction data is transmitted

No centralized data storage

Only clipped, noised gradients are shared

Resistant to inversion and membership inference attacks

This system follows privacy-by-design principles and is suitable for financial and regulatory-sensitive environments.

🔮 Future Enhancements
Real-time fraud alerts on the dashboard

Blockchain-based audit logging

Secure authentication for participating banks

Cloud-based federated deployment
👩‍💻 Author

Pranathi P K, Ragul P, Reena Evelin J, Rohith g
B.Tech Information Technology, Dr.N.G.P. Institute of Technology
BS Data Science – IIT Madras
