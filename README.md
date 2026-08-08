# GHOST-17X — Vox Archive

A soundboard for GHOST-17X, Aelyn Vox's companion construct. 1,242 voice fragments, searchable by what they actually say.

## What it does

- **PING** — big shard button up top pulls a random clip. If a filter is active it pulls from within that filter, so you can narrow to Combat and then PING for a random battle cry. Spacebar does the same.
- **Search** — every clip was run through speech recognition, so the tiles show what Ghost says and the search box matches on it. Press `/` to jump to the box.
- **Categories** — 20 of them, plus a length filter (Bark / Line / Speech / Monologue) as a second axis.
- **Star** clips you want on hand for a session. **✎** fixes a transcript the recogniser got wrong. Both persist in the browser; export/import lives in the Setup panel.

## Layout

```
index.html
Daeghost/
  du01dagoth_du01dagothfollo_00000006_1.mp3
  ...
```

Double-click `index.html` and it works. No build step, no dependencies.

## Publishing to GitHub Pages

Put this in **its own repo**, not the `fryedegg.github.io` one — Pages allows 1 GB per published site, and a separate repo gets its own budget instead of eating into the atlas's.

1. Use the `Daeghost` folder of MP3s (67 MB), not the original WAVs (489 MB). Git keeps deleted
   files in history forever, so committing the WAVs first would mean carrying half a gigabyte
   permanently even after you swapped them out. The board defaults to `.mp3`.

2. Push with GitHub Desktop or the CLI, not the web uploader — 1,242 files will hit its per-upload limit.

3. Settings → Pages → deploy from `main`, root folder.

## If a browser won't read the local files

Some browsers block `file://` subresources depending on settings. Open the Setup panel, hit **Point at the folder**, and select `Daeghost`. Playback then runs entirely from memory.

## Custom lines

Not built in. Generate them in the Artlist toolkit in a second tab and play them from there.

---

Oratoria: The Shattering · C2 · bonded unit: Aelyn Vox
