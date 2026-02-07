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

👩‍💻 Author

Pranathi P K, Ragul P, Reena Evelin J, Rohith g
B.Tech Information Technology, Dr.N.G.P. Institute of Technology
BS Data Science – IIT Madras
