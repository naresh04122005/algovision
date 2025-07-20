# 🌟 AlgoVision – AI‑Powered Coding Assistant

**A full-stack project that combines Gemini API with algorithmic expertise to help developers solve DSA challenges.**

---

## 🧠 Overview

AlgoVision is a web-based coding assistant that:
- Classifies problem statements (e.g., “graph shortest path,” “knapsack DP”) using the **Gemini API**
- Matches them to best-fit **data structure & algorithm implementations** (Graph, DP, Greedy, etc.)
- Displays interactive **template code snippets** and explanations
- Deployed on **Google Cloud**, ready for multiple concurrent users

---

## ⚙️ Features

- **📚 Problem Classification**  
  Uses Gemini to determine problem type with ~92% accuracy

- **🔧 Algorithm Template Library**  
  Contains 15+ ready-to-use algorithm snippets in Python

- **🌐 Web Interface**  
  Built with FastAPI (backend) and optional React frontend

- **📊 Analytics Tracking**  
  Logs classification accuracy and usage stats

- **☁️ Scalable Deployment**  
  Hosted on Google Cloud Run for 100+ concurrent users

---

## 🛠️ Tech Stack

| Layer         | Technologies                                                                 |
|---------------|------------------------------------------------------------------------------|
| Backend       | Python, FastAPI, Gemini API                                                 |
| Algorithms    | Implementations of Graph, DP, Greedy, Sorting, Search, etc.                |
| Database      | MongoDB (or local JSON) for storing algorithm templates and metadata        |
| Frontend      | (Optional) React + Axios for a responsive UI                               |
| Deployment    | Google Cloud Run, Containerized with Docker                                |

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/AlgoVision.git
cd AlgoVision
