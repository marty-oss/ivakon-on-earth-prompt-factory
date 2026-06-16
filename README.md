# Ivakon on Earth — Prompt Factory

Local production workflow for **Ivakon** — reptilian humanoid host of *Beyond the Signal*. Splits scripts into short **Grok Imagine image-to-video** mini-scenes with locked voice and varied camera refs.

**Repo:** https://github.com/marty-oss/ivakon-on-earth-prompt-factory  
**Siblings:** [Zorak Rogan](https://github.com/marty-oss/zorak-rogan-prompt-factory) · [Pomplarion](https://github.com/marty-oss/pomplarion-prompt-factory)

## v1 scaffold

- 8 angle reference PNGs in `references/character/`
- Identity + voice lock in `config/`
- Generator tools (no episodes in scene-map yet)

## Quick workflow (when episodes exist)

```bash
cd /Users/martywork/ivakon-on-earth-prompt-factory

# 1. Edit mini-scenes
open data/scene-map.json

# 2. Generate prompts (JSON + compact + TXT)
python3 tools/generate_prompts.py --episode EP001

# 3. Verify voice lock
python3 tools/verify_voice_lock.py --episode EP001

# 4. Paste into Imagine
open prompts/generated/EP001/compact/EP001-MS01-voice.json
```

## Folder layout

| Path | Purpose |
|------|---------|
| `config/ivakon-identity.md` | Visual bible |
| `config/voice-lock.json` | Locked `voice_direction` |
| `references/character/ivakon-angle-*.png` | Imagine start frames |
| `data/scene-map.json` | Speaking mini-scenes (empty until EP001) |
| `data/listening-scene-map.json` | Silent listen clips |
| `tools/generate_prompts.py` | Prompt generator |
| `tools/stitch_listening_hold.py` | Crossfade silent holds |
| `prompts/generated/` | Output JSON / TXT / compact |

## Reference angles

Default speaking ref: `ivakon-angle-04-front-close-smile.png`  
Default listening ref: `ivakon-angle-05-profile-left-smile.png`

See [references/character/SOURCE-MAPPING.md](references/character/SOURCE-MAPPING.md).

## Add first episode

1. Add script under `scripts/episodes/`
2. Add `episode_id: EP001` block to `data/scene-map.json` with `mini_scenes[]`
3. Run `python3 tools/generate_prompts.py --episode EP001`
4. Lock voice in `config/voice-lock.json` after MS02 sounds right

## Listening mode

```bash
python3 tools/generate_prompts.py --mode listening --episode EP001
python3 tools/stitch_listening_hold.py --input-dir video/raw/listening/EP001 --target 60
```

Outputs under `prompts/generated/listening/EP001/`.