# HumanizerAI Agent Skills

Agent skills for [HumanizerAI](https://humanizerai.com) - AI detection and text humanization.

## Features

- `/detect-ai` - Check if text is AI-generated (free)
- `/humanize` - Make AI text undetectable

## Installation

### Option 1: Using npx (Recommended)

```bash
npx skills add humanizerai/agent-skills
```

### Option 2: Clone to your project

```bash
git clone https://github.com/humanizerai/agent-skills.git
cp -r agent-skills/skills/humanizerai .claude/skills/
```

### Option 3: Manual copy

Copy the skill files to your project's `.claude/skills/humanizerai/` directory:

```bash
mkdir -p .claude/skills/humanizerai
# Copy files from skills/humanizerai/ to .claude/skills/humanizerai/
```

## Setup

1. Get an API key from [humanizerai.com](https://humanizerai.com)
2. Set your API key as an environment variable:

```bash
export HUMANIZERAI_API_KEY="hum_your_api_key_here"
```

## Usage

### Detect AI Content

```
/detect-ai [your text here]
```

### Humanize Text

```
/humanize [your text here]
```

With intensity option:

```
/humanize --intensity aggressive [your text here]
```

## Intensity Levels

| Value | Name | Description | Use Case |
|-------|------|-------------|----------|
| `light` | Light | Subtle changes | Low AI scores, preserve style |
| `medium` | Medium | Balanced (default) | Most use cases |
| `aggressive` | Bypass | Maximum bypass mode | High AI scores, strict detectors |

## Requirements

- HumanizerAI Pro or Business plan
- API key (get at https://humanizerai.com/dashboard)

## Pricing

- **Detection**: Free and unlimited
- **Humanization**: 1 credit = 1 word

Plans:
- Pro: $19.99/mo - 50,000 words/month
- Business: $49.99/mo - 200,000 words/month

## Compatibility

Works with:
- [Claude Code](https://claude.ai/code)
- [Cursor](https://cursor.sh)
- [Windsurf](https://codeium.com/windsurf)
- Any agent supporting the [Agent Skills](https://agentskills.io) format

## Support

- Documentation: https://humanizerai.com/docs/api
- Support: https://humanizerai.com/support

## License

MIT
