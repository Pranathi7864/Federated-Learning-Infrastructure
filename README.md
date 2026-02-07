# Federated-Learning-Infrastructure

🛡️ FedFraud

Privacy-Preserving Federated Fraud Detection Platform

FedFraud is a full-stack, decentralized financial intelligence system designed to detect fraud across multiple banking institutions without ever sharing raw customer data.

It combines a modern analytics dashboard (frontend) with a federated, privacy-preserving AI backend, enabling secure collaboration across institutions while maintaining strict data sovereignty and regulatory compliance.

🧠 Core Idea

“The model travels to the data — not the other way around.”

Banks collaboratively train a global fraud detection model using Federated Learning, while Differential Privacy ensures that no individual transaction or customer record can ever be reconstructed.

📁 Project Structure
fedfraud/
│
├── frontend/                     # Secure Insight Dashboard (UI)
│   ├── src/
│   │   ├── components/           # Reusable UI components (Modal, etc.)
│   │   ├── pages/
│   │   ├── App.tsx
│   │   ├── main.tsx
│   │   └── index.css
│   ├── index.html
│   ├── package.json
│   └── vite.config.ts
│
├── backend/                      # Federated AI Backend
│   ├── server.py                 # Global federated orchestrator
│   ├── client.py                 # Bank-side training node
│   ├── model_utils.py            # Shared FinancialBrain model
│   ├── cleaned_DATA.csv          # Local bank data (never shared)
│   └── requirements.txt
│
├── README.md                     # Combined project documentation
└── .gitignore

🚀 Key Features & Novelty
🔐 Backend (FedFraud Engine)

Federated Learning (Flower)

Model updates are aggregated, not raw data

Full data sovereignty for banks

Differential Privacy (Opacus – DP-SGD)

Mathematical noise added to gradients

Prevents inversion & membership inference attacks

FedProx Optimization

Handles system & data heterogeneity

Stable training across unequal clients

Zero-Trust Architecture

Server never sees data

Only anonymous, clipped, noised gradients are shared

🖥️ Frontend (Secure Insight Dashboard)

⚡ React + Vite + TypeScript

🎨 Tailwind CSS + shadcn/ui

📊 Fraud analytics dashboard

🪟 Reusable modal components

❌ Lovable branding fully removed

🔗 Ready for real-time backend integration

🏗️ System Architecture
Federated Backend Flow
Bank A (Client) ─┐
Bank B (Client) ─┼──► Global Server (FedProx Aggregation)
Bank C (Client) ─┘
        ▲
        │
  No raw data ever leaves the bank

Full-Stack Flow
Frontend Dashboard ──► Backend API ──► Federated Learning Engine

🛠️ Technology Stack
Frontend

React + Vite

TypeScript

Tailwind CSS

shadcn/ui

Backend

Python 3.10+

Flower (flwr)

PyTorch

Opacus (Differential Privacy)

Pandas

⚙️ Setup & Installation
1️⃣ Prerequisites

Python 3.10+

Node.js 18+

All backend clients connected to the same network

🖥️ Frontend Setup
cd frontend
npm install
npm run dev


Frontend runs at:

http://localhost:8080

🧠 Backend Setup (Federated Learning)
Install Dependencies
cd backend
pip install flwr torch pandas opacus

Network Configuration

Find Server IP

Windows: ipconfig

Mac/Linux: ifconfig

Update in client.py:

SERVER_IP = "192.168.x.x"


Ensure port 8888 is open in the firewall.

🚦 Execution Guide
Step 1: Start the Global Server
python server.py


Acts as the global coordinator

Waits for minimum 3 clients

Step 2: Start Bank Clients

On each bank laptop:

python client.py


✔ Each client:

Uses its own local dataset

Trains locally

Sends only privacy-preserving updates

📊 Technical Specifications
Component	Implementation
Framework	Flower (flwr)
Privacy Engine	Opacus (DP-SGD)
Model	FinancialBrain (Neural Network)
Loss Function	MSELoss
Optimizer	Adam + FedProx
Privacy Budget	ε = 1.1, δ = 10⁻⁵
Aggregation	FedProx
🛡️ Security & Privacy Disclaimer

❌ No raw transaction data is transmitted

❌ No centralized storage of sensitive data

✔ Only clipped, noised gradients are shared

✔ Resistant to inversion & membership attacks

This system is designed with privacy-by-design principles and aligns with financial data compliance requirements.

🔮 Future Enhancements

Real-time fraud alerts on dashboard

Blockchain-based audit trails

Secure authentication for banks

Deployment on cloud federated clusters

👩‍💻 Author

Pranathi P K, Ragul P, Reena Evelin J, Rohith g
B.Tech Information Technology, Dr.N.G.P. Institute of Technology
BS Data Science – IIT Madras
