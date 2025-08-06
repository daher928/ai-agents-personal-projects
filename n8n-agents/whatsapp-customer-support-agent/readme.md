# 🧠 WhatsApp Memory Agent – n8n Workflow

An AI-powered memory agent built in [n8n](https://n8n.io), designed to respond to WhatsApp messages with personalized, context-aware replies. It integrates Supabase for memory, OpenAI for reasoning and transcription, and Postgres for session memory.

---

## 🔧 Features

- 📲 WhatsApp Cloud API integration
- 🧠 Memory management via Supabase (`get`, `create`, `delete`)
- 🤖 Dual-agent system:
  - **Memory Picker** – backend memory processor
  - **Andrew (Know it all)** – main assistant persona
- 💬 Chat context stored in Postgres
- 📚 Document-based knowledge (Supabase vector store)
- 🎙️ Voice message support with transcription
- 🌍 Arabic prompt instructions (Palestinian dialect)

---

## ⚙️ Tech Stack

| Feature             | Tool                    |
|---------------------|-------------------------|
| Messaging           | WhatsApp Business API   |
| AI Model            | OpenAI GPT‑4o‑mini      |
| Memory DB           | Supabase                |
| Context Memory      | Postgres                |
| Vector Retrieval    | Supabase (RAG)          |
| Orchestration       | n8n workflow            |

---

## 🧩 Key Nodes

- `WhatsApp Trigger`: Incoming message entry
- `Memory Picker`: Retrieves/saves/deletes user memories
- `Know it all`: Responds with personalized, human-like messages
- `Supabase Tools`: Access `Memory` table
- `Postgres Chat Memory`: Maintains session context
- `OpenAI`: Transcribes audio messages

---

## 🔐 Credentials (Required)

Make sure these are configured in your n8n instance:

- OpenAI
- Supabase
- WhatsApp API
- Postgres

Only references (`id`, `name`) are in the JSON – **no secrets are exposed**.

---

## 🚀 Setup Steps

1. Import the workflow into n8n
2. Set up credentials under “Credentials” tab
3. Link your WhatsApp Business App to the webhook
4. Test the agent by messaging from a real WhatsApp number

---

## 👥 Use Cases

- Personal memory bots
- Arabic-language business assistants
- Long-term conversational agents
- Audio-to-text WhatsApp workflows

---

Built with ❤️ & 🧠 by Daher
