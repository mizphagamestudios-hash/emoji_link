# Sound credits

Every sound here is either made for the game or released under
[CC0](https://creativecommons.org/publicdomain/zero/1.0/) - free for any use,
commercial included, with no credit required. They are listed anyway, so it
is always clear where each one came from.

| File | What it is | Source | License |
|---|---|---|---|
| `bgm.wav` | the background music | supplied by the game's developer (`bgm.mp3`) | as supplied |
| `sfx/cheer.wav` | a cheer, as a level is finished | supplied by the game's developer (`cheer.mp3`) | as supplied |
| `sfx/ting.wav` | `glass_001` from Interface Sounds by Kenney - a rating star appearing | [kenney.nl](https://kenney.nl/assets/interface-sounds) | CC0 |
| `sfx/coin.wav` | "Plingy Coin" by Fupi - a star landing in the counter | [OpenGameArt](https://opengameart.org/content/plingy-coin) | CC0 |
| `sfx/clack.wav` | the slate's clapstick snapping shut: `impactWood_light_002` layered with `impactPlank_medium_000`, from Impact Sounds by Kenney | [kenney.nl](https://kenney.nl/assets/impact-sounds) | CC0 |
| `click.mp3` | the button click | - | the game's own |
| every other `sfx/*.wav` | synthesised for the game by `tools/make_sfx.py` | - | the game's own |

## How the recordings were prepared

- **`bgm.wav`** - decoded from the supplied MP3 with macOS `afconvert` and
  mixed to mono at 32 kHz, 16-bit. Its first 0.89 s - silence, then the
  opening clap - and the 2.17 s of near-silence after its fade-out were cut;
  it fades in over 40 ms on the soft pad that ran under that clap, and its
  last 20 ms are crossfaded into its first, so the loop has no gap or click
  where it joins. It is a WAV and not an .m4a because AAC adds silence at both ends,
  which a loop plays as a hiccup.
- **`sfx/cheer.wav`** - decoded from the supplied MP3, mixed to mono at
  44.1 kHz, set to a peak of -1.7 dB (the level-finish sound it replaced) and
  faded out over its last 20 ms.
- **`sfx/ting.wav`, `sfx/coin.wav`** - mixed to mono, trimmed of silence,
  faded out over their last 20 ms and set to a peak of -6 dB.
- **`sfx/clack.wav`** - the two hits lined up on their peaks (the plank at
  60%), a 300 Hz high-pass to take out the boom, 220 ms long with a 30 ms
  fade, peak -1.4 dB.
