<p align="center"><img src="docs/Horizon-Radio.png" alt="FH2 Horizon Radio" width="128" /></p>

# FH2 Horizon Radio

A free Windows companion for **Forza Horizon 2 on Azimuth**. Bring your YouTube music queue into the game's radio, with track information on the HUD and native Festival speaker effects.

<a href="https://github.com/P1upp3t/Forza-Horizon-2-Radio/releases/latest"><img src="docs/buttons/download-latest.svg" alt="Download latest release" height="48" /></a>&nbsp;&nbsp;<a href="https://ko-fi.com/puppetzim"><img src="docs/buttons/support-kofi.svg" alt="Support on Ko-fi — optional" height="48" /></a>&nbsp;&nbsp;<a href="https://puppetzim.itch.io/fh2-horizon-radio"><img src="docs/buttons/itchio.svg" alt="View on itch.io" height="48" /></a>&nbsp;&nbsp;<a href="https://github.com/P1upp3t/Forza-Horizon-2-Radio/issues"><img src="docs/buttons/report-issue.svg" alt="Report an issue" height="48" /></a>

<p align="center"><a href="README.md">English</a> · <a href="docs/translations/README.pt-BR.md">Português (Brasil)</a> · <a href="docs/translations/README.zh-CN.md">简体中文</a> · <a href="docs/translations/README.hi.md">हिन्दी</a> · <a href="docs/translations/README.es.md">Español</a> · <a href="docs/translations/README.fr.md">Français</a> · <a href="docs/translations/README.ar.md">العربية</a> · <a href="docs/translations/README.bn.md">বাংলা</a> · <a href="docs/translations/README.ru.md">Русский</a></p>

## Features

- Replace any of the seven radio stations with your queue. Innovative Leisure is selected by default.
- Search YouTube by song or artist, or add video links. Choose tracks, reorder entries, repeat a track or the queue and seek within a song.
- Preview and import public YouTube playlists (up to 500 unique tracks), or choose the initial Most Wanted 2005 / FH5 Bass Arena soundtrack playlists. Append or replace with confirmation.
- Save named queues and share them as JSON files. Append imported tracks or replace the current queue with confirmation.
- Optionally normalize volume before audio enters the native game mixer.
- Launch FH2 and enable your queue with **Open FH2 + Radio**.
- Check and install compatible official updates with a local backup; optional startup checks are off by default.
- Preview and export a diagnostic report without account details, local paths or queue links.
- Save favorites and a bounded local listening history; add recent tracks back to your queue.
- Exclude tracks or artist channels from recommendations and undo exclusions in Preferences.
- Prepare the next audio source in the background; this is not an offline download or guaranteed gapless playback.
- Configure optional Ctrl+Alt shortcuts for next, radio toggle and favorites; commands act only while FH2 is focused.
- Continue with related recommendations after your manual queue ends, without signing into Google.
- Play through the game's mixer, including the Festival speaker effects, with track and artist information on the HUD.
- Pause with the game, when leaving its window or when switching away from your replacement station.
- Apply a custom station name and the Horizon Radio logo, with a backup and restoration option.
- Keep different radio, audio and window preferences as named configuration profiles. Loading a profile disables the radio and preserves your queue.
- Switch between full and compact panel layouts; the view is remembered across launches.
- English by default, eight optional interface translations and optional tray preferences.

Version-by-version changes are in [Releases](https://github.com/P1upp3t/Forza-Horizon-2-Radio/releases) and the [itch.io devlog](https://puppetzim.itch.io/fh2-horizon-radio/devlog).

## Install & update

Requires **Windows x64**, **Azimuth 0.9.10** and your own legitimate **FH2 1.0.0.64** installation. Python, Node, VLC and a separate browser player are not required. The app window uses Microsoft Edge WebView2. [Get Azimuth](https://almost-there-games.itch.io/azimuth).

1. [Download the latest release](https://github.com/P1upp3t/Forza-Horizon-2-Radio/releases/latest) and extract `horizon-radio` next to `azimuth.exe`.
2. Open `FH2 Radio.exe` and search for music or add YouTube video links, one per line.
3. Choose a replacement station in **Preferences**, enable the radio, then select that station in FH2.
4. To install the station name and logo, close FH2 and choose **Apply station identity**, then reopen the game.

In **Preferences → App updates**, check official releases, download an update and choose **Install & restart** with FH2 closed. The previous app files are backed up in `runtime/updates`; installation errors restore those files. When updating to 0.6.1, restart FH2 to load the updated audio adapter. Manual updating is also supported: choose **Quit app** before replacing the app files. Keep the entire `runtime/` folder: it stores your queue, preferences and original interface backup. The radio starts disabled; enabling it is your choice. The initial volume is 65%.

Minimizing the Windows window or using **Minimize panel** sends the app to the tray near the clock. Double-click its icon or choose **Open Horizon Radio** to return.

Enable **Close to tray** in **Preferences → Window & tray** to keep the app running near the clock when you click X. Double-click the icon to reopen it; **Quit app** exits completely. **Start in tray** is optional.

## Compatibility & privacy

The current release was tested with **Azimuth 0.9.9 / FH2 1.0.0.64**. Azimuth 0.9.10 compatibility was previously confirmed. Other builds are not confirmed compatible. Native audio integration is experimental.

- The radio adapter modifies game memory while active. Applying the station identity modifies the game's UI archive and manifest, preserving verified originals. Game saves are not modified.
- Switching off the app returns audio to the original station. The installed visual identity remains until you restore it with FH2 closed.
- YouTube requests are sent to YouTube. Recommendations use the current track, without your Google account or browsing history. Queue and preferences stay on your PC. Search queries are sent to YouTube without signing in. Optional update checks contact the official GitHub repository. Diagnostic reports are reviewed and exported locally; nothing is uploaded automatically.
- Public YouTube playlist snapshots are supported (PL IDs, up to 500 unique tracks). Private/account-only playlists, YouTube Mix IDs, live playlist synchronization and Spotify queues are not supported. Removed, restricted or unavailable videos may fail. Interrupted streams produce an error instead of advancing as though the song finished.

Version 0.6.1 prepares radio source channels earlier; no original-radio fragment was heard during the tested station transitions. Native audio integration remains experimental. Common unsupported HUD punctuation is normalized, but the game font still limits character support.

## Feedback & credits

[App page](https://puppetzim.itch.io/fh2-horizon-radio) · [Azimuth community topic](https://itch.io/t/7136486/fh2-horizon-radio-free-in-game-music-queue-for-azimuth)

See the [FAQ](docs/FAQ.md) for setup, audio and restoration help. When [reporting an issue](https://github.com/P1upp3t/Forza-Horizon-2-Radio/issues/new/choose), include your app, game and Azimuth versions, reproduction steps and what you expected. Review attachments before posting; do not upload saves or your whole runtime folder.

All features and downloads are free. [Optional support](https://ko-fi.com/puppetzim) helps fund maintenance and development. This repository hosts downloads, documentation and issue tracking; **source code remains private**.

[Usage terms](docs/LICENSE.txt) · [Third-party notices](docs/THIRD-PARTY-NOTICES.txt) · [Artwork](docs/ARTWORK.md).

An independent fan project by Puppet / P1upp3t, not affiliated with Microsoft, Xbox, Playground Games, Turn 10, Azimuth, YouTube or Spotify. No game, DLC, game files or license keys are included; donations do not grant a game license.
