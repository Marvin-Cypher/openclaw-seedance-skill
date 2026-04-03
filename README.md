# openclaw-seedance-skill

OpenClaw skill wrapping [Dreamina (即梦)](https://jimeng.jianying.com) Seedance video generation for AI agents.

## What it does

Generate videos from text prompts or images using Dreamina's Seedance models — directly from an OpenClaw agent.

**Three workflows:**

| Workflow | Command | Use case |
|----------|---------|----------|
| Text → Video | `dreamina text2video` | Generate video from a text prompt |
| Ad Shots | `dreamina text2video` | Structured ad creative with explicit duration/ratio/model |
| Image → Video | `dreamina image2video` | Animate a reference image into video |

## Install

Add this skill to your OpenClaw instance:

```bash
openclaw skills install github:Marvin-Cypher/openclaw-seedance-skill
```

Or clone manually into your skills directory:

```bash
git clone https://github.com/Marvin-Cypher/openclaw-seedance-skill.git
cp -r openclaw-seedance-skill/skills/open-claw-seedance ~/.openclaw/skills/
```

### Dreamina CLI

The skill requires the `dreamina` CLI:

```bash
curl -fsSL https://jimeng.jianying.com/cli -o /tmp/install-dreamina.sh
sh /tmp/install-dreamina.sh
```

Then login:

```bash
dreamina login
```

Check credits:

```bash
dreamina user_credit
```

## Skill structure

```
skills/open-claw-seedance/
├── SKILL.md                              # Skill definition
└── references/
    ├── jimeng-cli-quickstart.md           # CLI quickstart guide
    ├── dreamina-cli-full.md               # Full CLI reference (all subcommands)
    └── generative-tools.md                # Generative AI tools comparison
```

## Supported models

- **Seedance 2.0** — Highest quality, capacity-constrained
- **Seedance 2.0 Fast** — Faster generation, good quality

Always check available models with `dreamina <subcommand> -h` as support varies by command.

## Examples

**Text to video:**
```bash
dreamina text2video \
  --prompt="A robot walking through a neon-lit city at night" \
  --duration=5 \
  --ratio=16:9 \
  --video_resolution=720p \
  --poll=30
```

**Image to video:**
```bash
dreamina image2video \
  --image=./hero-character.png \
  --prompt="camera slowly pushes in, character turns to face camera" \
  --duration=5 \
  --video_resolution=720p \
  --poll=30
```

## References

- [Dreamina (即梦) official site](https://jimeng.jianying.com)
- [Dreamina CLI docs](https://jimeng.jianying.com/cli)
- [OpenClaw](https://github.com/openclaw/openclaw)

## License

MIT
