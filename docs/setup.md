# Setup Guide

## Prerequisites

Before you begin, ensure you have:
- ✅ n8n instance
- ✅ Gmail account with API access enabled
- ✅ OpenAI API key or Anthropic Claude API key
- ✅ Pinecone account (free tier works)
- ✅ Google Cloud project (for Drive & Sheets API)
- ✅ OCRspace API Key (free tier works)

## Step 1: Install n8n

### Self-hosted
You can use Hostinger VPS or Elest.io

### Cloud (n8n.cloud)
Sign up at [n8n.cloud](https://n8n.cloud) and create new instance

## Step 2: Import Workflow

1. Download `workflows/email-agent.json` from this repo
2. Open your n8n instance
3. Click **Workflows** → **Import from File**
4. Select the downloaded JSON file
5. Click **Import**

## Step 3: Configure Gmail API

1. Go to [Google Cloud Console](https://console.cloud.google.com)
2. Create new project or select existing
3. Enable **Gmail API**
4. Create **OAuth credentials**
5. In n8n:
   - Go to **Credentials** → **Add Credential**
   - Select **Gmail OAuth2**

or watch the tutorial here: [Google OAuth Authentication in n8n](https://youtu.be/FBGtpWMTppw?si=WMn-q8iUxdgvhUHx)

## Step 4: Setup OpenAI/Claude API

1. Get API key from:
   - OpenAI: https://platform.openai.com/api-keys
   - Anthropic: https://console.anthropic.com
2. In n8n:
   - **Credentials** → **Add Credential**
   - Select **OpenAI** or **Anthropic**
   - Paste your API key

## Step 5: Configure Pinecone (Vector Database)

1. Sign up at [Pinecone](https://www.pinecone.io)
2. Create new index:
   - Name: `email-knowledge-base`
   - Dimensions: `1536` (for OpenAI embeddings)
   - Metric: `cosine`
3. Get API key from dashboard
4. Add to n8n credentials

## Step 6: Upload Knowledge Base

1. Prepare your company FAQ/documentation
2. Use the **"Upload to Vector DB"** workflow (included)
3. Run workflow to create embeddings

## Step 7: Customize Prompts

Edit prompts in the workflow nodes:
- **Text Classifier**: Modify categories for your business
- **Customer Support Agent**: Update company voice/tone
- **Priority Detector**: Adjust urgency criteria

## Step 8: Test Workflow

1. Send test email to your Gmail
2. Check workflow execution in n8n
3. Verify:
   - ✅ Email classified correctly
   - ✅ AI response generated (if customer support)
   - ✅ Invoice extracted (if billing email)
   - ✅ High priority forwarded (if urgent)

## Troubleshooting

**If workflow not triggering:**
- Check Gmail trigger is activated
- Verify OAuth token is valid

**If AI not responding:**
- Check API key is correct
- Verify you have API credits

**If vector search not working?**
- Ensure index name matches
- Check embeddings were uploaded

---
