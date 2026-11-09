# Release log

All notable changes to Tabloop (called Feedpak Player up to 0.9.1), newest first. Each version is published to https://tabloop.github.io/ and https://bazarcad-ai.github.io/feedpak-player-app/ (also downloadable as a single `index.html`).

## 0.35.0 — 2026-11-09

### New
- **Chord names worked out from the notes.** When 3 or more notes sound together — struck at once (or strummed, within 30 ms), or a note played while the notes before it still ring, as in an arpeggio — the chord's name is shown above the string lines, as for the chord names a song already carries: *C*, *Am7*, *D/F#*, *E5*, *Bm7b5*, *Cadd9*… It's worked out from the pitches with the part's tuning and capo (drop D, 4- and 5-string bass included). In **✏ Edit the tab** it follows every change as you make it: add the notes of a chord and its name appears, change one and it's renamed, delete one and it goes, undo brings it back. A song's own chord names come first; a chord you've edited is named from its new notes. Chords that came without a name — Guitar Pro and MIDI imports, *Tab (from images)* parts — are named too, in Scrolling, Page and Highway. A name is shown only when the chord changes, and notes that don't make a common chord get none. **💾 Save pack** stores the name of an edited chord in the pack (as a chord template), so other players show it too.

## 0.34.1 — 2026-11-09

### Fixed
- **🎸 Tuner and 👂 Live no longer double the panel at the bottom** (B-13). With both on, the input device, level meter and heard note showed twice, once in the record bar for the tuner and once in the live bar, so the two buttons looked like they did the same thing. Now that row shows once: with 👂 Live on, the tuner joins the live bar (its note, labelled *🎸 Tuner*, becomes the large tuner reading) and turning Live off brings it back to its own *🎸 Tuner* bar; with ⏺ Rec armed it's in the record bar only. Without the tuner the note is labelled *Heard*. The tooltips now say what each is for: 🎸 Tuner tunes the instrument (note, cents, nearest string), 👂 Live is for playing along with feedback (ghost notes and a score). Pressing 🎸 Tuner without a song now shows its message instead of nothing.

## 0.34.0 — 2026-11-09

### Improved
- **A small bullseye on the ghost-note card.** Point at a ghost note or a 🎯 marker (or tap it on a phone) after a take or with 👂 Live, and the card now shows a little target like the one in ⏱ Calibration → 🎯 Target practice: a dot for that note, left when early and right when late, up when sharp and down when flat, over rings at your forgiveness limits (and twice and four times them). The dot is green within the limits, yellow when a little off and red when clearly off, like the markers, with the numbers beside it (e.g. *+38 ms late · −12 ¢ flat*). Change the forgiveness in ⚙ Settings and the rings follow. Judging timing only, there's no up and down (*pitch not judged*); a chord is judged on its timing, so its dot sits on the timing line; a missed note shows the empty target and says *missed*; an extra note has no target. Screen readers read out the numbers.

## 0.33.0 — 2026-11-08

### New
- **Open Guitar Pro, TuxGuitar and MIDI files as songs.** Guitar Pro 3, 4 and 5 (`.gp3` `.gp4` `.gp5`), Guitar Pro 6 (`.gpx`), Guitar Pro 7 and 8 (`.gp`), TuxGuitar 2 (`.tg`) and MIDI (`.mid`) files open with **Open file**, drag and drop, **Open folder** and from the **📚 Library** (which now lists Guitar Pro and TuxGuitar files with their parts and tunings). Each track becomes a part: guitar and bass as tab with their tuning (4 to 8 strings) and capo, keyboards as a piano roll, the drums as the drum part, a vocal track as the 🎤 Vocals melody with the file's lyrics. The tempo changes, time signatures and markers (as sections) come along, and repeats and first / second endings are played out, so the beat grid, the metronome, loops and sections follow the song as it's heard.
- **The techniques too:** hammer-ons and pull-offs, slides, bends with their shape, vibrato, harmonics, palm mute, dead notes, tapping, slap and pop, accents, let ring, staccato, tremolo picking and trills, ties, grace notes, chord names and the fingering, drawn on the tab and played by the tab synth.
- **No recording, so it plays with the synths:** the tab synth is switched on for you (*Both*), and the keys and drum parts play through their synths while they're shown. **💾 Save pack** turns the file into a feedpak (with the original file kept inside), so it opens like any other song. Swing, D.C. / D.S. jumps, gradual tempo changes and a Guitar Pro 7 file's own audio track aren't carried over; the message when the song opens says so. Tabloop reads these files itself, on your device: nothing is uploaded or downloaded.

## 0.32.2 — 2026-11-08

### Fixed
- **Tab synth: sustained notes died out long before the end of their line** (*Tab* / *Both* playback). Every note faded like a short pluck, high notes fastest, and a pluck with little fundamental faded faster still, so a note held for 2 s on the high E string was 30 dB down after 0.3 s. Now a held note keeps ringing, slowly mellowing like a held string, to the end of its sustain, then stops in a short click-free release; this holds for chords, bends, slides, vibrato, hammer-ons, harmonics and at slow speeds. Measured on notes held 1–4 s (low E, G and high E strings, 100 % and 50 % speed): the sound now stays within 30 dB of the pluck right to the drawn end (it used to fall that far 0.04–7.5 s early) and is gone 0.02–0.07 s after it. Short notes sound as before; a new note on the same string still stops the old one, a note on another string doesn't.

## 0.32.1 — 2026-11-08

### Improved
- **✏ Edit the tab: moving a note to another string keeps the same note.** Shift+↑ / ↓ (or ▲ ▼) now changes the fret by the interval between the two strings, with the part's tuning: a C on the D string stays a C on the G string. A slide's target moves with it, and a note that can't be played on that string (below its open note) stays where it is, with a message.

## 0.32.0 — 2026-11-08

### New
- **✏ Edit the tab: fix a tab, or write one, right in the app.** With a tab part shown (a song's own guitar or bass part, or the *Tab (from images)* part), press **✏ Edit** in the toolbar: **click a note** to select it (Shift-click adds more), then type its **fret** (or ↑ / ↓), move it to **another string** (Shift+↑ / ↓) or **earlier / later** on the beat grid (← / →), make it longer or shorter, and set its **techniques** — hammer-on, pull-off, slide, bend, vibrato, palm mute, muted note, harmonic, pinch harmonic, tap, accent, tremolo. **Click an empty spot on a string** to add a note there, on the song's beats (whole, ½, ⅓, ¼ or ⅙ beats, or free); **Delete** removes. **⌘Z / ⇧⌘Z** (Ctrl+Z / Ctrl+Y) undo and redo, and **Revert…** puts the part back as it was written. Works in the Scrolling, Page and Highway views, and on a phone (tap a note, then the bar's buttons). Outside edit mode, clicking the tab seeks as before.
- **Everything follows your edits:** the views, the tab synth (*Tab* / *Both*), 👂 Live and the feedback on your takes, loops and sections. An edited part shows ✏ on its tab.
- **Kept with the song, and in the pack if you like.** The edits are saved on your device with the song (and folder-synced and backed up to Google Drive with it, like its loops). **💾 Save pack** writes them into a copy of the pack: the edited part's notes change, everything else stays exactly as it was.

## 0.31.1 — 2026-11-08

### Fixed
- **Extra notes (ones not in the tab) read an octave or two too low** (since 0.28.0) in take feedback and 👂 Live: a D3 played while the A2 before it still rang showed as "Extra note: you played G1". With no tab note to guide the reading, the two notes sounding together were read as one lower note (the pitch at which they repeat together). Many such extra notes were also not shown at all, taken for an echo of the note before. Now an extra note is measured again with the note before it filtered out, as notes in the tab already were. In the detection benchmark, extra notes found and read right go from 46 % to 56 % (takes) and from 48 % to 58 % (👂 Live). Notes in the tab are read the same as before.

## 0.31.0 — 2026-11-08

### New
- **📷 Tab from an image: turn a picture of a tab into a tab part of the song.** A photo of a tab book or sheet, an image file, a screenshot you've taken: with any song open (a feedpak or a YouTube video), **paste it** (Cmd/Ctrl+V), drop it on the window, or use **📷 Tab from an image** in the toolbar. Tabloop reads the tab on it — staves of 4 to 7 lines (several per image, dark on light or light on dark), fret numbers 0–24, chords, bar lines, `x`, string names, and `h` `p` `/` `\` `b` `~` `<12>` — and draws what it read over the image: click a number to fix it, Delete to remove it, click a line to add one. Then say where it goes in the song (**the loop A–B**, **from a time for N bars at a tempo** — the song's tempo there, tap tempo, *after the last part* — or **from … to …**), the tuning and capo, and **Add to the tab**: the notes become a **Tab (from images)** part, shown, heard (Tab / Both) and judged like the song's own parts; for a YouTube video it shows under the player. Add more images to build up the song; an overlapping one asks *Replace* or *Merge*; images' notes can be removed, the part cleared or **exported as text**. Saved with the song (exported, synced and backed up like its loops); **💾 Save pack** writes it into the pack as a real arrangement.
- **Your image stays on your device.** It's read by Tabloop's own recogniser (no upload, no online service, no library download) and isn't kept once the window closes: only the notes are saved. On 120 generated test images (7,197 notes, 16 fonts, plain, dark and photo-like backgrounds, JPEG) about 96 % of the numbers read are right and about 95 % of the numbers are found; small (under ~8 px) or blurred numbers give more mistakes.
- **🧭 A guided tour of the app.** New here? The welcome screen offers **Take a 1-minute tour**: the page dims and each main feature is highlighted in turn with a short card saying what it does (and *Learn more* in the help) — opening songs, the Library and YouTube before a song is open; with one, its parts, the Scrolling / Page / Highway views, speed and pitch, loops, sections and saved loops, the 🎚 Mixer and Tracks, the 🎸 Tuner, 👂 Live and ⏺ Rec, ghost notes or 🎯 markers, 🎤 Vocals, ⏱ Calibration and 🔍 Check my input, 📈 Practice and ⚙ Settings. **Next / Back** (or → / ←), **Esc** or **Skip** to stop. It follows what's on screen: features a song doesn't have are left out, and in the Portrait layout it opens the ☰ menu where needed. Then three short tours: *Practising with your instrument*, *Singing* and *Sync & backup*. After an update, a small **See what's new** note walks through what was added since the version you last used. All of them are in **⚙ Settings → 🔒 Privacy & about** (*Take the tour*), and the [help page](https://tabloop.github.io/help/) links to it. Saying no is remembered on this device; nothing is sent anywhere.

## 0.30.1 — 2026-11-08

### Improved
- **New default string colours:** brighter tones that read better on the dark tab, in the same colour per string as before (Low E red, A yellow, D blue, G orange, B green, high E purple). If you'd picked the previous default, you get the new one; custom colours are kept.
- **New colour presets:** **High contrast (black & white)** for the strings, and a new **Colour-blind friendly** palette (Paul Tol's "bright" scheme). If you'd chosen the old colour-blind preset, your colours stay as they were (shown as *Custom*).

## 0.30.0 — 2026-11-08

### New
- **🎯 Target practice: see where your notes land, and fix the latency from it.** A new **🎯 Target** tab in ⏱ Calibration (also **⚙ Settings → ⏱ Audio & calibration → 🎯 Target practice**, and a button in 🔍 Check my input). The app tells you what to play and when — the 5th fret of the A string 8 times, the open strings low to high (in the song's tuning), or a string and fret you pick — with a count-in, a click and a flash on every beat (or the flash alone, silent). After each note a dot lands on a **bullseye**: left early, right late, up sharp, down flat, with rings at your forgiveness limits (Normal: ±40 ms, ±15 ¢) and at 2× and 4× them; point at a dot for its note, ms and cents; missed notes are listed. Then the average timing and its spread, the average pitch, and tips: when every note is off by about the same (e.g. all 40 ms late) the app proposes the **input nudge** that fixes it (−40 ms), and after a round on the flash alone also a **screen offset**, with **Apply** (try another round with it) and **💾 Save**; scattered notes mean practice, not latency; notes all sharp or flat mean tuning. Nothing is recorded.

## 0.29.0 — 2026-11-08

### New
- **YouTube videos as songs: loop them and slow them down** ([#5](https://github.com/bazarcad-ai/feedpak-player/issues/5)). **▶ YouTube** (header, or **▶ YouTube video…** on the welcome screen): paste a link (`youtube.com/watch?v=…`, `youtu.be/…`, Shorts, embed links, or the 11-character id; a `t=` start time is kept), or drop a YouTube link on the window, or paste one anywhere. The video plays in **YouTube's own player** in the song area, and Tabloop's controls drive it: **▶ / ❚❚**, the seek bar, Space and ← →; playing or pausing in YouTube's player is followed too.
- **Loops on a video** like on a feedpak: ⟲ Loop, start / end, ⌖, nudges (‹ › 0.25 s, ⇤ ⇥ 1 s, − + 0.05 s), the seek-bar handles, `[` `]`, ⏮ Restart, **saved loops**, **loop chains** and the **speed trainer**, kept per video (exported, synced and backed up like a song's). On a real video the jump back is sent 1–9 ms after the loop end (1–19 ms at 200 %) and YouTube's player confirms it about 10 ms later (up to ~50 ms); it may stutter briefly while it buffers.
- **Sections you mark** on a video: **＋ Mark** in Sections (or **M**) where a part starts, then name it; each runs to the next mark. Click to loop, Shift-click for several, ✎ rename, ✕ delete. Kept (and synced) with the video.
- **Speed on a video**: the speeds YouTube offers for it (usually 25–200 % in 25 % steps, pitch kept); − / + step through them, a typed speed goes to the nearest, and the tooltip lists them. A video with only 100 % turns the speed control off.
- **Not for YouTube videos, by design:** pitch (*YouTube's player doesn't allow changing the pitch*), the tab, metronome and count-in, ⏺ Rec, 👂 Live, the mixer: the sound stays inside YouTube's player, which Tabloop never downloads, records or processes (YouTube's terms don't allow it). The 🎸 Tuner works. Practice stats count the time the video actually plays, and 🕘 Recent lists it.
- **Privacy:** YouTube's player script is loaded only when a video is opened, and the player is YouTube's privacy-enhanced one (youtube-nocookie.com). The [privacy policy](https://tabloop.github.io/privacy.html#youtube) and the [terms](https://tabloop.github.io/terms.html) now cover YouTube videos; usage counts gain `features/youtube` (never a video's id or title).
- **Spotify isn't supported:** its developer terms limit an app like this to 5 hand-listed Premium users unless it belongs to a business with 250,000+ monthly users, don't allow its music to overlap other sound, and its player has no speed control (see the help).

## 0.28.0 — 2026-11-08

### New
- **🔍 Check my input: see what the app hears of a note.** For when notes are missed or judged wrong ([#2](https://github.com/bazarcad-ai/feedpak-player/issues/2)): open it from the 👂 Live bar (**🔍 Check input**) or ⚙ Settings next to ⏱ Calibration, pick a string and fret (the song's tuning, or standard; presets for the lowest string open, the 5th fret of the 2nd string and the highest string's 12th fret), hear it if you like (**🔊 Hear it**), and play it a few times — freely or **on a click** every 2 s. For each try a row shows the input level (peak and RMS, clipping), whether a note start was found and how early or late it was on the click, the pitch heard and how clear it is, the cents off, and how the note would be judged with your ⚙ Settings limits; under it, advice: *your signal is clipping: lower the input level in 🎚 Mixer → Input*, *too quiet*, *pitch unclear: distortion — try the clean channel or ⏱ Timing only*, *heard F3 instead of D3*, *25 ¢ flat*, *80 ms late: ⏱ Calibrate*. Nothing is recorded or stored.

### Improved
- **Note detection copes with effects: distortion, fuzz, delay, chorus, reverb, a quiet input, legato runs** ([#2](https://github.com/bazarcad-ai/feedpak-player/issues/2)). 👻 Ghost notes, 🎯 markers and the 👂 Live count used to miss most notes played through distortion or fuzz (a clipped signal hardly gets louder when a new note starts), hammer-ons and pull-offs, and notes from a quiet input; a delay pedal's repeats counted as extra notes, and a note still ringing under the next one often read as the wrong pitch. Now: notes are also found where the **sound changes** (spectral flux and a longer-lasting spectral change, with thresholds that adapt to the playing), the **tab's notes are looked for harder where they're due**, each pitch is read **with the expected note as a hint** (fixing octave-type mistakes and a note ringing under the new one; a wrong note played clearly still reads as played), echoes, the same note again and string noise away from the tab's notes aren't extra notes, and a note whose pitch **can't be read clearly** (heavy distortion) is judged on its **timing only**, labelled *pitch unclear* on the ghost, the hint card and the summary — not counted wrong or missed. On a benchmark of synthetic guitar and bass phrases through 19 kinds of effects (`tools/bench-detection.mjs`), the notes a perfect player is credited with went from 56 % to 95 % on average in recorded takes and from 55 % to 94 % in 👂 Live (distortion 6 % → 85 %, fuzz 13 % → 90 %, a low input level 17 % → 94 %, delay 60 % → 83 %, legato runs with distortion 13 % → 100 %); clean playing is better too (83 % → 96 %: a note ringing under the next one no longer pulls its pitch off). 👂 Live uses about 3 % of one CPU core for it.
- **The drums highway in the lane layout drummers know from rhythm games.** The kick is now a bar across the whole highway (in the kick's colour), and the pads run left to right **snare · hi-hat · high tom / ride · floor tom / crash**, so a lane can carry a drum and a cymbal: drums are pads, cymbals discs with a bell, an open hi-hat a ring, told apart at a glance. The mid tom shares the high tom's lane, every crash (splash, china too) the floor tom's, the ride bell the ride's; cowbells and other percussion get a narrow lane on the right, only when the song has them. Pads and the targets on the hit line show the same drum icons as the Scrolling and Page views instead of letters, the kick's target is a bar across the line. Your drum colours, the kit mapping, loudness, accents and ghost notes apply as before. Prefer a lane per piece, as the kit sits? **⚙ Settings → Drums highway → Full kit**.
- **⚙ Settings in tabs, and wider.** Settings had become one long list; it's now split into **🎨 Display**, **🎯 Playing & feedback**, **⏱ Audio & calibration**, **🔄 Sync & backup** and **🔒 Privacy & about**. It opens at the tab you used last (remembered on this device), the arrow keys move between tabs, and on a large screen the window is wider, in two columns; on a phone and in the Portrait layout it's a full-width sheet. Links into Settings (the ⏱ timing only badge, the sync / Drive dot on ⚙) open the right tab.
- **See at a glance when only timing is judged.** With **Judge timing only** on, a small **⏱ timing only** badge now stays in the tab's corner whenever notes are judged on screen (👂 Live, or a take shown), in every view including the Highway and Portrait; the record bar's take summary starts with it and the Portrait layout shows a ⏱ at the bottom. Click it to open the setting.
- **Switch between takes from the main screen.** With two or more takes, the **🎙 My take** tab has **‹ ›** arrows and shows which take it is (e.g. *2/5*), the **,** and **.** keys do the same, and in the Portrait layout **‹ 2/5 ›** sits at the bottom while the take is shown, all without opening the 🎙 Takes list. While the song plays, it keeps playing from the new take.

## 0.27.0 — 2026-11-07

### New
- **Karaoke songs: UltraStar files open in Tabloop.** Open an UltraStar song folder (the `.txt` song file of UltraStar Deluxe, Vocaluxe or Performous, its audio and cover) with **Open folder**, drop it on the window, or open a zip of it (or just the `.txt`, without sound) with **Open file**. It opens on the **🎤 Vocals** tab alone, with the melody, the lyrics joined into words and lines, the cover and the audio (separate vocals and instrumental tracks too, when the song has them). Golden notes are drawn in gold; rap and freestyle notes have no pitch, so 🎙 Sing only checks that you sing them on time. Duets get a singer menu in the vocal bar: the melody and the lyrics switch together, remembered per song. Old song files in Windows (Latin-1) text, relative timing and tempo changes are read too. **💾 Save pack** keeps the song as a feedpak (audio, melody, lyrics), so it opens like any other song. Lyrics and melodies are usually copyrighted: only open files you have the right to use.
- **Rock Band / Clone Hero / YARG vocals.** A chart loaded with **＋ Drums** now also brings its vocals: `PART VOCALS` and the harmonies `HARM1`–`HARM3` become the 🎤 Vocals tab's melody and lyrics (one part per harmony, each with its lyric track), with the chart's phrases as lyric lines, slides held, and talky / unpitched notes judged on timing only by 🎙 Sing. They move with the drum sync offset, and **💾 Save pack** writes them into the song.

## 0.26.0 — 2026-11-07

### New
- **Highway for drums, keys and vocals.** The Highway view now draws every kind of part, not only guitar and bass tab. **Drums** get a lane per kit piece the song uses, left to right as the kit sits in front of you (crash, hi-hat, snare, kick, the toms, ride), in your drum colours: drums are pads, cymbals flat discs, an open hi-hat a ring, with the piece's letters; louder hits are bigger, accents get a light rim and ghost notes are small with a dashed edge. The kit mapping and the drum sync apply as in the chart. **Keys** and MIDI instruments fall onto a piano keyboard at the hit line, each note on its key (black keys narrower), long notes as long bars, the keys lighting up as they sound; Pitch moves them. **🎤 Vocals** show the melody on a pitch highway, and with 🎙 Sing your voice as a line coming out of the hit line.
- **Split-screen highways for several players.** Show several parts (the **+** on their tabs, any mix of guitar, bass, drums, keys and vocals) and the Highway splits into one highway per part, side by side and equal in width, each with its own name at the top, lanes and hit line, all moving together, so two or more players can each follow their own part. Up to 4 fit on a computer, 2 on a phone (also in the Portrait layout); more are named at the top (Scrolling and Page still show them all). Tap a part's name to swap it with its neighbour. Ghost notes and 🎯 markers stay on their own part, clicking any highway jumps to that moment, and the lyric line runs once under them all.

## 0.25.0 — 2026-11-07

### New
- **Judge timing only (ignore pitch).** For when you're sure of the notes and want to train speed and timing: tick **Judge timing only** in ⚙ Settings → ⚖️ How forgiving the judging is, or press **⏱ Timing only** in the 👂 Live bar (the two stay in sync). With 👂 Live and recorded takes, a note played on time then counts as right whatever its pitch: only *early*, *late*, *missed* and *extra* count, never flat or sharp. Ghost notes are coloured by timing (green on time, yellow a little off, red clearly off, like the markers), 🎯 markers show only 🎯 ◀ ▶ ✕, the live box says *timing only* and take summaries start *Timing only:* without the pitch part; the card on a ghost or marker still shows the pitch you played, marked *not judged*. What's on screen is judged again as soon as you switch. Off by default; remembered, exported and synced. 🎙 Sing is judged on pitch by nature and isn't affected. [#3](https://github.com/bazarcad-ai/feedpak-player/issues/3)

### Improved
- **The anonymous usage counts (hosted site only) now also include rough practice patterns, still without any user ID.** Once a day, for the last day you used Tabloop, a few counts with ranges only: about how long you practised (e.g. 10–20 minutes), in how many sessions and the longest one, how many different songs, and which features you used (e.g. the tuner, loops, the speed trainer, slowed-down playback, the metronome); once a week, on how many of the last 7 days you opened the app. This shows how Tabloop is used (how many people practise 10–20 minutes a day, how many use the tuner …), never who: no cookies, no user ID, no song names, no settings. As before they're never sent from a downloaded copy, respect Do Not Track and Global Privacy Control, and stop when you untick **⚙ Settings → Send anonymous usage counts** (which also deletes the day gathered so far). The [privacy policy](https://tabloop.github.io/privacy.html) lists them.

## 0.24.2 — 2026-11-07

### Fixed
- **🕘 Recent stays on each device: it's no longer copied to Google Drive, the sync folder or the settings export.** Each computer, phone or tablet opens songs from its own files and its own library folder, so another device's list didn't work there and overwrote this one's. Now each device keeps its own Recent list. Backups and sync files made by earlier versions still contain the old list: it's ignored (it never replaces this device's list and isn't listed in the Google Drive differences window), and the next backup or sync leaves it out. Importing an older settings export keeps this device's list too. The 📚 Library's folder and song list already stayed on each device; its sort order is a preference and still syncs. [#1](https://github.com/bazarcad-ai/feedpak-player/issues/1)
- **Playlists synced from another device find their songs even when its library folders are organised differently.** A playlist song is looked up in this device's library by its place in the library folder, and now also by title and artist, so it no longer shows as *missing* just because the folders differ.
- **📈 Practice time now counts only while the song is actually heard, in real time.** It used to count from the moment ▶ was pressed: the count-in, the short wait before the sound starts and time with the audio stopped by the system (e.g. a phone's background tab) were counted as practice. Now the time comes from the audio clock: it counts while the song plays in every mode (loops and loop chains, 👂 Live, ⏺ recording, 🎙 Sing, the speed trainer, ▶ Play take), at real time whatever the speed (5 s at 50 % counts 5 s), and with the page in the background as long as the song keeps playing; never while paused, during the count-in, while the audio is suspended or with the app just open. [#6](https://github.com/bazarcad-ai/feedpak-player/issues/6)

## 0.24.1 — 2026-11-07

### Fixed
- **Safari (Mac, iPhone and iPad): the input opens again.** 🎸 Tuner, ⏺ Rec, 👂 Live, 🎙 Sing and ⏱ Calibration failed with *Couldn't start recording: AudioSession category is not compatible with audio capture.* Safari only lets a page use the microphone while its audio is set up to play *and* record, and the app switched to that only after asking for the microphone. It now switches just before opening the input, and back to plain playback (which on iPhone/iPad keeps the song playing with the silent switch on) as soon as nothing uses the input any more, or when opening it fails. If Safari still refuses, the message says so plainly (*Safari couldn't switch the audio to play-and-record…*) instead of the technical text.

## 0.24.0 — 2026-11-07

### Improved
- **🎚 Mixer: Reset.** A **Reset** button in the mixer's header (next to ✕) puts this song's mix back to its defaults, after asking (*Reset the mixer for “Song”?*, with **Cancel** focused; Cancel or Escape changes nothing): every level — Master, the song and this song's parts (also in the Tracks panel), the tab synth, MIDI drums and instruments, My take and the metronome (which the count-in follows) — and every mute and solo cleared. Your *Song / Tab / Both* choice, the Metronome switch and the other songs' part levels are kept. The input level is set per device, so it's kept too unless you tick **Also reset the input level** (100 %, monitoring off).
- **⏱ Calibration now works out the settings for you and proposes them.** After tapping (step 1) and after Automatic or Play along (step 2), a result card shows what was measured, how steady it was (e.g. *taps varied by ±10 ms · 12 of 12 clicks and 12 of 12 flashes used*), what the browser already reports, and the proposed setting (e.g. *Screen: +80 ms*, *Input (Line In): −60 ms*) next to the current one, with **Use this** (preselected), **Keep current** and **Try again**. If your taps or notes varied too much, it says so (*your taps varied by ±54 ms, too much to be sure*), suggests trying again and doesn't propose the value by default. Step 3, now **Apply & check**, lists both proposals side by side with the values used now; **Apply all** uses them straight away so the check runs with them, and **Save** keeps them (with any fine-tune). Nothing is stored until you press Save: closing the window puts the old values back. A skipped step proposes what's known and is labelled as an estimate. With Bluetooth headphones the window suggests doing step 1 (**Go to step 1**), and if Automatic hears none of its clicks, it suggests **🎸 Play along** instead.
- **Speed from 10 % to 200 %, and you can type an exact speed.** The speed now goes down to 10 % and up to 200 % (was 25–150 %), with the pitch kept. The slider moves in 1 % steps below 50 % and 5 % steps above, so the slow speeds get more room; **− / +** still step 5 % (hold Shift for 1 %). Click the **%** box and type a speed (e.g. 37), then Enter (or click away); Esc cancels, ↑ / ↓ change it by 1 % (Shift: 5 %), and a value outside 10–200 % is set to the nearest end. **Double-click the % box to go back to 100 %** (a single click now lets you type). The speed trainer, takes (*Play at 37 %*), practice stats, 👂 Live, the metronome, count-in, tab synth, lyrics, highway and the Portrait transport all follow. Below about 20 % drums and attacks sound smeared: that's the time-stretch at work.

### Fixed
- **No more "The player didn't start" message when the app is just slow to open.** With a sync folder or Google Drive linked (or on a slower computer) the app can take a few seconds to start, and the red message could show up although everything then worked. Now it only appears when the app really couldn't load; if starting takes unusually long (15 seconds), a calmer *Still starting…* note shows instead, and it goes away by itself as soon as the app is ready.
- **Songs in iCloud Drive (and other folders Chrome or Edge won't open) can be opened again.** In Chrome and Edge, **Open file**, **Open folder** and 📚 Library → **Choose folder…** use the browser's own picker, which refuses some locations as "system files" (on a Mac, the top of iCloud Drive or the Library folder), or hands over a file it then can't read. The message now has a button **Choose … with the standard dialog**, which has no such limit, and the song opens. Songs opened that way can't be reopened from 🕘 Recent by themselves: pick them again next time. Files stored online only still get the clear "make it available offline" message.
- **Technique marks no longer pile onto the notes in very busy bars** (fast solos, in the Scrolling, Page and Highway views). Accents, P.M., H / P, T, P.H., tremolo marks and bend amounts now never cover a fret number or each other: when a bar is crowded they stack in rows above the tab, move a little to the side or get a bit smaller, and the least important ones (accents first) are left out when there's really no room. A fast hammer-on / pull-off run gets one slur and one label (H, P or H/P) instead of a letter on every note, and bend arrows and slurs pass behind the fret numbers instead of across them.

## 0.23.1 — 2026-11-06

### Improved
- **Phones and tablets held upright now use the Portrait layout automatically; turn it off in ⚙ Settings → Layout.** *Automatic: use Portrait when the screen is taller than wide* is now on by default, so the song gets most of the height out of the box on an upright screen; turning the screen sideways, or a computer's landscape window, keeps the Standard layout as before. Untick Automatic to always use the Layout chosen above it (Standard unless you pick Portrait). If you already chose a layout in 0.22.0, your choice is kept.

## 0.23.0 — 2026-11-06

### New
- **⏱ Calibration:** a short guided calibration of what you see, hear and play on your setup, in ⚙ Settings → *Calibration* and behind **⏱ Calibrate** in the record, live and vocal bars. The first time an input is opened, the app suggests it once. Three steps (about a minute), each one skippable and each showing its result in ms:
  1. **Sound & screen:** tap along with 12 clicks you hear, then with 12 flashes you see. The difference is how much later the sound reaches you than the picture (Bluetooth headphones often add a lot), and the cursor and notes are drawn that much later. **▶ Preview** shows a marker that should reach its line on each click, with a slider to fine-tune it.
  2. **Your input:** **🔊 Automatic** (the mic near the speaker listens for the app's clicks) or **🎸 Play along** (play a short note on each of 8 clicks after a count-in; works with headphones and audio interfaces). The result becomes the input's nudge for ⏺ Rec, 👂 Live and 🎤 Sing.
  3. **Check:** play on 8 clicks. Each note shows as 🎯 or ◀ / ▶ with its ms, plus the median, while a cursor crosses each beat as you hear it. **Looks right** keeps it; **Adjust** gives a fine-tune slider (the markers move as you drag) and **Use median**.
- The values are kept **for each output and input device** in this browser only (never exported or synced). ⚙ Settings lists them and has **Reset**. A warning shows for Bluetooth outputs and recommends wired headphones or an audio interface. Until you calibrate, nothing changes.

### Improved
- **🎚 Mixer: bigger, scrollable, and steady.** With many channels (the song's parts and stems, MIDI instruments, My take, the input…) the mixer no longer runs off the screen: it's wider, as tall as there's room for (when there isn't room below 🎚 Mixer it takes the window's full height beside the button), and its channels scroll inside it while the title and a new **✕** stay put. On a phone and in Portrait it's a sheet along the bottom, up to about 85 % of the height, scrolling inside. The **Input** section keeps one size: the level meter, its readout (*—* when silent) and the Clip light always take their room and the *you hear yourself … ms late* line keeps its space while monitoring is off, so nothing in the mixer moves while you play, stop, clip or switch Monitor.

## 0.22.0 — 2026-11-06

### New
- **Portrait layout (optional), for phones and tablets held upright or a monitor turned on its side.** In ⚙ Settings → *Layout*, choose **Portrait (more room for the song)**: the tab, page or highway gets most of the height (about 77 % on a phone, 86 % on a tablet, 90 % on a tall monitor). The header and the toolbar rows fold into one slim bar with the song title, its parts (scrolling sideways) and a **☰** menu holding everything else; Sections, Saved loops and Tracks open over the tab (✕ or a tap on the tab closes them); ▶, seek, the time, ⟲ Loop and speed stay at the bottom, and the loop, record and live bars appear as one compact row each while they're on. **Automatic** uses Portrait while the screen is taller than wide and goes back to Standard when you turn it; Portrait chosen on its own stays when you turn the screen. Kept per device (not synced). Standard stays the default and is unchanged.
- **🎚 Mixer → Input: set the level of your microphone or instrument, and hear yourself.** While the input is open (🎸 Tuner, ⏺ Rec, 👂 Live or 🎙 Sing), the mixer has an **Input** section: a **Level** (0–400 %, double-click for 100 %) that applies to everything that listens — new recordings (it's part of the take), the tuner, Live and Sing — with a level meter and a **Clip** light, remembered for each input device. **Monitor** plays your input through the app with its own volume: off by default (and after every reload), with a reminder to use headphones and how late you hear yourself. It doesn't change your recordings, and it stops when the input is closed.

### Improved
- **🎙 Takes: delete several takes at once.** Tick takes in the list (or **Select all**; it shows how many are selected) and press **Delete selected**, or **Delete all** to clear this song's takes (other songs keep theirs). Before anything is deleted, a window says how many takes and how long they are, e.g. *Delete 3 takes (2:14)? This can't be undone.*, with **Cancel** focused; Cancel or Escape deletes nothing. Deleting a single take with ✕ asks in the same window. If the selected take is deleted, the newest one left is selected; if a deleted take was playing, playback stops.
- **Ghost notes and 🎯 markers explain themselves:** hover one (or tap it on a phone or tablet) and a small card shows what the tab expected and what you played, e.g. *Expected D3, A string, fret 5 · Played C#3 · Pitch −30 ¢, flat · Timing +25 ms, on time · ♭ Flat*. Chords show their name and notes (timing only), missed notes say *not played*, extra notes say *Extra note: you played E3 (not in the tab)*. In tune, on time, flat and sharp follow your ⚖️ forgiveness setting, with the same colours as the ghosts and markers. It works in Scrolling, Page and Highway, while playing or paused, and replaces the short browser tooltip. On touch screens, tapping a ghost shows its card instead of jumping there; tap anywhere else to hide it (and jump, as before).

## 0.21.0 — 2026-11-06

### New
- **Google Drive keeps several computers in step.** Each time the app starts while you're signed in to Google (or right after you click **Reconnect**), it compares this browser with your Drive backup. Nothing differs: nothing happens. Only one side changed since they were last in step: the app takes the newer side by itself, another computer's changes come here or this browser's go to Drive, and a small message says what it did, with **Undo**.
- **When both changed, you choose.** A window lists what differs. For practice stats: **Combine** (every session from both computers, each counted once), **Use Google Drive's** or **Keep this browser's**. For each setting, saved loop or song's state: this browser's or Google Drive's value, with when each changed (the newer one is selected), or all at once. Then: **Also update Google Drive with the result?** (Yes by default).
- **A new computer asks first:** the first time a browser that already has data connects to a Google Drive that has a backup, the same window opens. Settings you never changed on that browser (its defaults) are grouped in one folded row with Google Drive's value selected, so only real differences stand out. A browser with nothing of its own yet simply takes the backup.
- **Restore from Drive** now opens the same window with Google Drive's side selected, so you can keep some things from this browser instead of replacing everything. **Back up now** still backs up; if another computer changed something in Drive since, it's merged in first instead of being overwritten.

### Improved
- **Practice history from several computers adds up exactly through Google Drive**, as it already did through the sync folder: the backup now keeps each browser's own share (and when each setting and saved loop changed, deletions included). Backups made by older versions can still be read and restored; when merging one of those, sessions on the same day and song count once (the larger of the two) instead of twice. Backups made by this version can't be restored by older versions (0.20 and before): update the app on your other computers too.
- **Saved and synced at more moments:** opening or changing songs, adding or editing instruments, saving, renaming or deleting a loop, changing a setting, tagging a song, editing a playlist and closing a window now save at once and make the sync folder and the automatic Google Drive backup write within a few seconds. A burst of changes still makes one write.
- **Sync folder and Google Drive together** agree on what's newer and never count a session twice.
- **Solo silences the metronome and the count-in too:** while a part is soloed in the Tracks panel you hear only that part. The Metronome and Count-in settings stay as they were and come back when the solo ends; solo is still not remembered.
- **Songs that have both a full mix and separate stems now play the separate stems,** so each part can be muted, soloed and set on its own in the Tracks panel (before, these songs played the full mix while every stem was on). The full mix is used when a song has no separate stems, or when one of them can't be read or decoded; the Tracks rows then say "in the full mix (stems couldn't load)".
- **Highway:** techniques are now drawn as on the tab in Scrolling and Page, with the same marks turned to fit the highway: bends as an arrow rising from the note and leaning across the lane, with ¼, ½, full, 1½ or PB; hammer-ons and pull-offs as a slur from the note before with H / P; slides as the tail leaning towards the fret they end on, with its number; vibrato as a wave along the tail; P.M. with a dashed line over a palm-muted run; T, P.H., tremolo slashes, accents, x and <12>. Labels never cover a fret number and stay readable on a phone.

## 0.20.0 — 2026-11-06

### New
- **Tracks panel:** a new side panel (the **Tracks** button next to *Saved loops*) lists the song's parts: each tab part (Lead, Bass…), Keys, Drums, MIDI instruments, 🎤 Vocals and **My take** once a take is selected. Each row has an 👁 eye to show or hide the part on screen (the same as clicking or shift-clicking its tab; one part always stays shown), **M** to mute it, **S** to solo it and a volume slider (double-click for 100 %). Clicking a part's name shows only that part.
- A part's sound is whatever plays it: its stem of the recording in *Song*, the tab synth in *Tab* (while it's shown), both in *Both*, its MIDI-instrument synth, the drum synth or your take. Each row says what that is right now, e.g. "guitar stem + tab synth", and says so when no stem matches the part. Two parts that share a stem (Lead and Rhythm on the guitar stem) both say so: the stem goes silent only when both are muted.
- Stems that belong to no part (e.g. *other*, the rest of the band) are listed under **Other stems**, with their own mute, solo and volume.
- **Solo** plays only that part; Cmd/Ctrl-click S to add more parts. The metronome and the count-in keep playing. Solo is only for listening: it doesn't change the saved levels, and it isn't remembered.
- The part levels are remembered for each song. They work inside the 🎚 Mixer's channels (Song, Tab synth, MIDI drums, MIDI instruments), and the Mixer lists the same levels under **This song's parts**: changing one changes the other. My take's row is the Mixer's My take channel.
- **The side panels are stacked:** with more than one of Sections, Saved loops and Tracks open, each shows its title bar and only one is expanded. Click another title (or press Enter on it) to expand it, and the one that was open folds up. The toolbar buttons still open and close each panel, the expanded one is remembered, and 💾 Save brings Saved loops forward. To see them all at once as before, with the bar to drag between Sections and Saved loops, choose ⚙ Settings → *Side panels* → **Side by side**. On phones it works the same way, in the sheet over the tab.

### Improved
- **Techniques drawn like printed tab**, in the Scrolling and the Page view, in the string's colour: **bends** as a curved arrow up from the note with the amount (*¼*, *½*, *full*, *1½*, *2*), **releases** as an arrow down, **pre-bends** as a straight arrow up marked *PB*, and bend curves drawn as their shape; **hammer-ons / pull-offs** as an arc from the note before with a small *H* / *P*; **taps** as *T*; **slides** as a line rising or falling towards the next fret, and a slide off a note as a short slanted line after it; **vibrato** as a clearer wavy line; **tremolo picking** as three slashes; **pinch harmonics** as *P.H.*; **palm mutes** as *P.M.* with a dashed line over the run of palm-muted notes; **accents** as *>* (once per chord). Harmonics stay *<12>* and muted notes *x*.
- The marks are placed so they never cover a fret number, a chord name or each other, grow with the Page view's text size (**A−** / **A+**), and stay readable on phones.
- **Help:** a new *Reading the tab* section lists the symbols, with a picture.

## 0.19.0 — 2026-11-06

### New
- **Highway view:** a third view next to **Scrolling** and **Page**. The notes come down towards you in one lane per string, coloured like the strings (lowest string on the left, as on a chord diagram), to a red hit line near the bottom, and light up as they cross it. Each note is a block with its fret number, with a tail for how long it rings; chords get a bar across their strings with the chord's name. Beats and bars are lines across the highway, sections are labelled, and a loop is shaded.
- At the hit line, each string's target shows the fret of its next note, and the **fret** number beside it is your hand position (the lowest fretted note coming up).
- Techniques are marked simply for now: bends (an arrow with ½ / full), slides (the tail leans towards where it goes and ends on the target fret), H / P / T, PM, vibrato (a wavy tail), muted notes (x) and harmonics (<12>).
- It follows **Zoom** (how fast the notes come), the speed, loops and **Pitch**, shows ghost notes or 🎯 markers from 👂 Live or a take, and the current lyric line under the highway when lyrics are **In tab**. Click above the hit line to jump to that moment, or drag the notes up or down. Several guitar / bass parts sit side by side (as many as fit); drums, keys and vocals stay in the Scrolling and Page views. Remembered like the other views.

### Improved
- **Practice and song settings are saved more often**, so less is lost if the browser or the computer closes unexpectedly. In this browser they're saved every 2 seconds while you play (was 5), and at once when you pause, at the end of each loop pass, at the end of the song and when you jump to another place.
- **The sync folder is up to date sooner:** practice is written 5 seconds after it changes (was 15), at most 20 seconds apart while you keep playing (was a minute), and also when you pause or leave the page.
- **Automatic Google Drive backup during long sessions:** it still runs half a minute after you stop practising, and now also at least every 2 minutes while you keep playing, and when you pause or leave the page. Only while signed in, and only when something changed; it never asks you to sign in.
- **Option to start new songs with the lyrics hidden:** ⚙ Settings → *Lyrics* → **Show lyrics for new songs** (on by default). Songs you've already opened keep their own choice, and the **Lyrics** box in the toolbar still shows or hides them for each song. When lyrics are hidden, the 🎤 Vocals tab says how to show them.

## 0.18.2 — 2026-11-06

### Improved
- **Demo song "First Riff" has its own Keys part:** soft chords that follow the song and sit under the melody (verse Em – Em – C – D, chorus Em – G – Am – D). Show **Keys** to hear it.
- **Terms of use:** a short, plain-English terms page at https://tabloop.github.io/terms.html (free, as is; only open songs you have the right to use; optional services such as Google Drive have their own terms). Linked next to the privacy policy on the welcome screen, at the top of ⚙ Settings and in the help, and from the privacy policy.

### Fixed
- **The Tab synth now plays guitar techniques** instead of a plain note each time. Bends glide up to the bent pitch (pre-bends, releases and bend curves too), slides glide to their fret, and an unpitched slide rises or falls and fades out. Hammer-ons, pull-offs and taps change the note on the ringing string without a new pick. Vibrato wobbles the pitch, palm mutes are short and dull, muted notes are a dead thunk with no pitch, and harmonics ring like a bell at the harmonic's own pitch (a harmonic at fret 7 sounds an octave above the fretted note; pinch harmonics squeal higher). Tremolo picking re-picks and accents are louder.
- These follow the playback speed (at 50 % a bend takes twice as long, like the slowed-down song) and the song's **Pitch** setting.
- The Tab synth's notes are also a little more in tune (they were about 5 ¢ flat on the higher strings).

## 0.18.1 — 2026-11-06

### Improved
- **Help and guide brought up to date:** new sections for the 🎸 Tuner, 👂 Live, ghost notes or 🎯 markers, how forgiving the judging is, and the 🎤 Vocals tab, with new screenshots; the Drive "backup paused" notice, "A song or folder won't open" and "When does Tabloop use the microphone?" in the FAQ. The demo video now shows 👂 Live with 🎯 markers and singing in the 🎤 Vocals tab.
- **Demo song "First Riff"** now has a vocal melody, so its 🎤 Vocals tab has something to sing along to.

## 0.18.0 — 2026-11-05

### New
- **🎤 Vocals tab (karaoke):** songs with lyrics, a vocal melody or a vocals stem get a **🎤 Vocals** tab next to the arrangement tabs. It shows the vocal melody as bars on a pitch axis (like the keys piano roll), the lyrics in time under it and in the karaoke bar, following playback, loops, speed and **Pitch** (move the song up or down to suit your voice: the melody moves with it). Show it alone, or beside the tab with **+** / shift-click.
- **Where the melody comes from:** a pack's own vocal pitch files (`vocal_pitch.json` and its pitch contour, drawn as a thin line), **🎹 Melody from MIDI…** (any track of a MIDI file, marked *Vocal melody* in the ＋ Instrument / ⚙ Instruments dialog, with the file's sync offset), or **🔎 Find the melody from the vocals**, which finds it automatically from the pack's vocals stem (approximate; done once per song, then kept). A song with several lists them in the vocal bar. A song without any says how to add one.
- **💾 Save pack keeps the vocal melody:** a melody from MIDI or found from the vocals is written into the saved copy as the pack's own `vocal_pitch.json` (feedpak spec §7.2; a found one with its `pitch_extraction` note), synced and at the song's own pitch, as tab is saved. A pack that already has its own vocal melody keeps it unchanged.
- **🎙 Sing:** turn it on in the vocal bar and sing along: your voice is drawn as a line on the melody, green when in tune, blue when flat, orange when sharp, and each note is judged on its pitch (not its timing). The judging ignores the scoop into a note and the slide out of it, and takes the middle of a note with vibrato. Singing has its own, wider pitch limit in ⚙ Settings → *How forgiving* → **🎤 Singing**: Relaxed ±50 ¢, **Normal ±30 ¢** (the default), Strict ±20 ¢, or Custom (5–100 ¢); the instruments' limit is unchanged, and what's shown is judged again when you change it. Singing an octave off counts as right (a man singing a woman's melody, say). A score shows notes in tune out of notes sung, this pass and the best. The microphone opens only while 🎙 Sing is on and nothing is recorded or stored.

## 0.17.0 — 2026-11-05

### New
- **⚖️ How forgiving the judging is:** choose in **⚙ Settings** how far off a note can be and still count as right — **Relaxed** (±60 ms, ±25 ¢), **Normal** (±40 ms, ±15 ¢, as before and the default), **Strict** (±25 ms, ±10 ¢), or **Custom** with your own values (timing 10–150 ms, pitch 5–50 ¢). **Reset to Normal** puts it back.
- One setting for 👂 Live and recorded takes: the ✓ and X/Y counts, early / late / flat / sharp, ghost colours, the 🎯 markers (yellow up to twice the limit, red beyond), take summaries and timing marks all follow it. Change it and what's on screen is judged again right away, including the loop's last passes in the live box. Remembered, and exported and synced with your settings.

### Fixed
- **Google Drive backup no longer stops without telling you.** Google's sign-in in the browser lasts about an hour. With automatic backup on, the app now tries to renew it a few minutes before it ends, without a click or any Google screen. Browsers often block this (it needs Google's popup), and when it doesn't work a small **Google Drive backup paused** notice appears in the corner, outside Settings, with when the last backup was and a one-click **Reconnect**; ⚙ gets a dot. It shows once each time the sign-in is lost and can be dismissed with ✕.
- **Practice done while Drive was disconnected is backed up when you reconnect**, from the notice or from Settings, also after a reload or in a new tab. Before, reconnecting from Settings didn't back it up until you practised again.
- Nothing changes if you never linked Google Drive or back up by hand.
- **Songs from some folders didn't play:** an unpacked song folder or a song file whose file names have accents (*Café*, *Ünïcode*) failed with "File missing from pack" when it was made or copied on a Mac, which spells accents differently from the song's manifest. These songs now open and play.
- Songs whose manifest names a file in different upper/lower case (*Stems/Guitar.ogg* for *stems/guitar.ogg*), or with `./` in front, now open too, as they do on Mac and Windows disks.
- **External drives:** the hidden `._` files a Mac leaves on USB drives and network shares no longer show up as broken songs in the 📚 Library, and are no longer taken for a song's drum chart.
- **Files the browser can't read** now say why and what to do, instead of the browser's "could not be read, typically due to permission problems": a song stored *online only* in OneDrive, iCloud Drive, Google Drive or Dropbox (make it available offline), a file moved or deleted since it was opened (also when reopening from 🕘 Recent), a Library song changed since the folder was picked (pick the folder again), and, on a Mac, a folder the browser isn't allowed to read (Privacy & Security settings).
- One unreadable file no longer stops everything: a song folder opens even if an unrelated file in it can't be read, and a Library scan lists every other song, marking only the unreadable one.
- Picking a folder that comes through empty (e.g. a link to another folder) now says so instead of doing nothing.

## 0.16.1 — 2026-11-05

### Improved
- **Privacy policy:** a full privacy policy at https://tabloop.github.io/privacy.html (what's stored where, the optional Google Drive backup and its app-folder-only access, the anonymous usage counts, how to delete your data), linked from the welcome screen, ⚙ Settings and the help.

## 0.16.0 — 2026-11-05

### New
- **🎯 Markers under the tab:** a second way to see how you played, for 👂 Live and recorded takes. Instead of ghost notes on the strings, each note of the tab gets a small marker in a row under the tab: **🎯** when you nail it (on time and in tune), a **triangle pointing to what was off** — ▲ sharp, ▼ flat, ◀ early, ▶ late — **yellow** when it's a little off and **red** when it's clearly off (more than twice the ±40 ms / ±15 ¢ limits), and **✕** for a missed note. When a note is off in both pitch and timing, the worse one shows; hover a marker for the numbers.
- Choose it in **⚙ Settings → Note feedback**, or switch with the new **👻 Ghost notes / 🎯 Markers** button in the live bar and the record bar. Ghost notes stay the default; the choice is remembered (and synced with your settings).

## 0.15.2 — 2026-11-05

### Improved
- **Page view:** fret numbers are bigger again: 50% bigger than in 0.15.0 (0.15.1 made them 30% bigger), with the same line spacing. The Scrolling view is as before.

## 0.15.1 — 2026-11-05

### Improved
- **Page view:** fret numbers are 30% bigger, so they're easier to read from a music stand; the line spacing and layout are unchanged, and A−/A+ still scale everything from there. The Scrolling view is as before.

## 0.15.0 — 2026-11-05

### New
- **👂 Live:** see how you're playing while you play, without recording. Press **👂 Live** (next to ⏺ Rec) and play along: every note of the tab is judged as it passes — right when it's on time (±40 ms) and in tune (±15 ¢), else early, late, flat, sharp or missed — and shown as ghost notes on the tab. A box in the tab's corner counts this pass, e.g. **14/16**, with what went wrong and your run of right notes.
- **Loop passes:** with a loop on, each pass is counted on its own, and the box shows the **last 5 passes** (*12/16 14/16 16/16…*) and your best. A pass you stop or skip out of isn't kept. Without a loop it counts from ▶ and over the last 30 seconds.
- Uses the record bar's input and latency compensation (and the input's nudge), works at any speed, and alongside ⏺ Rec. Nothing is stored; the setting is remembered in this browser.
- **Tuner in the live bar:** the live bar shows the input note, as the record bar does while ⏺ Rec is armed: the note, how many cents off, the frequency and the nearest open string.
- **Edit the MIDI instruments:** once a MIDI file is loaded, ＋ Instrument becomes **⚙ Instruments**, and the Instrument sync bar has **⚙ Edit instruments…** (it was 🎹 Tracks). Both open the tracks list with your current choices: switch a track between tab and piano roll, guitar and bass, change its tuning, or set it to *Not used*. The tabs, the sound and the remembered settings follow right away; the sync offset stays.
- **None / Suggested / Another file…** in the list: mark every track as not used (then pick the few you want), go back to the automatic choice, or load a different MIDI file.
- **🎸 Tuner:** the input note and the level meter without recording. The **🎸 Tuner** button (toolbar, next to 🎚 Mixer) opens your input just to listen: the record bar shows the input, its level and the note you play (name, cents needle, frequency, nearest open string), while the song plays or is paused. Nothing is recorded or stored. Arming ⏺ Rec while it's on carries on with the same input (no second permission prompt); disarming keeps the tuner. With both off, the microphone is released. It starts off on every visit, so Tabloop never asks for the microphone on its own.

### Improved
- **Phones:** ⟲ Loop and ⏺ Rec fit on screen next to the seek bar (on narrow phones ⏺ Rec ran past the right edge, and tapping it scrolled the bottom bar sideways).
- **MIDI file not in this browser:** when a song's instrument settings are here but the file isn't (settings synced from another computer, storage cleared), the tab shows **⚙ Instruments ⚠** and the dialog says so, lists what's remembered and asks for the file again; choosing it brings the parts back as they were.
- **Saved copies:** in a pack saved with its instruments, loading the same MIDI file again marks the tracks already in the pack (*Already in this pack as “Guitar”*) and leaves them out, so they aren't added twice; the copy keeps its own choices and starts at the saved parts' offset.
- A MIDI part stays on screen when another track is switched off or when it changes from tab to piano roll.
- **Remove** now also forgets the song's instrument choices, so the song doesn't bring them back or ask for the file.
- **Input note (tuner):** fixed width in the record and live bars, so ⏱ Calibrate, Only keep complete passes and the buttons after it no longer shift as the note changes or goes silent.

## 0.14.0 — 2026-11-05

### New
- **Input note (tuner):** while ⏺ Rec is armed, the record bar shows the note you're playing next to the level meter — the name with its octave (“A2”), how far off it is (“−12 ¢”) on a small −50…+50 ¢ needle, green within ±5 ¢, blue flat, orange sharp — plus the frequency and the nearest open string of the song's tuning (“A string”). “—” when the input is silent or not a clear note. It reads down to a bass's low E, against the song's reference pitch (A440, or e.g. A435 when the arrangement has a cent offset), so it agrees with the ghost notes. Handy to check the input works and to tune up before recording.
- **Lyrics:** songs with lyrics show a **Lyrics** box in the toolbar, and under the tab the line being sung, each syllable lighting up in amber as it's sung, with the next line dimmed. It stays in time at any speed, in loops and after seeks. Click a word or the next line to play from there. Songs without lyrics look as before.
- **In tab:** the words in a row along the tab, each at its time, in the Scrolling and Page views.
- **Lyrics languages:** when a song has several lyric tracks (original, a romanisation such as romaji, a translation), a menu switches between them. Right-to-left and Japanese, Chinese or Korean lyrics display correctly.
- Remembered per song: lyrics on or off, the track, and *In tab*.
- The demo song "First Riff" now has lyrics.
- **＋ Instrument:** add guitar, bass and keys parts from a MIDI file. A dialog lists the file's tracks (name, instrument, notes, range); choose what each becomes: guitar or bass tab (with a tuning; E Standard and 4-string E A D G by default) or a keys piano roll. Each part gets its own tab (*Guitar (MIDI)*, *Keys (MIDI)*…), can be shown beside the other parts, and plays on the new **MIDI instruments** mixer channel.
- **Automatic tab fingering:** low positions first, close to the previous hand position, chords on separate strings; notes the tuning can't reach are skipped and counted (Drop D brings back a low D).
- **Instrument sync:** nudge, type an offset, or align the first note to the cursor, like the drums. The MIDI's tempo changes are followed.
- **💾 Save pack** writes the instruments into the pack as real arrangements: guitar/bass tab files and a keys notation part, validated against the spec. The file, track choices and offset are remembered per song.
- **Notation-only parts** in packs (keys, `type: piano`) now show as a piano roll and play, instead of "not supported yet".

### Improved
- Opening another song right after changing a setting (speed, loop, lyrics…) no longer loses that change for the song you left.
- **Usage counts** (web version, anonymous, can be turned off in ⚙ Settings): new users, daily and weekly active users, loops saved, loop chains played and takes recorded are now counted too. Users are counted without any ID: the browser remembers that it was already counted (once ever, once a day, once a week), outside the settings, so exports, sync and *Reset settings* don't count it again. Nothing about the song, loop or take is sent. See the README's "Privacy and usage stats" for how to read the dashboard.
- Texts and help now just say **.feedpak** for song files. Older `.sloppak` files still open as before.

## 0.13.1 — 2026-11-05

### New
- **▶ Play take:** one click plays the selected take with the song: it stops recording, matches the take's speed, and plays the loop with your take when the take is in it.
- **‹ Prev / Next ›:** step through your takes (the bar shows *Take 2 (2/5)*); while playing, the new take starts right away.

## 0.13.0 — 2026-11-04

### New
- **Loop with your takes:** with a loop on (and recording not armed), ▶ plays the loop with your take on every pass. Choose in the record bar what each pass plays: **Selected take every pass**, or **Cycle through takes** — pass 1 plays the loop's take 1, pass 2 take 2… to compare attempts. Works with saved loops, and in a loop chain each loop plays its own takes.
- **Song + me / Only me / Only song:** quick solos in the record bar to hear just yourself, just the song, or both. The mixer's own settings stay as they are; changing the mixer ends the solo.
- **👻 Ghost notes:** what you played, drawn on the tab note by note — moved by your timing and coloured by your pitch: green within ±15 ¢, blue flat, orange sharp, with labels such as “−22 ¢ · +35 ms”. Missed notes show as hollow boxes and extra notes as faint rings. Chords get timing only. Works for guitar and bass (down to the low E), in the Scrolling and Page views; the **👻 Ghost** button shows or hides them.
- **Summary:** now pitch, missed and extra notes too, e.g. “Timing: 82 % within ±40 ms · Pitch: 74 % within ±15 ¢ · 3 missed”, also in the record bar.
- **Only keep complete passes:** a record-bar setting (off by default). When on, a loop pass is kept only if you recorded it from the loop start to the loop end; a pass cut short is dropped, and the bar says so. Takes without a loop are always kept.

### Improved
- **Timing marks:** low notes no longer show up as several notes (the note detector now checks a whole period of a bass's low E).
- **Tab synth:** an open string (fret 0) under a capo sounds at the capo.

## 0.12.0 — 2026-11-04

### New
- **⏺ Record takes:** record yourself playing along from a microphone or audio interface. Press **⏺ Rec**, pick the input, then ▶: you're recorded until you pause, one take per pass when a loop is on. Echo cancellation, noise suppression and auto gain are off, so instruments sound like themselves; use headphones so the song doesn't bleed in.
- **My take:** the selected take plays on its own mixer channel, in sync with the song, seeks and loops, at the speed it was recorded at (at other speeds it's silent and says so).
- **Take lane:** the take's waveform under the tab, in the Scrolling and Page views; show or hide it with the **🎙 My take** tab.
- **Timing feedback:** marks on the take lane show which notes you played early, late or on time (±40 ms), with a summary such as “82 % within ±40 ms”.
- **Latency:** the app compensates for the output and input delay; nudge any take by ±1 / ±10 ms, keep a default per input device, or measure it with **⏱ Calibrate**.
- **🎙 Takes:** each song's takes with date, length and speed; rename, delete, choose which one plays, download as WAV. Takes stay in this browser (up to 30 per song, 250 MB in all) and aren't part of the settings export or sync.

### Improved
- **Mixer on phones:** it opens along the bottom of the screen instead of running off the left edge.

## 0.11.1 — 2026-11-04

### Improved
- **Which browser?** The welcome screen notes that Tabloop works best in Chrome or Edge on a computer (shown only in browsers where something is limited), with a link to a new *Which browser?* section in the help that says what's limited in Firefox, Safari, on iPhone / iPad and in the downloaded file.
- **Credits open by default:** in ⚙ Settings, the credits and open-source licences at the bottom are now shown open; each licence text is still collapsed.

## 0.11.0 — 2026-11-04

### New
- **Help & guide:** https://tabloop.github.io/help/ explains opening songs, playing, looping, saved loops, the speed trainer, drums, practice tracking and settings, with screenshots and a 1-minute demo video. Linked from ⚙ Settings and the welcome screen.
- **Welcome screen:** until a song is open, a card offers **▶ Try the demo song**, Open a song file, the Library and Help.
- **Demo song:** “First Riff”, a short original song with lead guitar, bass and drums on separate tracks, sections and a drum chart, to try every feature.

## 0.10.1 — 2026-11-04

### Improved
- **Logo:** the loop now fills more of the icon, so it reads better in the browser tab and on the home screen.

## 0.10.0 — 2026-11-04

### New
- **New name: Tabloop** (shown as **tabl∞p**). Feedpak Player is now Tabloop; it still opens feedpak song packages. Your settings, practice history, sync folder and Drive backup carry on as before.
- **New logo:** an infinity loop drawn as tab strings, with a play-head dot.
- **New address:** https://tabloop.github.io/. The old address keeps working; each address keeps its own browser data, so use the sync folder, Export / Import or a Drive backup to move yours across.
- The downloaded file is now called `tabloop.html`.

## 0.9.1 — 2026-11-04

### New
- **Share song names (opt-in):** ⚙ Settings → *Also share the names of songs I play*. Off by default and per browser; when ticked, the usage counts list the songs you play by artist and title instead of an anonymous ID. Never file names.

## 0.9.0 — 2026-11-04

### New
- **Usage stats** (web version, anonymous): besides visits and unique users, the app now counts songs played and how many *different* songs are played, using an anonymous song ID, never the title. Opt out in ⚙ Settings; Do Not Track and Global Privacy Control are respected.
- **Tuning and 🥁 badges everywhere songs are listed:** Recently played (Library row and 🕘 menu), playlists, the ＋ Add songs picker and the 🔁 Loops dialog, as well as the Library cards.
- **What's new:** ⚙ Settings shows the version and a link to these release notes at the top. Credits and open-source licences are collapsed at the very bottom.

### Fixed
- **Google Drive stays connected after a reload.** Google's sign-in lasts about an hour; after that, one click on *Reconnect* (no password) continues, and a small note offers it when an automatic backup is due.

## 0.8.1 — 2026-11-04

### New
- **App logo:** a guitar pick with strings and a play button. It shows in the browser tab, as the iPhone/iPad home-screen icon, discreetly at the left of the header, and next to *About* in ⚙ Settings.

## 0.8.0 — 2026-11-04

### New
- **🔄 Sync folder** (Chrome or Edge on a computer): ⚙ Settings → *Sync folder* → **Choose sync folder…**, pick a folder that Google Drive for desktop, iCloud Drive, Dropbox or OneDrive syncs, then pick the same folder on your other computers. Settings, per-song state, practice history, saved loops and playlists stay in sync by themselves through one file, `feedpak-player-sync.json`. Changes from several computers are merged; no account or sign-in needed.
- **🕘 Recent:** the last 5 songs you opened, newest first, in the header and as a *Recently played* row in the Library. Replaces the old ↻ last-song button.
- **Tuning and drums badges:** library cards show each song's tuning (*E Std*, *Drop D*, *E♭ Std · capo 2*, *DADGAD (A432)*…) and a 🥁 badge for songs with a drum part. Filter chips by tuning or drums, and search matches tunings. The song header shows the tuning of the track on screen and 🥁 when there are drums. Songs without tuning info show no badge. Library lists saved by older versions are re-read automatically the first time the Library opens.
- **Sidebar:** sections and saved loops share the sidebar half and half; drag the bar between them to resize (double-click resets). A new **💾 Loops** toggle shows or hides saved loops, next to *Sections*.
- **⚙ Settings** (header): one dialog for string and drum colours, sync folder, export/import/reset, Google Drive backup, then about and credits. The 🎨 Colours button moved in here.
- **☁ Google Drive backup** is now configured on the web version: ⚙ Settings → *Google Drive* → **Connect Google Drive**.

## 0.7.0 — 2026-11-04

### New
- **Pitch:** transpose the song −12…+12 half-steps and keep the tempo, at any speed. The tab, notation, chord names and tab synth follow. *Tab: move frets* changes the fret numbers and moves notes to another string when needed; *Tab: retune strings* keeps the frets and renames the strings. Remembered per song.
- **⏮ Restart** (or **R**): back to the loop start and play.
- **Count-in:** one bar of clicks (1-2-3-4, accented 1) at the song's tempo and speed before playback starts, with big numbers on screen.
- **🏋 Speed trainer:** each loop pass a little faster. Set the start and end speed, the step, and loops per step; it stays at the end speed once it gets there.
- **💾 Saved loops:** name and keep loops per song, then rename, re-range, reorder or delete them. Tick several to **play them in a row** (× N each, optionally repeating) with a steady beat between loops. **🔁 Loops** lists every song's loops; it opens songs from the library and can be searched.
- **☁ Google Drive backup** (web version, optional): back up and restore settings and practice history to a private app folder in your own Drive. Not active until a Google client ID is configured.
- **Anonymous usage counts** (web version only, optional): cookie-free GoatCounter visit and song-open counts with an opt-out, respecting Do Not Track and GPC. Off until a site code is configured. The downloaded file never sends anything.
- Phones: when everything doesn't fit, the page scrolls instead of the controls covering the tab.

## 0.6.0 — 2026-11-04

### New
- **📚 Library:** choose your songs folder once. Every `.feedpak` (zipped or unpacked), subfolders included, is listed with cover, artist, length and parts. Search, sort, ↻ Refresh. The list is cached, and Chrome/Edge remember the folder.
- **🎵 Playlists:** create playlists, then add songs with ＋ Add songs, the ＋ Playlist on any song card, or ＋ Playlist in the header for the open song. Rename, reorder, remove, delete. ▶ Play, ⏮ ⏭ and Auto-advance. Songs missing from the library are skipped.
- **Settings are remembered:** view, zoom, text size, speed, mixer and colours globally. Tracks, drum part, position, loop and speed per song. ↻ reopens the last song (Chrome/Edge). ⓘ → Settings (now ⚙ Settings) exports, imports or resets.
- **Practice tags:** mark songs *Learning* or *Mastered*. The Practice dialog filters by tag and shows your repertoire.
- **Rock Band / Clone Hero drums:** ＋ Drums accepts `notes.mid`, `.chart`, `.sng`, zipped song folders and Xbox 360 CON/LIVE files. Supports Expert to Easy, pro-drums tom markers, 5-lane charts and disco flip. Picks up `song.ini` hints.
- On phones, the header buttons scroll sideways.

## 0.5.1 — 2026-11-04

### New
- **Drum chart icons:** each drum row has a small kit-piece icon next to its label (crash, ride, hi-hat, toms, snare, floor tom, kick, percussion), in both views.
- **Rock Band / Guitar Hero lane colours:** kick orange, snare red, hi-hat and high tom yellow, ride and mid tom blue, crash and floor tom green. The playing hit lights up white.
  - 🎨 Colours → *Drum colours* switches to a colour-blind friendly set or plain white, and remembers your choice.
- Page view drum rows are spaced a little wider to fit the icons.

## 0.5.0 — 2026-11-04

### New: MIDI drums

- **＋ MIDI drums:** load a `.mid` drum part onto any song. It shows as a **Drums (MIDI)** tab, alone or beside the guitar/bass parts, as a drum chart (× cymbals, ● drums), and plays through a built-in drum kit on its own mixer channel.
- **Drum sync:** line the MIDI up with the recording with ±10 / ±100 ms nudges, a typed offset, or **Align first hit to cursor**. Remembered per song.
- **🥁 Kit mapping:** choose which track/channel holds the drums and which kit piece each note plays, with a ▶ preview and a *Chart row* column matching the chart.
  - General MIDI and **Rock Band / Clone Hero** charts (`PART DRUMS`, Expert/Hard/Medium/Easy, pro-drums tom markers) are detected automatically.
- **💾 Save pack:** saves a copy of the song with the synced, mapped drums built in as a feedpak drum chart, so you set it up once.
  - All original files are kept unchanged, and the result validates against the feedpak spec.
- **Drum charts in packs** are now displayed and played; they were "not supported yet".

## 0.4.0 — 2026-11-04

### New: practice tracking (📈 Practice)

Recorded automatically while you play, and stored only in your browser.
- **Time:** per day, per song, per track and per speed.
- **Sections played through:** each section's start-to-end passes, in normal playback or once per loop pass. Each keeps its best and latest speed, and a best-speed-per-day trend.
- **Loops:** repeats and speeds for each loop, plus plays and full plays per song.
- **Streak:** consecutive days with at least 1 minute of playing. Today counts until midnight. The header shows 🔥 *n* while a streak is running.
- **Dashboard:** stat tiles, a one-year calendar of practice per day, and a song list that expands into sections and loops.
- **Export / Import** a backup to move history between browsers; **Reset** clears it.

### Fixed
- Pausing no longer nudges the cursor forward or skips a moment of sound on resume.

## 0.3.1 — 2026-11-04

### New
- **Page view text size:** **Text A− / A+** (70–250 %) makes fret numbers, string names, notation and spacing bigger or smaller. Click the % to reset. Remembered.
- **About & credits (ⓘ):** version, privacy note, and credits with full licence texts for all open-source software bundled in the app.

### Fixed
- For the first few seconds after opening the app, the Page view could stay at the top of the song instead of following the cursor.

## 0.3.0 — 2026-11-04

Five new features.

### New
- **Tab synth (Audio: Song / Tab / Both):** hear the tab notes played by a plucked-string synth instead of, or alongside, the recording. Notes keep their true pitch when slowed down and follow loops. Palm mutes, dead notes and harmonics sound different.
- **Metronome:** clicks on the song's own beat grid with an accented downbeat. It follows tempo changes, the speed setting and loops.
- **Mixer (🎚):** separate on/off and volume (0–150 %) for Song, Tab synth and Metronome, plus Master. Changes are smooth and remembered.
- **String colours (🎨):** Fee[dB]ack's default string colours, plus colour-blind friendly, pastel and monochrome presets, or pick each string yourself. A colour follows its named string across guitar and bass.
- **Rhythm:** note durations (stems, beams, flags, dots, rests) under the tab without the notation staff. Works in both views and combines with Notation.

**Tested** in Chrome and Firefox. Synth pitch and timing, metronome click timing and mixer levels were measured on the real audio output.

## 0.2.1 — 2026-11-03

Bug-fix release.

### Fixed
- **Looping at reduced or increased speed:** the audio kept playing past the loop end while the cursor jumped back. It now repeats correctly at any speed.
- **Space after clicking a loop adjust button:** it re-clicked the button (moving the loop) instead of playing or pausing. Shortcuts now work regardless of focus.
- **Firefox:** at non-100 % speed the cursor could run about 0.25 s ahead of the sound.

### Improved
- New audio engine on the browser's audio thread. Busy pages no longer make slowed-down audio stutter or drift, and the cursor matches the sound within about 20 ms at 25–150 %.

## 0.2.0 — 2026-11-03

Standalone build of Feedpak Player: a single HTML file with no install, and it works offline.


**What's in it**
- Open feedpak packs (zip or folder) and play them along with the tab
- Several arrangements side by side
- Scrolling or static Page view, with optional standard notation derived from the tab
- Pitch-preserving speed, 25–150 %
- Section list: click to loop, shift-click to extend; fine-tune the loop by bar, beat, 0.05 s, typed time or drag handles

**Shortcuts:** Space play/pause · ← → ±5 s · L loop on/off · [ ] set loop start/end
