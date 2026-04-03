# 即梦 / Dreamina CLI Quickstart

This is a short quickstart for the `dreamina` CLI based on the official Feishu doc.

## Install

```bash
curl -fsSL https://jimeng.jianying.com/cli | bash
```

## Login

```bash
dreamina login
```

If browser login is not available, use:

```bash
dreamina login --headless
```

and import the login JSON:

```bash
dreamina import_login_response --file /path/to/dreamina-login.json
```

Check credits / login state:

```bash
dreamina user_credit
```

## Core generator commands

### text2video

```bash
dreamina text2video \ 
  --prompt="your prompt" \ 
  --duration=5 \ 
  --ratio=9:16 \ 
  --video_resolution=720p \ 
  --poll=30
```

### image2video

```bash
dreamina image2video \ 
  --image=./first.png \ 
  --prompt="camera push in" \ 
  --duration=5 \ 
  --video_resolution=720p \ 
  --poll=30
```

For more details, agents should call:

```bash
dreamina <subcommand> -h
```

and follow the combinations described there.
