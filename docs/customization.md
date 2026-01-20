# Customization Guide

## Adding New Email Categories

1. Open **Text Classifier** node
2. Update the prompt:
```
Classify this email into one of these categories:
- Promotion
- Invoice/Billing
- High Priority
- Customer Support
- NEW_CATEGORY  ← Add here
```

3. Add new branch in workflow for your category

## Changing AI Model

Replace OpenAI with Claude:
1. Delete OpenAI node
2. Add **Anthropic** or Open Router node
3. Update prompt format (Claude prefers structured prompts)

## Integration with Slack

Instead of Email response, send to Slack:
1. Add **Slack** node after AI response
2. Configure channel
3. Format message with thread support

## Custom Vector Database

Using Supabase instead of Pinecone:
1. Replace Pinecone nodes with Supabase or HTTP Request nodes
2. Point to API endpoint
3. Adjust embedding format

---

Feel free to fork and modify for your needs!
