# Prior Authorization Agent

A **Streamlit-based Prior Authorization agent** that uses **LLMs and LangGraph** to analyze prescriptions, patient EHR data, drug information, and insurance policy rules to generate automated prior authorization decisions.

---

## 🌐 Live Application

The application is deployed on Render and can be accessed here:

👉 https://prior-authorization-agent.onrender.com/

---

## 🚀 Overview

This application demonstrates a **multi-agent AI workflow** for automating prior authorization decisions in healthcare scenarios.

The system orchestrates multiple AI agents to:

* Parse prescription documents
* Evaluate patient EHR context
* Analyze drug information
* Apply insurance policy rules
* Produce a final authorization decision with reasoning

This project is intended as a **technical demonstration and prototype**.

---

## 🧠 Architecture

The application is built using **LangGraph** to coordinate multiple agents:

```
Prescription Parser
        |
        ├──> EHR Agent
        ├──> Drug Agent
        |
        └──> Policy Agent
                |
        Final Prior Authorization Decision
```

Each agent produces structured output that feeds into the final decision-making step.

---

## 🖥️ User Interface

* Built with **Streamlit**
* Sidebar-based document selection
* Real-time streaming of agent outputs
* Clear, color-coded decision summaries
* Dedicated **Settings page** for API key management
* Embedded demo walkthrough video

---

## 🔐 API Key Handling

* Users must provide their **OpenAI API key** on the Settings page
* The API key:

  * Is stored **only in Streamlit session memory**
  * Is **never written to disk**
  * Is automatically cleared when the session ends
* The application will not run without a valid API key

---

## 📂 Project Structure

```
.
├── app.py
├── pages/
│   └── 0_settings.py
├── nodes/
├── state_schema.py
├── prior_auth_prompt.py
├── structured_output.py
├── requirements.txt
├── render.yaml
├── .gitignore
└── .streamlit/
    └── config.toml
```

---

## ⚙️ Local Development

### 1. Clone the repository

```bash
git clone https://github.com/gesivak21/prior-auth-agent.git
cd prior-auth-agent
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the application

```bash
streamlit run app.py
```

---

## 📽️ Demo Video

A full demo walkthrough video is available here:

👉 https://gesivak21.github.io/MyPortfolio/projects/demo.html

The demo covers:

* Document selection
* Running the agent
* Interpreting authorization decisions

---

## ⚠️ Disclaimer

This project is provided **for demonstration and evaluation purposes only**.

* Not a medical device
* Not HIPAA compliant
* Not intended for use with real patient data
* Not intended for clinical or operational decision-making

---

## 🔒 Rights & Usage

All rights are reserved.

* No license is granted for reuse, redistribution, or modification
* Use of this codebase requires **explicit permission from the author**


