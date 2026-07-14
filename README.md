![n8n](https://img.shields.io/badge/n8n-Automation-orange)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT-green)
![Loveable](https://img.shields.io/badge/Loveable-Frontend-blue)
![Google Workspace](https://img.shields.io/badge/Google-Workspace-red)

# 🤖 AI Personal Assistant using n8n

An AI-powered Personal Assistant built with **n8n**, **OpenAI**, and a **Loveable chat interface**.

Users interact with the assistant through a modern web-based chat UI built in Loveable. Every message is sent to an n8n Webhook, where an AI Agent processes the request, uses connected tools (Gmail, Google Calendar, Google Docs, Google Tasks, Google Sheets, etc.), and returns the response back to the chat interface in real time.

## 🏗 Architecture

```
┌─────────────────────────┐
│     Loveable Chat UI    │
└─────────────┬───────────┘
              │
        POST Request
              │
              ▼
      n8n Webhook Trigger
              │
              ▼
          AI Agent
              │
 ┌────────────┼────────────┐
 │            │            │
 ▼            ▼            ▼
OpenAI     Memory       Calculator
 │
 ├──────── Gmail
 ├──────── Google Calendar
 ├──────── Google Docs
 ├──────── Google Tasks
 └──────── Google Sheets
              │
              ▼
      Respond to Webhook
              │
              ▼
     Loveable Chat UI
```

## ✨ Features

- 💬 Modern chat interface built with Loveable
- ⚡ Real-time communication using n8n Webhooks
- 🤖 AI-powered conversations with OpenAI
- 🧠 Context-aware responses using memory
- 📧 Read, summarize, and send emails
- 📅 Create and manage calendar events
- ✅ Manage Google Tasks
- 📝 Create and update Google Docs
- 💰 Track personal expenses
- 🧮 Perform calculations
- 🔄 Responses are streamed back to the chat interface


## 🛠 Tech Stack

- n8n
- OpenAI
- Loveable
- Gmail API
- Google Calendar API
- Google Docs API
- Google Tasks API
- Google Sheets API

---

## 📋 Supported Commands

### Ask Questions

- Explain APIs
- What is RAG?
- Summarize this concept

### Calendar

- Schedule a meeting tomorrow at 3 PM
- Show today's events

### Gmail

- Read my latest emails
- Summarize unread emails
- Send an email

### Tasks

- Create a task
- Update a task
- Delete a task
- Show pending tasks

### Notes

- Create meeting notes
- Read notes
- Update notes

### Expenses

- Add a new expense
- Show expense history
- Track monthly spending

---

## 🚀 Setup

1. Clone this repository.
2. Import `workflow.json` into n8n.
3. Configure your credentials:
   - OpenAI
   - Gmail
   - Google Calendar
   - Google Docs
   - Google Tasks
   - Google Sheets
4. Activate the workflow.
5. Connect your Loveable frontend to the webhook endpoint.
6. Start chatting with your AI Personal Assistant.

---

## 🔮 Future Improvements

- Voice Assistant
- WhatsApp Integration
- Telegram Integration
- MCP Support
- RAG Knowledge Base
- Multi-Agent Architecture
