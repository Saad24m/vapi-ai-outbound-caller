# Vapi AI Outbound Caller & GoHighLevel CRM Automation n8n Workflow

An advanced, bidirectional n8n integration workflow that handles real-time webhooks from **Vapi.ai** voice agents, parses structured tool calls, synchronizes leads with **GoHighLevel (GHL)**, checks calendar availability, and books appointments automatically.

---

## 🚀 What This Workflow Does

1. **Webhook Trigger:** Receives real-time call event data and tool calls from Vapi.ai voice agents.
2. **Dynamic Routing (`Switch` Node):** Directs incoming payloads based on the specific action requested by the AI agent (e.g., checking slot availability, handling voicemails/callback times, updating strategy call interests, or booking appointments)[cite: 8].
3. **Calendar Availability (`Get free slots of a calendar`):** Queries HighLevel calendar slots dynamically based on the requested date and responds back via webhook to the AI agent[cite: 8].
4. **CRM Contact & Custom Fields Management:** Searches for existing contacts by phone number in HighLevel, creates or updates them, and populates custom lead data (like budget, decision-maker status, and company info)[cite: 8].
5. **Automated Appointment Booking:** Books confirmed appointments directly inside HighLevel calendars and triggers corresponding success/failure responses to the voice agent[cite: 8].

---

## 🛠️ Prerequisites & Credentials

* **Vapi.ai Account & Webhook Endpoint**
* **GoHighLevel (GHL) OAuth2 API / Bearer Token**

---

## ⚙️ How to Use

1. Import the cleaned `vapi-ai-outbound-caller.json` workflow into your **n8n** instance[cite: 8].
2. Configure your **HighLevel** credentials and map your custom field IDs / calendar IDs[cite: 8].
3. Set your active Vapi.ai assistant and phone number IDs[cite: 8].
4. Activate the webhook URL and link it inside your Vapi.ai agent settings[cite: 8].
