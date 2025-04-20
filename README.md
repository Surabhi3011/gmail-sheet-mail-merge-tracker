# 📬 Gmail + Google Sheets Mail Merge with Open Tracking

This project lets you send **personalized emails in bulk** using Gmail drafts and Google Sheets — with built-in:
- 📅 Scheduled delivery
- 👁️ Open tracking (via pixel)
- 📎 Attachments from Google Drive
- 📈 Status updates + reporting

---

## 🚀 Use Cases

- Invite emails for art/GIS workshops
- Networking emails with personalization
- Follow-up campaigns with status tracking

---

## 💡 Features

✅ Send emails using Gmail drafts  
✅ Schedule emails via Google Sheets  
✅ Track if the recipient opened the email  
✅ Add attachments from Google Drive  
✅ Logs all activity in your sheet  
✅ No 3rd-party tools, no coding required

---

## 🔧 How It Works

1. You fill a Google Sheet with:
   - Name, Email, Draft Subject, Attachment URL
2. You write a Gmail **Draft** using `{{Name}}` as placeholder
3. The script:
   - Pulls the draft
   - Adds a unique tracking pixel
   - Sends the email on schedule
   - Logs "Sent" and "Opened" in the Sheet

---

## 📄 Sheet Format

| Email | Name | Draft Subject | Attachment (Drive URL) | Status | Opened |
|-------|------|----------------|--------------------------|--------|--------|

- `Status` auto-updates to `Sent`, `Draft Not Found`, or `Attachment Error`
- `Opened` auto-updates when the recipient opens the email

---

## 🛠️ Setup Instructions

### 1. Copy the Google Sheet  
Create a Google Sheet with the above headers.

### 2. Open Apps Script (`Extensions > Apps Script`)  
Add two script files:

- `CODE.gs` → Paste the main logic (email + scheduler)
- `WEBAPP.gs` → Paste the open tracker script

### 3. Deploy the Web App (for open tracking)

- Go to **Deploy > Manage deployments**
- Choose **Web App**
- Execute as: `Me`
- Access: `Anyone`
- Copy the URL and paste it in `WEB_APP_URL` in your code

### 4. Add a time-driven trigger

- From Apps Script → `Triggers`
- Run: `scheduleEmails`
- Type: Time-driven
- Every 5 minutes

---

## 📊 Generating Reports

You can use a helper function to export a `.txt` or `.pdf` status report from your sheet (see `generatePDFReport()` in code).

---

## 📸 Screenshots (optional)
You can add screenshots of:
- Gmail draft
- Sheet structure
- Status updating
- Deployment panel

---

## 📝 License

MIT License — you’re free to reuse, customize, and share.

---

## Disclaimer

This project was created using ChatGPT LLM completely.

## ✨ Created by

**Surabhi Gupta**  
https://geocloudinsights.substack.com/
https://www.linkedin.com/in/surabhiguptageo/

