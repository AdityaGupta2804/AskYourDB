# AskYourDB – Natural Language to SQL Converter

### Convert plain English queries into SQL statements using a locally hosted LLM and visualize results instantly

## Project Summary

AskYourDB is a smart web app that lets you **talk to your database using natural language**.

Imagine asking:
> _"Show me all users who signed up last month."_

And the app automatically converts that into a proper SQL query, runs it, and even **visualizes the result** using interactive charts.

No SQL experience? No problem.  
No internet? Still works — everything runs **locally on your system**.

---
## Project Demo
###  Query & Result Page  
![App Demo](/llama_git.gif)

### PyGWalker Visualization  
![Visualization](/pygwalker.jpg)


## Technical Overview 

This app combines:
- A **locally hosted LLM (Code Llama)** for converting natural language to SQL
- A **Flask backend** for query handling and model communication
- A dynamic **frontend UI** to interact with databases and visualize outputs using **PyGWalker**

It's designed to run **entirely offline**, using the `GGUF` format for optimized LLM inference on CPUs.

---

## Features

- **Natural Language → SQL** conversion via LLM
- **Multiple Database Selection**
- **Table Selection UI**
- **Editable SQL Queries**
- **Instant Data Visualization** with PyGWalker
- **Fully Local Deployment** (no cloud dependencies)
- **Model Swappable** (just change one line to try another LLM)

---

## Architecture Diagrams

## User Flow
![User Flow](/SQL.png)

## Tech Stack

| Layer          | Tech Used                                     | Description                          |
|----------------|-----------------------------------------------|--------------------------------------|
| LLM            | Code Llama 7B (GGUF - 5bit)                   | Converts text to SQL locally         |
| Backend        | Flask                                         | REST API, model handling             |
| Visualization  | PyGWalker                                     | Turns SQL results into charts/tables |
| Model Serving  | ctransformers                                 | Lightweight LLM runner on CPU        |
| UI             | HTML, CSS, JS                                 | Clean frontend with SQL editor       |
| Env Config     | Python dotenv                                 | Manage credentials and paths         |
| Database       | MySQl,SQLite,PostgreSQl                       | Manage Relational Database           |

---


---

## Installation Guide

```bash
# 1. Clone the repo
git clone https://github.com/raghujhts13/text-to-sql.git
cd text-to-sql

# 2. Install dependencies
pip install -r requirements.txt

# 3. Set up environment variables (in config/.env)
# FLASK_KEY = any random string
# MODEL_PATH = path to the downloaded GGUF model

# 4. Run the app
python app.py
```
> Visit the app at: http://127.0.0.1:5000

## Conclusion
This project turns a complex task like database querying into something as easy as chatting. It’s lightweight, fully offline, and customizable — ideal for analysts, devs, or anyone tired of writing boilerplate SQL.
## License
MIT License – free to use, modify, and distribute.

## Contributions
Pull requests, suggestions, and issues are always welcome!
Feel free to fork and build your own enhanced version.