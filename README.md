# AlgoVision – AI‑Powered Coding Assistant

**A full-stack project that combines Gemini API with algorithmic expertise to help developers solve DSA challenges.**

---

## Overview

AlgoVision is a web-based coding assistant that:
- Classifies problem statements (e.g., “graph shortest path,” “knapsack DP”) using the **Gemini API**
- Matches them to best-fit **data structure & algorithm implementations** (Graph, DP, Greedy, etc.)
- Displays interactive **template code snippets** and explanations
- Deployed on **Google Cloud**, ready for multiple concurrent users

---

## Features

- **Problem Classification**  
  Uses Gemini to determine problem type with ~92% accuracy

- **Algorithm Template Library**  
  Contains 15+ ready-to-use algorithm snippets in Python

- **Web Interface**  
  Built with FastAPI (backend) and optional React frontend

- **Analytics Tracking**  
  Logs classification accuracy and usage stats

- **Scalable Deployment**  
  Hosted on Google Cloud Run for 100+ concurrent users

---

## Tech Stack

| Layer         | Technologies                                                                 |
|---------------|------------------------------------------------------------------------------|
| Backend       | Python, FastAPI, Gemini API                                                 |
| Algorithms    | Implementations of Graph, DP, Greedy, Sorting, Search, etc.                |
| Database      | MongoDB (or local JSON) for storing algorithm templates and metadata        |
| Frontend      | (Optional) React + Axios for a responsive UI                               |
| Deployment    | Google Cloud Run, Containerized with Docker                                |

---

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/AlgoVision.git
cd AlgoVision

Installation
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Set environment variables in a .env file:

ini
Copy
Edit
GEMINI_API_KEY=your_gemini_key_here
GEMINI_MODEL=gemini-2.5-flash-preview
MONGODB_URI=mongodb://localhost:27017/algovision
Add algorithm templates in the algorithms/ directory.
Example JSON format:

json
Copy
Edit
{
  "name": "Dijkstra's Algorithm",
  "category": "Graph",
  "code": "def dijkstra(...): ...",
  "time_complexity": "O(E log V)"
}
Start the application:

bash
Copy
Edit
uvicorn app.main:app --reload
The app will be available at http://localhost:8000/

Usage
Open http://localhost:8000/ in your browser.

Enter a problem description, for example:
"Find the shortest path in an unweighted graph."

The app will:

Classify the problem (for example, Graph)

Provide the most suitable algorithm template

Display complexity and explanation

API Endpoints
Endpoint	Method	Description
/classify	GET	Classifies input and returns algorithm type
/snippet/{category}	GET	Returns code template for a given category
/stats	GET	Shows usage analytics and accuracy metrics

Running Tests
Run all tests with pytest:

bash
Copy
Edit
pytest tests/
Deployment on Google Cloud Run
Build Docker image:

bash
Copy
Edit
docker build -t algovision .
Push to Google Container Registry:

bash
Copy
Edit
docker tag algovision gcr.io/$GCP_PROJECT/algovision
docker push gcr.io/$GCP_PROJECT/algovision
Deploy:

bash
Copy
Edit
gcloud run deploy algovision \
  --image gcr.io/$GCP_PROJECT/algovision \
  --platform managed \
  --region YOUR_REGION \
  --allow-unauthenticated
Contributing
Fork this repository

Create a feature branch:

bash
Copy
Edit
git checkout -b feature/my-feature
Commit your changes:

bash
Copy
Edit
git commit -m "Add new feature"
Push to your branch and open a pull request.

Roadmap
Add additional algorithms (Backtracking, Heap, etc.)

Build a React-based frontend with live code execution

Support for multi-language snippets (Java, C++, Go)

Enhance analytics dashboard with real-time charts

Add CI/CD pipelines for testing and deployment

License
This project is licensed under the MIT License.
