---
name: detect-ai
description: Analyze text to detect if it was written by AI. Returns a score from 0-100 with detailed metrics. Use when checking content before publishing or submitting.
user-invocable: true
argument-hint: [text to analyze]
allowed-tools: WebFetch
---

# Detect AI Content

Analyze text to determine if it was written by AI using the HumanizerAI API.

## How It Works

When the user invokes `/detect-ai`, you should:

1. Extract the text from $ARGUMENTS
2. Call the HumanizerAI API to analyze the text
3. Present the results in a clear, actionable format

## API Call

Make a POST request to `https://humanizerai.com/api/v1/detect`:

```
Authorization: Bearer $HUMANIZERAI_API_KEY
Content-Type: application/json

{
  "text": "<user's text>"
}
```

## Response Format

Present results like this:

```
## AI Detection Results

**Score:** X/100 (verdict)
**Words Analyzed:** N

### Metrics
- Perplexity: X (interpretation)
- Burstiness: X (interpretation)
- Readability: X
- N-gram Score: X

### Recommendation
[Based on score, suggest whether to humanize]
```

## Score Interpretation

- 0-20: Human-written content
- 21-40: Likely human, minor AI patterns
- 41-60: Mixed signals, could be either
- 61-80: Likely AI-generated
- 81-100: Highly likely AI-generated

## Error Handling

If the API call fails:
1. Check if HUMANIZERAI_API_KEY is set
2. Suggest the user get an API key at https://humanizerai.com
3. Provide the error message for debugging
