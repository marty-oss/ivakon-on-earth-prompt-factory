# Ivakon on Earth — Character & Voice Bible

Use across every clip. **Voice timbre is locked in** [config/voice-lock.json](config/voice-lock.json) — do not override per scene.

## Visual identity (locked)

- **Name:** Ivakon (on Earth)
- **Look:** Adult male humanoid with pale gray cracked reptilian skin, pointed ears, spiky brown hair with lighter highlights
- **Wardrobe:** Plain black crew-neck t-shirt, thin silver chain necklace
- **Props:** Black studio condenser microphone on boom arm with foam windscreen
- **Set:** *Beyond the Signal* podcast studio — dark brick wall, blue neon circular logo sign, wooden shelves, red **ON AIR** light, warm table lamp
- **Expression guardrails:** Friendly, confident, engaging — never evil, angry, demonic, scary, or aggressive

## Approved voice (locked)

**Adult male Swedish-accented tech podcast host; hyper, fast-paced, high-energy delivery with upbeat enthusiasm — distinctive Nordic accent, never monotone.**

Vocal reference: Ivan on Tech — Swedish accent, hyper enthusiastic tech-host energy. Ivakon matches that **style family**, not a literal impersonation.

Same speaker, same Swedish accent, same fast hyper pacing on every mini-scene. Calibrate on **MS02**; re-take MS02 if timbre or accent drifts.

Per-scene `voice_notes` in scene-map are **delivery emphasis only** — never change accent, energy level, or timbre.

## Motion style (dynamic but controlled)

- Subtle push-in when camera note requests it
- Expressive eyes, realistic blinking, small natural head movement
- Natural mouth movement synced to exact dialogue (speaking clips only)

## Hard rules for Imagine

1. **Exact dialogue only** — no improvise, paraphrase, add, or skip
2. **Speech within 0.2–0.5 seconds** — no silent lead-in (speaking clips)
3. **Same voice** — `voice_direction` identical on every JSON prompt
4. **Same visual identity** — match reference image; swap ref file for angle variety
5. **Keep cracked skin texture, pointed ears, spiky hair, black tee, chain, and Beyond the Signal studio**