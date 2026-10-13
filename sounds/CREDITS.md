# Sound credits

Every sound here is either made for the game or released under
[CC0](https://creativecommons.org/publicdomain/zero/1.0/) - free for any use,
commercial included, with no credit required. They are listed anyway, so it
is always clear where each one came from.

| File | What it is | Source | License |
|---|---|---|---|
| `bgm.wav` | "Happy Vibes" by Ruskerdax - the background music | [OpenGameArt](https://opengameart.org/node/160228) | CC0 |
| `sfx/ting.wav` | `glass_001` from Interface Sounds by Kenney - a rating star appearing | [kenney.nl](https://kenney.nl/assets/interface-sounds) | CC0 |
| `sfx/coin.wav` | "Plingy Coin" by Fupi - a star landing in the counter | [OpenGameArt](https://opengameart.org/content/plingy-coin) | CC0 |
| `sfx/clack.wav` | the slate's clapstick snapping shut: `impactWood_light_002` layered with `impactPlank_medium_000`, from Impact Sounds by Kenney | [kenney.nl](https://kenney.nl/assets/impact-sounds) | CC0 |
| `click.mp3` | the button click | - | the game's own |
| every other `sfx/*.wav` | synthesised for the game by `tools/make_sfx.py` | - | the game's own |

## How the recordings were prepared

- **`bgm.wav`** - decoded from the original MP3 with macOS `afconvert`; the
  28 ms of silence the MP3 encoder puts at the start was trimmed, and the last
  20 ms crossfaded into the first, so the loop has no gap or click where it
  joins. Then mixed to mono at 32 kHz, 16-bit. It is a WAV and not an .m4a
  because AAC adds silence at both ends, which a loop plays as a hiccup.
- **`sfx/ting.wav`, `sfx/coin.wav`** - mixed to mono, trimmed of silence,
  faded out over their last 20 ms and set to a peak of -6 dB.
- **`sfx/clack.wav`** - the two hits lined up on their peaks (the plank at
  60%), a 300 Hz high-pass to take out the boom, 220 ms long with a 30 ms
  fade, peak -1.4 dB.
