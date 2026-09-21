# IT Incident Assistant

> 🏆 **2nd Place — IT Incident Track, 2026 TSMC Hackathon**

**IT Incident Assistant** is an AI-powered incident management system designed to help engineering teams handle IT incidents more efficiently.

The system integrates **Discord, Gemini on Vertex AI, internal engineering data, historical incident reports, external knowledge retrieval, and Google Calendar** to support incident analysis, documentation, and team coordination.

Developed for the **2026 TSMC Hackathon**, where our team received **2nd Place in the IT Incident Track**.

---

## Features

### 🤖 IT Incident Assistant

- **Real-time Discussion Summarization**  
  Summarizes ongoing Discord discussions and extracts key incident information.

- **Incident Analysis**  
  Analyzes the scope of impact, possible causes, mitigation strategies, and potential improvements.

- **Multi-source Knowledge Retrieval**  
  Retrieves relevant information from Discord messages, source code, system logs, and historical incident reports.

- **Historical Incident Search**  
  Uses embedding-based retrieval to find similar previous incidents and provide additional context for analysis.

- **External Knowledge Retrieval**  
  Searches external technical resources for troubleshooting, prevention, and code improvement suggestions.

- **Automatic Incident Reports**  
  Generates structured reports containing incident summaries, impact analysis, detected problems, solutions, and future improvements.

- **Incident Visualization**  
  Displays incident reports and visualizes how different teams or departments may contribute to similar incidents.

### 📅 Calendar Assistant

- **Availability Checking**  
  Checks individual members' availability through Google Calendar.

- **Group Meeting Scheduling**  
  Finds common available time slots across multiple participants.

- **Participant Management**  
  Adds relevant users to Discord incident channels when additional expertise is needed.

- **Automatic Notifications**  
  Sends Discord notifications to newly added participants.

---

## Project Structure

```text
IT_Incident_Agent/
├── backend/
│   ├── app/
│   │   ├── api/
│   │   ├── services/
│   │   ├── tools/
│   │   ├── main.py
│   │   ├── models.py
│   │   ├── schemas.py
│   │   └── database.py
│   ├── alembic/
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── requirements.txt
│   └── .env.example
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── Dockerfile
│   ├── package.json
│   └── .env.example
│
└── README.md
```

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/sjtseng0924/IT_Incident_Agent.git
cd IT_Incident_Agent
```

### 2. Configure the Backend

```bash
cd backend
cp .env.example .env
```

### 3. Start the Backend

The backend and PostgreSQL database can be started with Docker Compose:

```bash
docker compose up --build
```

```

### 4. Start the Frontend

Open another terminal:

```bash
cd frontend
npm install
npm run dev
```

Vite will display the local development URL in the terminal.

---

## How It Works

Engineers interact with the assistant directly through Discord.

During an incident, the agent can retrieve relevant discussions, code, logs, and historical reports to understand the current situation. It then assists with incident analysis and mitigation suggestions.

Once the incident is resolved, the assistant can automatically generate a structured incident report and store it for future retrieval.

For team coordination, the Calendar Assistant connects to Google Calendar through n8n to check availability, find common meeting times, and notify participants through Discord.

---

## Incident Report

Generated incident reports can include:

- Basic Information
- Discussion Summary
- Scope of Impact
- Problem Detection
- Solution
- Future Improvements

The reports are stored in the database and can be displayed through the web interface, turning temporary incident discussions into reusable organizational knowledge.

---

