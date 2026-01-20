# AI-Email-Automation-Agent
Transform business email management with an intelligent AI agent that eliminates manual sorting and accelerates response times.

*Link demo:*
*[Billing Email Demo](https://youtu.be/8L0NR_yeIoU)*
*[Email Customer Support Demo](https://youtu.be/e-POJ1eO1fY)*

## 🎯 Problem Statement
Manual email management consumes valuable time and creates bottlenecks:
- ⏰ Hours spent sorting and categorizing emails
- 📧 Delayed responses to urgent customer queries
- 📄 Manual invoice processing and data entry
- 🗑️ Inbox cluttered with promotional emails

## 💡 Solution
An intelligent n8n workflow that automatically processes, categorizes, and responds to emails using AI agents with RAG capabilities.

## ✨ Key Features

### 1. *AI Customer Support Agent*
- Answers customer queries using RAG (Vector Database)
- Retrieves accurate information from your company knowledge base
- Generates contextual responses automatically

### 2. *Automated Invoice Processing (OCR)*
- Scans incoming invoices and extracts key data
- Automatically archives to Google Drive
- Updates Google Sheets for accounting records

### 3. *Smart Email Routing*
- Classifies email priority using AI
- Forwards high-priority emails to team via Email/WhatsApp/Telegram
- Instant notifications for urgent matters

### 4. *Zero-Noise Inbox*
- Auto-marks promotional/marketing emails as 'read'
- Keeps your inbox focused on important communications

## 🛠️ Tech Stack
- **Automation Platform**: n8n
- **AI Models**: OpenAI, Claude (Anthropic)
- **Vector Database**: Pinecone
- **OCR**: OCRspace API & Information Extractor
- **Integrations**: Gmail API, Google Drive, Google Sheets
- **Notifications**: Telegram/WhatsApp API

## 📊 Potential Impact
- ⚡ **80% faster** response time for customer queries
- 📉 **90% reduction** in manual email sorting
- 💰 **5+ hours saved** per day on email management
- ✅ **95% accuracy** on invoice data extraction

## 🚀 Quick Start
### Prerequisites
- n8n instance (self-hosted or cloud)
- Gmail account with API access
- OpenAI/Anthropic API key
- Pinecone account (for Vector Database)
- OCRspace API Key

### Installation

1. **Import workflow to n8n**
   - Open n8n
   - Go to Workflows → Import from File
   - Select `workflows/email-agent.json`

2. **Configure credentials**
   - Gmail OAuth2
   - OpenAI API Key
   - Pinecone API Key
   - Google Drive/Sheets credentials
   - OCRspace API Key

3. **Customize prompts**
   - Edit prompts in `prompts/` folder to match your business needs
   - Update vector database with your company knowledge

4. **Test the workflow**
   - Send test emails to verify each branch works correctly

📖 Detailed setup guide in `docs/setup.md`

## 📋 Workflow Components

| Component | Purpose | AI Model Used |
|-----------|---------|---------------|
| Text Classifier | Categorize incoming emails | GPT-5 mini / Claude |
| Customer Support Agent | Answer queries with RAG | GPT-5.2 + Pinecone |
| Invoice OCR | Extract billing data | OCRspace API |
| Priority Detector | Identify urgent emails | GPT-5.2 |

## 🎨 Customization

This workflow is designed to be flexible. You can:
- Add new email categories
- Customize AI prompts for your industry
- Integrate with different tools (Slack, Discord, etc.)
- Modify routing rules

## 📸 Screenshots

You can see in `assets/`

## 🔐 Security Notes

- Never commit API keys to the repository
- Use environment variables for sensitive data
- Enable OAuth2 for Gmail instead of app passwords
- Regularly rotate API credentials

## 🤝 Use Cases

This automation is perfect for:
- **E-commerce businesses** - Handle customer inquiries at scale
- **Service providers** - Automate appointment confirmations
- **Agencies** - Manage client communications efficiently
- **SaaS companies** - First-line support automation

## 📝 License

MIT License - feel free to use and modify for your business needs.

## 👤 Author

**Muhammad Shabrun ALgifari**
- 💼 LinkedIn: [linkedin.com/in/muhammadshabrunalgifari](linkedin.com/in/muhammad-shabrun-algifari-70625a39b/)
- 📧 Email: gifar969@gmail.com

## Acknowledgments

- n8n Community for excellent automation platform
- OpenAI / Claude for powerful language models
- Pinecone for vector database solution

---

⭐ **Found this helpful?** Give it a star and share with others!
