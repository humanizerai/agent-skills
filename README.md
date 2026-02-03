# HumanizerAI Agent Skills

AI detection and text humanization skills for [Claude Code](https://claude.ai/code), [Cursor](https://cursor.sh), and other AI coding assistants.

**Detect AI-generated content** and **humanize text** to bypass GPTZero, Turnitin, Originality.ai, and other AI detectors.

## Skills

| Skill | Command | Description | Credits |
|-------|---------|-------------|---------|
| detect-ai | `/detect-ai` | Check if text is AI-generated | Free |
| humanize | `/humanize` | Make AI text undetectable | 1 word = 1 credit |

## Installation

### Using npx (Recommended)

```bash
npx skills add humanizerai/agent-skills
```

Installs both `/detect-ai` and `/humanize` commands to Claude Code, Cursor, Codex, and other supported agents.

### Manual Installation

```bash
git clone https://github.com/humanizerai/agent-skills.git
cp -r agent-skills/skills/detect-ai .claude/skills/
cp -r agent-skills/skills/humanize .claude/skills/
```

## Setup

1. Get an API key from [humanizerai.com](https://humanizerai.com)
2. Subscribe to Pro ($19.99/mo) or Business ($49.99/mo) plan
3. Click your **profile picture** → **Settings** → **API Keys** and create a key
4. Set your API key as an environment variable:

```bash
export HUMANIZERAI_API_KEY="hum_your_api_key_here"
```

## Usage

### Detect AI Content

```
/detect-ai [your text here]
```

Returns a score (0-100) with detailed metrics showing how likely the text is AI-generated.

### Humanize Text

```
/humanize [your text here]
```

Transforms AI-generated text into natural human writing that bypasses AI detectors.

**With intensity option:**

```
/humanize --intensity aggressive [your text here]
```

## Intensity Levels

| Value | Name | Description | Best For |
|-------|------|-------------|----------|
| `light` | Light | Subtle changes, preserves style | Low AI scores, preserve voice |
| `medium` | Medium | Balanced rewrites (default) | Most use cases |
| `aggressive` | Bypass | Maximum bypass mode | High AI scores, strict detectors |

## Example Workflow

1. **Check your text**: `/detect-ai [paste your AI content]`
2. **See the score**: Get detailed metrics and recommendations
3. **Humanize if needed**: `/humanize [your text]`
4. **Verify results**: `/detect-ai [humanized text]`

## Bypasses These Detectors

- GPTZero
- Turnitin
- Originality.ai
- Copyleaks
- ZeroGPT
- Winston AI
- And more...

## Pricing

| Plan | Price | Words/Month | API Access |
|------|-------|-------------|------------|
| Pro | $19.99/mo | 50,000 | Yes |
| Business | $49.99/mo | 200,000 | Yes |

- **Detection**: Always free and unlimited
- **Humanization**: 1 credit = 1 word

## Compatibility

Works with:
- [Claude Code](https://claude.ai/code)
- [Cursor](https://cursor.sh)
- [Windsurf](https://codeium.com/windsurf)
- Any agent supporting the [Agent Skills](https://agentskills.io) format

## API Documentation

Full API docs: [humanizerai.com/docs/api](https://humanizerai.com/docs/api)

## Support

- Website: [humanizerai.com](https://humanizerai.com)
- Support: [humanizerai.com/support](https://humanizerai.com/support)

## License

MIT
