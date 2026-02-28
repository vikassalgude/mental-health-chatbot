

# 🛡️  AI Mental Health Chatbot

It is an AI-powered mental health companion designed to support students experiencing stress, anxiety, and loneliness. Built with healthcare-specialized AI and a privacy-first architecture, SafeSpace provides empathetic conversations, intelligent agentic workflows, and critical crisis intervention support.

---

## 🌟 Overview

SafeSpace leverages healthcare-tuned large language models and agent-based decision systems to:

* Detect emotional distress using sentiment analysis
* Provide empathetic and science-backed responses
* Offer motivational support
* Trigger emergency interventions when high-risk distress is detected

The system prioritizes **privacy, safety, and accessibility**.

---

## 🚀 Key Features

### 🤖 Empathetic AI Chatbot

* Powered by **Google MedGemma** (healthcare-specialized LLM family)
* Provides compassionate, evidence-based support
* Designed specifically for mental health use cases

### 🚨 Crisis Intervention

* Integrated with **Twilio**
* Automatically initiates emergency phone calls during high-risk situations
* Designed for real-time safety escalation

### 🧠 Agentic Workflow

* Built using **LangGraph** and **LangChain**
* AI agent "thinks" before acting
* Dynamically selects tools such as:

  * Emergency Call Tool
  * Ask Expert Tool
  * Find Therapist Tool

### 🔒 Privacy-First Architecture

* Runs local models via **Ollama**
* Sensitive student data remains on-device
* Minimal external data exposure

---

## 🛠️ Technical Stack

| Layer                   | Technology                                               |
| ----------------------- | -------------------------------------------------------- |
| **LLM Core**            | MedGemma (Healthcare-specialized model family by Google) |
| **AI Frameworks**       | LangGraph + LangChain                                    |
| **Backend**             | FastAPI                                                  |
| **Frontend**            | Streamlit                                                |
| **Local Model Serving** | Ollama                                                   |
| **Communication API**   | Twilio                                                   |

---

## 🏗️ System Architecture

SafeSpace follows a modular, agent-driven architecture:

### 1️⃣ User Input

* Student interacts through the Streamlit frontend
* Inputs emotional state, concerns, or distress signals

### 2️⃣ API Routing

* FastAPI handles request validation
* Securely forwards request to the AI agent layer

### 3️⃣ Intelligence Layer

* LangGraph agent processes input
* MedGemma (via Ollama or Groq) performs:

  * Sentiment analysis
  * Risk assessment
  * Context reasoning

### 4️⃣ Action / Tool Selection

Based on risk detection:

| Condition         | Action                                  |
| ----------------- | --------------------------------------- |
| Mild Stress       | Empathetic response + coping strategies |
| Moderate Distress | Suggest therapist resources             |
| High-Risk Crisis  | Trigger Twilio emergency call           |
| Medical Question  | Ask Expert Tool                         |

---

## 📦 Installation & Setup

### 🔧 Prerequisites

* Python 3.10+
* Ollama installed
* Twilio account (for crisis calling)
* Virtual environment recommended

---

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/safespace-ai.git
cd safespace-ai
```

---

### 2️⃣ Setup Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Run Ollama with MedGemma

```bash
ollama pull medgemma
ollama run medgemma
```

---

### 5️⃣ Configure Environment Variables

Create a `.env` file:

```
TWILIO_ACCOUNT_SID=your_sid
TWILIO_AUTH_TOKEN=your_token
TWILIO_PHONE_NUMBER=your_twilio_number
```

---

### 6️⃣ Start Backend

```bash
uvicorn main:app --reload
```

---

### 7️⃣ Start Frontend

```bash
streamlit run app.py
```

---

## 🧠 Agentic Workflow Logic

The AI Agent operates as follows:

1. Analyze sentiment
2. Classify risk level
3. Select appropriate tool
4. Generate empathetic response
5. Log safely (if enabled)
6. Escalate when necessary

The system ensures:

* No unnecessary emergency triggers
* Ethical decision boundaries
* Responsible AI interaction design

---

## 🛡️ Safety & Ethics

SafeSpace is designed with:

* Human-centered AI principles
* Crisis detection safeguards
* Minimal data retention
* Transparent intervention logic

⚠️ Disclaimer: SafeSpace is a support tool and not a replacement for licensed medical professionals.

---

## 🗺️ Implementation Roadmap

### Phase 1: Frontend Setup

* Initialize Streamlit interface
* Enable real-time chat display
* Implement session state management

### Phase 2: Backend Development

* Setup FastAPI
* Implement secure routing
* Input validation & sanitization

### Phase 3: AI Agent & Tool Integration

* Configure Ollama with MedGemma
* Integrate Twilio emergency API
* Develop location-based therapist finder
* Connect LangGraph agent to backend logic

### Phase 4: Full System Integration

* End-to-end workflow testing
* Crisis trigger validation
* Performance optimization
* Security audit

---

## 📌 Future Improvements

* Multilingual emotional support
* Voice-based AI interaction
* University-specific therapist directory
* HIPAA-compliant cloud deployment
* Real-time emotion detection via speech

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss proposed updates.

---

## 📄 License

MIT License

---

If you'd like, I can also:

* Create a **GitHub-ready badge version**
* Generate a **system architecture diagram**
* Provide a **folder structure template**
* Or prepare a **pitch deck version** for investors**
