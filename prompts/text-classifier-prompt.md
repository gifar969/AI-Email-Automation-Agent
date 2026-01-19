# Text Classifier Prompt
Note: This is a demo workflow using a fictional automotive company (Voltx) as an example. Replace company names, categories, and keywords with your actual use case.

## Text to Classify:
Subject: {{ $json.headers.subject }}
Body: {{ $json.text }}

## Workflow Category:
- Promotion
"Marketing or sales-focused emails promoting offers, discounts, or new products. Tone is upbeat and persuasive. Common keywords: sale, offer, discount, promotion, new feature, upgrade, limited time, exclusive."
- Finance/Billing
"Emails regarding vehicle payments, refunds, or VAT incentives (PPN DTP). Includes inquiries about paid software packages or billing for home charger installation. Common keywords: invoice, payment, refund, billing, tax incentive, PPN DTP, charge, receipt."
- High Priority
"Critical issues such as vehicle breakdowns, running out of battery on the road, or urgent Roadside Assistance requests that require the emergency number. Common keywords: urgent, emergency, 1-500-VOLTX, breakdown, out of battery, towing, ASAP."
- Customer Support
"Emails requesting help with VoltX vehicles, charging equipment, or the VoltX Connect app. Includes troubleshooting software updates, vehicle features, or maintenance inquiries. Common keywords: error, issue, help, charging, Wallbox, OTA, maintenance, sync, app, reset."
