# Bloom / Release 001 (Garden)
Mark Walhimer, 2026

Live: https://walhimer.github.io/bloom-release/

---

## What it is

Twenty-two blooms appear, one by one. Each carries emergent DNA — unique color, size, breath speed, position, and a pentatonic piano note. They grow, hold, and release in order. The garden that appears tonight will never appear again.

## File structure

```
bloom-release/
├── index.html      ← presentation page + artwork embedded (single file)
├── samples/        ← 22 Salamander Grand Piano MP3 files
│   ├── C2.mp3
│   ├── D2.mp3
│   └── ... (22 files total, C pentatonic across 4 octaves)
└── README.md
```

## Audio

- Salamander Grand Piano samples (CC license), loaded from `./samples/`
- Tone.js 14.7.77 via CDN
- C pentatonic scale: C2 D2 E2 G2 A2 / C3 D3 E3 G3 A3 / C4 D4 E4 G4 A4 / C5 D5 E5 G5 A5 / C6 D6
- Each bloom is assigned one unique note per cycle — no two blooms share a note
- Audio activates on first click anywhere on the page (browser requirement)

## Running locally

Opening index.html directly from your Desktop will not work — browsers block local audio files over file:// protocol.

Run a local server instead:

```bash
cd path/to/bloom-release
python3 -m http.server 8000
```

Then open: http://localhost:8000

## Deploying to GitHub Pages

1. Push index.html and samples/ folder to main branch
2. Settings → Pages → Deploy from branch → main / root
3. Wait 2–3 minutes for deployment
4. Live at https://walhimer.github.io/bloom-release/

## Architecture note

The garden sketch is embedded directly in index.html — not in a separate file, not in an iframe. This is the same approach as Traveling Landscape and is required for audio to activate on a single click. Do not move the sketch to a separate file.

## Sample files

The 22 MP3 files in samples/ are the exact notes used by the sketch. Do not rename them. Do not replace them with the standard Salamander 16-file set — the sketch maps directly to these filenames.

| File | Note |
|------|------|
| C2.mp3 | C2 |
| D2.mp3 | D2 |
| E2.mp3 | E2 |
| G2.mp3 | G2 |
| A2.mp3 | A2 |
| C3.mp3 | C3 |
| D3.mp3 | D3 |
| E3.mp3 | E3 |
| G3.mp3 | G3 |
| A3.mp3 | A3 |
| C4.mp3 | C4 |
| D4.mp3 | D4 |
| E4.mp3 | E4 |
| G4.mp3 | G4 |
| A4.mp3 | A4 |
| C5.mp3 | C5 |
| D5.mp3 | D5 |
| E5.mp3 | E5 |
| G5.mp3 | G5 |
| A5.mp3 | A5 |
| C6.mp3 | C6 |
| D6.mp3 | D6 |
