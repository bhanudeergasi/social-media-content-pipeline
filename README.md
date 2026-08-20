# AI-Powered Social Media Content Automation

An n8n-based AI automation workflow that converts a natural-language content brief into platform-specific social media content for **LinkedIn, X/Twitter, and Instagram**, with a human approval workflow through Telegram.

## 🚀 What It Does

The workflow automates the complete content creation and approval process:

```text
Telegram Brief
      ↓
AI Content Generation
      ↓
LinkedIn + X/Twitter + Instagram
      ↓
Draft Storage
      ↓
Telegram Review
      ↓
[ APPROVE ]
      ↓
Google Sheets Publishing Calendar
      ↓
Telegram Confirmation

```
## ✨ Key Features

- 📝 Accepts natural-language content briefs through Telegram
- 🤖 Generates platform-specific content using Groq LLM
- 💼 Creates LinkedIn posts
- 🐦 Generates X/Twitter threads
- 📸 Generates Instagram captions
- 📦 Uses structured JSON output for reliable processing
- 💾 Stores drafts and approval status in an n8n Data Table
- ✅ Provides one-click approval through Telegram
- 🔒 Prevents already-approved drafts from being processed again
- 📅 Adds approved content to a Google Sheets publishing calendar
- 🔔 Sends confirmation to Telegram after successful approval
- ⚠️ Handles AI failures and preserves the original brief
```text
Telegram
   ↓
n8n
   ↓
Groq LLM
   ↓
Structured Output
   ↓
Data Table
   ↓
Telegram Approval
   ↓
Callback Validation
   ↓
Google Sheets
   ↓
Telegram Confirmation
```
AI failures follow a separate path:
```
Groq LLM
   ↓
Error
   ↓
Telegram Error Message
   ↓
Original Brief Preserved
```
## 🛠️ Tech Stack
- Technology	Purpose
- n8n	Workflow automation
- Telegram Bot API	User interaction & approval
- Groq	AI content generation
- LLM	Platform-specific content creation
- n8n Data Tables	Draft & status management
- Google Sheets	Publishing calendar
- 📊 Draft Status Flow
    pending → approved

The approval flow validates the current status before updating the record, helping prevent duplicate processing.

## 🧪 Tested
- Telegram message reception
- AI content generation
- Structured output
- Multi-platform content creation
- Draft storage
- Telegram approval
- Callback processing
- Duplicate approval protection
- Google Sheets integration
- Scheduled date
- Telegram confirmation
- AI failure handling
- 🔐 Security

API credentials are stored using n8n credentials and are not committed to the repository.

## 🔮 Future Improvements
- Automatic publishing to social media platforms
- User-selected publishing dates
- Content editing before approval
- Content regeneration
- Publishing analytics
- Performance-based content optimization
  
👩‍💻 Author
Bhanu Deergasi
