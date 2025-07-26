# 📅 AI-Powered Meeting Room Booking Workflow (n8n)

This repository contains a fully automated **meeting room booking workflow** built using [n8n](https://n8n.io/), powered by OpenAI and integrated with Slack, Gmail, and Google Calendar.

---

![Workflow Screenshot](./workflow-screenshot.png)

---

## 🧠 Features

- 📝 Accepts natural language input for meeting scheduling
- 🧠 Uses OpenAI GPT to classify and process requests
- ✅ Automatically drafts a booking email with structured JSON
- 💬 Sends messages to Slack for approval
- 📧 Sends confirmation emails via Gmail
- 📆 Creates events in Google Calendar upon approval

---

## 🔧 Required Integrations

To run this workflow, you need active API credentials set up in n8n for the following:

- ✅ OpenAI API
- ✅ Slack OAuth2
- ✅ Gmail OAuth2
- ✅ Google Calendar OAuth2

---

## 📥 How to Use

### 1. Import the Workflow into n8n

- Click **"Import"** in the top right of the n8n editor
- Select the `meeting_room_booking_workflow_scrubbed.json` file

### 2. Set Up Your Credentials

- Go to **n8n → Credentials**
- Create credentials for:
  - OpenAI
  - Slack OAuth2
  - Gmail OAuth2
  - Google Calendar OAuth2

### 3. Start the Workflow

You can start the workflow via a trigger (Webhook, chat input, etc.):

**Example Input:**

```
Book a meeting room on July 30th from 2 PM to 3 PM.
```

---

## 🔁 Workflow Flow

1. Message is received with meeting request
2. OpenAI classifies the intent and generates a booking email
3. Slack message is sent for approval
4. If approved:
   - Email is sent via Gmail
   - Google Calendar event is created
5. If rejected:
   - Slack notification sent

---

## 🧪 Future Improvements

- Add database logging (Airtable, Notion, Supabase)
- Integrate with Zoom or Microsoft Teams
- Add real-time calendar availability check

---

## 📁 Repository Structure

```
n8n-meeting-room-booking/
├── meeting_room_booking_workflow_scrubbed.json
├── workflow-screenshot.png
├── README.md
```

---

## 👩‍💻 Created By

**Prerna Kosta**  
Built with ❤️ using [n8n](https://n8n.io) and [OpenAI](https://platform.openai.com)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
