---
name: open-claw-seedance
description: Wrap Dreamina (即梦) Seedance video generation for OpenClaw agents. Use this skill to log in, check credits, generate Seedance 2.0/2.0fast videos from text prompts, create structured ad shots, or generate videos from a reference character image using image2video.
---

# Open Claw Seedance Skill

Use this Skill whenever an agent needs to call the `dreamina` CLI (即梦) to generate Seedance videos for OpenClaw workflows.

It standardizes three workflows:

1. Text → video via `dreamina text2video`
2. Structured "ad shots" with explicit duration / ratio / model
3. Image → video via `dreamina image2video` using a hero character image for consistency

See `references/jimeng-cli-quickstart.md` for the CLI quickstart based on the official Feishu doc.
