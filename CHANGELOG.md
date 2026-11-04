# Release log

All notable changes to Tabloop (called Feedpak Player up to 0.9.1), newest first. Each version is published to https://tabloop.github.io/ and https://bazarcad-ai.github.io/feedpak-player-app/ (also downloadable as a single `index.html`).

## 0.10.1 — 2026-11-04

### Improved
- **Logo:** the loop now fills more of the icon, so it reads better in the browser tab and on the home screen.

## 0.10.0 — 2026-11-04

### New
- **New name: Tabloop** (shown as **tabl∞p**). Feedpak Player is now Tabloop; it still opens feedpak / sloppak song packages. Your settings, practice history, sync folder and Drive backup carry on as before.
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
- **📚 Library:** choose your songs folder once. Every `.feedpak` / `.sloppak` (zipped or unpacked), subfolders included, is listed with cover, artist, length and parts. Search, sort, ↻ Refresh. The list is cached, and Chrome/Edge remember the folder.
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
- Open feedpak / sloppak packs (zip or folder) and play them along with the tab
- Several arrangements side by side
- Scrolling or static Page view, with optional standard notation derived from the tab
- Pitch-preserving speed, 25–150 %
- Section list: click to loop, shift-click to extend; fine-tune the loop by bar, beat, 0.05 s, typed time or drag handles

**Shortcuts:** Space play/pause · ← → ±5 s · L loop on/off · [ ] set loop start/end
