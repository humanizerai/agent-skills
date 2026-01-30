# HumanizerAI API Reference

Base URL: `https://humanizerai.com/api/v1`

## Authentication

All requests require an API key in the Authorization header:

```
Authorization: Bearer hum_your_api_key
```

## Endpoints

### POST /detect

Analyze text for AI detection.

**Request:**
```json
{
  "text": "Text to analyze (max 10,000 words)"
}
```

**Response:**
```json
{
  "score": 85,
  "metrics": {
    "perplexity": 42.5,
    "burstiness": 0.35,
    "readability": 65.2,
    "satPercent": 12.5,
    "simplicity": 78.3,
    "ngramScore": 0.15,
    "averageSentenceLength": 18.4
  },
  "verdict": "likely_ai",
  "wordsProcessed": 250
}
```

### POST /humanize

Transform AI text into human-like content.

**Request:**
```json
{
  "text": "Text to humanize (max 10,000 words)",
  "intensity": "medium"
}
```

**Response:**
```json
{
  "humanizedText": "The humanized text...",
  "score": {
    "before": 85,
    "after": 15
  },
  "wordsProcessed": 250,
  "credits": {
    "subscriptionRemaining": 49750,
    "topUpRemaining": 0,
    "totalRemaining": 49750
  }
}
```

## Error Codes

| Code | Message | Description |
|------|---------|-------------|
| 400 | Text is required | Missing text parameter |
| 400 | Text exceeds maximum | Over 10,000 word limit |
| 401 | API key required | Missing Authorization header |
| 401 | Invalid API key | Key not found or revoked |
| 403 | API access requires Pro/Business | Plan doesn't include API |
| 403 | insufficient_credits | Not enough credits |

## Rate Limits

| Plan | Requests/min | Max Words |
|------|--------------|-----------|
| Pro | 60 | 10,000 |
| Business | 300 | 10,000 |

## Documentation

Full documentation: https://humanizerai.com/docs/api
