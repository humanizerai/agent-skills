# HumanizerAI Skill Examples

## Detecting AI Content

### Basic Detection
```
User: /detect-ai Artificial intelligence has revolutionized numerous industries
by enabling machines to perform tasks that previously required human intelligence.
Furthermore, these advancements have led to significant improvements in efficiency
and productivity across various sectors.

Claude: ## AI Detection Results

**Score:** 87/100 (Highly likely AI-generated)
**Words Analyzed:** 35

### Metrics
- Perplexity: 28.3 (Low - very predictable text)
- Burstiness: 0.25 (Low - uniform sentence structure)
- Readability: 62.4 (Consistent grade level)
- N-gram Score: 0.22 (AI patterns detected)

### Recommendation
This text shows strong AI patterns. Consider using `/humanize` to make it
more natural before publishing or submitting.
```

### Human-like Text
```
User: /detect-ai I've been thinking about this for weeks now. Sometimes
you just know when something's off, you know? Like yesterday - my coffee
tasted weird. Turns out I'd grabbed the decaf by accident. Classic me.

Claude: ## AI Detection Results

**Score:** 12/100 (Human-written)
**Words Analyzed:** 41

### Metrics
- Perplexity: 89.4 (High - natural variation)
- Burstiness: 0.82 (High - varied sentence lengths)
- Readability: 48.7 (Natural variation)
- N-gram Score: 0.03 (No AI patterns)

### Recommendation
✅ This text appears human-written. No humanization needed.
```

## Humanizing Text

### Basic Humanization
```
User: /humanize The implementation of artificial intelligence in healthcare
has demonstrated significant potential for improving patient outcomes and
streamlining clinical workflows.

Claude: ## Humanization Complete ✨

**Score:** 82 → 18 (64 points improvement)
**Words Processed:** 21
**Credits Remaining:** 49,979

---
### Humanized Text

AI in healthcare is actually making a real difference now. Doctors are seeing
better results with their patients, and honestly, the whole clinical process
runs way smoother than it used to.

---

✅ Text should now pass most AI detectors.
```

### Aggressive Intensity
```
User: /humanize --intensity aggressive Furthermore, the utilization of
machine learning algorithms has enabled unprecedented levels of automation
in data processing and analysis procedures.

Claude: ## Humanization Complete ✨

**Score:** 91 → 8 (83 points improvement)
**Words Processed:** 18
**Credits Remaining:** 49,961

---
### Humanized Text

ML is changing how we handle data - it's pretty wild. Stuff that took forever
to analyze? Now it just... happens.

---

✅ Text should now pass most AI detectors.
Note: Aggressive mode significantly shortened the text for maximum bypass.
```

## Workflow Example

### Check Then Humanize
```
User: /detect-ai [their essay text]

Claude: Score: 75/100 - This text shows AI patterns.
Recommendation: Use /humanize to reduce the AI score.

User: /humanize --intensity medium [same text]

Claude: Score improved from 75 to 22.
Text is now likely to pass AI detectors.

User: /detect-ai [the humanized text]

Claude: Score: 22/100 - Appears human-written.
✅ Safe to submit.
```
