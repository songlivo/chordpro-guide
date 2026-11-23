# ChordPro guide for Songlivo

[ChordPro](https://www.chordpro.org/) is a plain-text format for songs: chords go in square brackets right before the syllable they belong to. [Songlivo](https://songlivo.com/en/) reads and writes it, so a song typed here works in the app and in most other songbook tools.

## The basics

```chordpro
{title: Morning Road}
{artist: Songlivo example}
{key: G}

[G]Coffee on the [C]window, [G]sun is coming [D]up
```

The app renders the chord above the lyric:

```
G               C        G              D
Coffee on the window, sun is coming up
```

## Directives Songlivo understands

| Directive | Short form | What it does |
|---|---|---|
| `{title: …}` | `{t: …}` | Song title |
| `{artist: …}` | `{a: …}` | Artist; `{subtitle:}` / `{st:}` also work |
| `{key: …}` | | Original key, the starting point for transposing |
| `{start_of_verse}` / `{end_of_verse}` | `{sov}` / `{eov}` | Verse section |
| `{start_of_chorus}` / `{end_of_chorus}` | `{soc}` / `{eoc}` | Chorus section |
| `{start_of_bridge}` / `{end_of_bridge}` | `{sob}` / `{eob}` | Bridge section |
| `{start_of_tab}` / `{end_of_tab}` | `{sot}` / `{eot}` | Tab block, kept monospaced |
| `{start_of_grid}` / `{end_of_grid}` | `{sog}` / `{eog}` | Chord grid block |

A label can follow a section start, e.g. `{start_of_verse: Verse 2}`. A file without any section is shown as one verse.

## Tips

- **Slash chords** (`[D/F#]`) transpose correctly: both the chord and the bass note move.
- **Keep one chord per bracket.** `[G]` `[C]`, not `[G C]`.
- **Capo is personal, not part of the file.** In stage sync the key is shared with the band, but each player sets their own capo.
- **Lyrics-only mode** hides every bracket, so singers can use the same file.

## Example

[`morning-road.cho`](morning-road.cho) is a short original song written for this guide. Open it in Songlivo (share → open with) or paste its text into the editor.

## Exporting from Songlivo

The app can export a single song as ChordPro text (a `.txt` file), or a whole library or setlist as one `.songlivo` file (a zip archive) to move everything to a new phone.

---

Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The example song is © Songlivo and free to use for testing.
