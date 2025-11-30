# 🧠 AI Daily Task Agent  
A multi-agent AI system that helps users manage their daily tasks through intelligent task intake, prioritization, scheduling, and summarization.

---

## 🌟 Overview  
The **AI Daily Task Agent** is a lightweight, modular multi-agent system designed to automate daily task planning.  
Users can input natural-language tasks (ex: *“Finish project report in the morning for 1 hour”*), and the system automatically:

1. **Parses and stores the task**  
2. **Assigns priority based on urgency and duration**  
3. **Builds a smart schedule starting from 9 AM**  
4. **Generates a human-readable daily summary**

This system demonstrates multi-agent orchestration, state management, and simple automation — perfect for beginners learning agent workflows.

---

## 🚀 Features

### ✔ **1. Multi-Agent Architecture**
- **Intake Agent** → Understands user task input  
- **Priority Agent** → Scores tasks using a rule-based system  
- **Scheduler Agent** → Assigns time slots automatically  
- **Summary Agent** → Generates a clean daily summary  

### ✔ **2. State / Memory System**
- Tasks are stored in a lightweight JSON memory bank  
- Persistent across agent calls  

### ✔ **3. End-to-End Orchestration**
A single pipeline orchestrates all agents:

### ✔ **4. Fully Modular**
Each agent is independent and testable.

---

## 🏗 Project Architecture
    ┌────────────┐
    │ User Input │
    └──────┬─────┘
           ▼
    ┌──────────────┐
    │ Intake Agent │
    └──────┬───────┘
           ▼
    ┌────────────────┐
    │ Priority Agent │
    └──────┬─────────┘
           ▼
    ┌────────────────┐
    │ Scheduler Agent │
    └──────┬─────────┘
           ▼
    ┌────────────────┐
    │ Summary Agent  │
    └────────────────┘


### **Agent Workflow Diagram:**
    ┌────────────┐
    │ User Input │
    └──────┬─────┘
           ▼
    ┌──────────────┐
    │ Intake Agent │
    └──────┬───────┘
           ▼
    ┌────────────────┐
    │ Priority Agent │
    └──────┬─────────┘
           ▼
    ┌────────────────┐
    │ Scheduler Agent │
    └──────┬─────────┘
           ▼
    ┌────────────────┐
    │ Summary Agent  │
    └────────────────┘

---

## 📁 Folder Structure

final_ai_daily_agent/
│── agents/
│ ├── intake_agent.py
│ ├── priority_agent.py
│ ├── scheduler_agent.py
│ └── summary_agent.py
│
│── memory/
│ ├── memory_bank.py
│ └── tasks.json
│
│── tools/
│ └── task_storage_tool.py
│
│── tests/
│ └── test_integration.py
│
│── main.py
│── requirements.txt
│── README.md

---

## 🧩 Core Agents

### **Intake Agent**
Extracts:
- task name  
- duration  
- urgency (high/medium/low)

### **Priority Agent**
Adds a **priority score** based on:
- urgency  
- duration  
- short tasks = bonus  

### **Scheduler Agent**
Schedules tasks starting from **9:00 AM**.

### **Summary Agent**
Outputs clean formatted summary.

---

## ⚙️ Installation & Running

### **1. Create Virtual Environment**
```bash
python -m venv venv

2. Activate
.\venv\Scripts\activate

3. Install Dependencies
pip install -r requirements.txt

4. Run Project
python main.py demo

5.INPUT
 Finish ML assignment tomorrow 3 hours 
 Buy groceries today 30 min 
 Call team at 4pm today 30 min 
 Finish ML assignment tomorrow 3 hours 
 Buy groceries today 30 min

6.OUTPUT

| Component | Technology                   |
| --------- | ---------------------------- |
| Language  | Python 3.12                  |
| Framework | No ML framework — rule-based |
| Memory    | JSON local store             |
| Modules   | datetime, uuid, json         |
| Testing   | pytest                       |

🧭 Future Enhancements
Natural Language Processing (NLP) for better task understanding
Calendar integration (Google Calendar API)
Web UI dashboard
User preferences & profiles
Better schedule optimization







[output of AI daily task agent.pdf](https://github.com/user-attachments/files/23840824/output.of.AI.daily.task.agent.pdf)
