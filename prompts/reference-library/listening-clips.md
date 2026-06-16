# Silent listening clips — Ivakon

Use when a guest speaks and Ivakon stays on camera **without talking**.

1. Add clips to `data/listening-scene-map.json`
2. `python3 tools/generate_prompts.py --mode listening --episode EP001`
3. Paste `prompts/generated/listening/EP001/EP001-Lxx.json` + matching ref PNG
4. For long holds, use crossfade stitch:
   ```bash
   python3 tools/stitch_listening_hold.py --input-dir video/raw/listening/EP001 --target 60
   ```
5. **Guest audio only** — mute Ivakon track

Default listen ref: `ivakon-angle-05-profile-left-smile.png`