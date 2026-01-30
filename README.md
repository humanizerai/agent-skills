# HumanizerAI Agent Skills

Agent skills for [HumanizerAI](https://humanizerai.com) - AI detection and text humanization for Claude Code.

## Features

- `/detect-ai` - Check if text is AI-generated
- `/humanize` - Make AI text undetectable

## Installation

### Option 1: Copy to your project

Copy the skill files to your project's `.claude/skills/humanizerai/` directory:

```bash
mkdir -p .claude/skills/humanizerai
cp SKILL.md detect-ai.md humanize.md api-reference.md examples.md .claude/skills/humanizerai/
```

### Option 2: Clone the repository

```bash
git clone https://github.com/humanizerai/agent-skills.git .claude/skills/humanizerai
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

| Level | Description | Use Case |
|-------|-------------|----------|
| `light` | Subtle changes | Low AI scores, preserve style |
| `medium` | Balanced (default) | Most use cases |
| `aggressive` | Maximum bypass | High AI scores, strict detectors |

## Requirements

- HumanizerAI Pro or Business plan
- API key (get at https://humanizerai.com/dashboard)

## Pricing

- **Detection**: Free and unlimited
- **Humanization**: 1 credit = 1 word

Plans:
- Pro: $19.99/mo - 50,000 words/month
- Business: $49.99/mo - 200,000 words/month

## Support

- Documentation: https://humanizerai.com/docs/api
- Support: https://humanizerai.com/support

## License

MIT
