# 🩺 AI Voice Health Chatbot — Doctor Appointment Booking System  
### 🤖 Built with n8n · Vapi Voice Agent · Google Gemini · Google Workspace

---

## 🚀 Overview

This project is an **AI-powered voice assistant** that interacts with patients, collects symptoms, performs triage, and automatically books **doctor appointments** — all using conversational AI and workflow automation.

It integrates **voice AI**, **LLMs**, and **n8n** automation to streamline patient intake, triage, and scheduling, saving healthcare providers time while improving patient experience.

---

## 🧠 Features

✅ **Voice or Chat Interface (Vapi Integration)**  
Patients can talk naturally — the voice agent listens, understands, and records their health concerns.

✅ **AI Triage & Symptom Analysis**  
Uses **Google Gemini (LLM)** to classify symptoms, assess urgency, and recommend the next step.

✅ **Automated Doctor Appointment Booking**  
Schedules appointments in **Google Calendar** and logs data in **Google Sheets**.

✅ **Notifications & Alerts**  
Sends confirmation via **WhatsApp** or **Email**, and urgent case alerts to the medical team.

✅ **Structured Data Flow**  
Uses n8n’s **Webhook**, **Code**, **Switch**, and **HTTP Nodes** for end-to-end logic and structured JSON output.

---

## 🧩 Tech Stack

| Component | Description |
|------------|-------------|
| **n8n Cloud** | Workflow automation & orchestration |
| **Vapi.ai** | Voice Agent API for real-time patient interaction |
| **Google Gemini / OpenAI** | Large Language Model for triage and decision logic |
| **Google Calendar API** | Doctor scheduling and appointment booking |
| **Google Sheets API** | Patient record & schedule tracking |
| **Gmail / WhatsApp API** | Notification and alert system |

---

## ⚙️ Workflow Architecture

### 🩺 Triage Agent (Patient Intake)
1. **Webhook Node** — receives data from the Vapi voice call  
2. **LLM Node (Gemini Chat)** — analyzes symptoms and urgency  
3. **Structured Output Parser** — formats triage data (name, age, symptoms, urgency)  
4. **Switch Node** — decides whether to:
   - Book appointment  
   - Send alert for urgent cases  
   - Generate wellness plan  

### 🗓️ Appointment Booking
1. **Doctor Appointment Node** — creates calendar event  
2. **Google Sheets Node** — logs patient data  
3. **Gmail Node** — sends confirmation email  
4. **WhatsApp / Twilio Node** — sends SMS confirmation  

### 🛠️ Response
- Responds back to Vapi webhook with confirmation message  
- Workflow execution ends after success/failure log  

---

## 🧾 Example JSON Output (Structured Data)
```json
{
  "type": "appointment_booking",
  "data": {
    "patient": {
      "name": "Sara Malik",
      "age": 35,
      "symptoms": ["fever", "fatigue", "joint pain"],
      "duration": "2 days"
    },
    "triage_level": "moderate",
    "appointment": {
      "doctor": "Dr. Ahmed",
      "department": "Internal Medicine",
      "date": "2025-11-02T15:00:00Z"
    },
    "notifications": {
      "email": "sent",
      "whatsapp": "sent"
    }
  }
}
🧰 Setup Guide
Prerequisites


n8n Cloud


Vapi.ai


Google Cloud Console (for Calendar, Sheets, Gmail APIs)


API key for Google Gemini or OpenAI


(Optional) WhatsApp / Twilio credentials


Steps


Import the n8n Workflow JSON


Open n8n → Import → Paste or upload your workflow file.




Configure Environment Variables
GOOGLE_API_KEY=
GEMINI_API_KEY=
VAPI_API_KEY=
TWILIO_API_KEY=



Set up Google Workspace APIs


Enable Calendar, Sheets, and Gmail APIs in your Google Cloud Project.


Use OAuth credentials for n8n connections.




Connect Voice Agent


In Vapi, set your webhook URL from n8n (e.g. https://your-instance.n8n.cloud/webhook/triage-agent)


Configure assistant prompt for symptom collection and booking.




Deploy and Test


Make a test voice call → data flows into n8n → AI triage → appointment booked → confirmation sent.





🧪 Example Prompts
🗣️ Voice Agent System Prompt
You are a healthcare triage assistant. Collect patient details including:
- Name
- Age
- Symptoms and duration
- Preferred date/time for appointment

Respond conversationally and pass structured data to the webhook.

🤖 LLM Prompt (Triage Node)
Analyze the patient's symptoms and classify the urgency as:
- mild
- moderate
- urgent

Output structured JSON with triage level and suggested action.


📦 Future Enhancements


Multi-language support (English, Urdu, Arabic)


EHR/CRM integration


Doctor availability optimization


Patient follow-up reminders


HIPAA-compliant deployment



🧑‍💻 Author
Madeeha Tassadaq
AI Automation Engineer | n8n Workflow Builder | Voicebot Developer
🌐 Upwork Profile | 💬 LinkedIn | 📧 madeeha@example.com

🪄 License
This project is licensed under the MIT License — free to use, modify, and distribute with attribution.


⚡ Automating healthcare one conversation at a time.


---

Would you like me to also create a **short version of this README** (for GitHub front-page summary with visuals and badges) — e.g., with emojis, a project banner, and shield.io badges?  
That makes it look more professional and eye-catching for recruiters or clients.

