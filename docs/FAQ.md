# Frequently asked questions

## Which versions are supported?
Windows x64, Azimuth 0.9.10 (confirmed in game) and FH2 1.0.0.64. Azimuth 0.9.9 was also tested previously. Other builds are not confirmed.

## Why is there no sound?
Enable the radio in the app, return to FH2 and select the replacement station. Unpause the game and check both the app and game radio volumes. The default app volume is 65%. Other stations do not play your queue.

## What if a song fails or ends early?
Try selecting the track again. Video restrictions and availability can change. Version 0.4.1 checks later audio ranges before playback and does not treat interrupted streams as completed tracks. Report repeatable failures with the video link and app version.

## Does the audio use the game effects?
Yes. Audio is passed through the native game mixer. Festival speaker effects, pause/resume and station switching were confirmed in the tested installation.

## Can I use Spotify or a full YouTube playlist?
Public YouTube playlists are supported in 0.6.1. Open YouTube playlists & themed stations, paste a URL or PL ID, preview it and choose Append or Replace. Up to 500 unique tracks are imported in order. Previewing does not change your queue or start playback; Replace asks for confirmation and stops playback. Spotify is not supported yet.

## How do I change the station name and logo?
Choose the station and name in Preferences. Close FH2, apply the station identity and reopen the game. Changes to audio station selection apply immediately; visual changes require applying the identity with FH2 closed.

## How do I uninstall?
Close FH2 and use Restore original identity before deleting the app folder. Keep runtime/branding until restoration succeeds. Do not replace another mod's changed interface files blindly; the app stops if it detects incompatible file changes.

## Where are my data stored?
In runtime beside the executable. Keep this folder during updates. It contains your queue, preferences and original interface backups and is not included in the release download.

## Does it require an account or external player?
No Google login or external player is required. Audio libraries and the resolver are bundled; Microsoft Edge WebView2 provides the app window.

## How do I keep the app running when I close its window?
In Preferences → Window & tray, enable Close to tray. The X then hides the panel near the Windows clock. Double-click the icon to restore it, or use Open Horizon Radio in the tray menu. Quit app stops it completely. Version 0.4.2 fixes the tray initialization timing problem.

## How do I save or share queues?
Expand Saved queues & sharing on Overview. Save a named queue, export the current queue as JSON, or import a Horizon Radio queue file. Append is the default. Replace asks for confirmation and stops playback. A queue holds up to 500 tracks; up to 50 named queues can be saved. Exported files contain public video IDs and displayed titles/artists, with no preferences or stream URLs.

## Can I search inside the app?
Yes. Search YouTube by song or artist and add a result with +. No account is used. Search results can still be removed or restricted by YouTube.

## How do I reduce volume differences between songs?
Enable Normalize volume in Preferences. It is optional and off by default. The filter runs before PCM enters the game mixer, retaining the Festival effects.

## How do official updates work?
Check App updates in Preferences. Optional startup checks are off by default. A compatible official release is staged and verified before installation. Close FH2 and confirm Install & restart. The three previous app files are backed up in runtime/updates, with restoration on an installation error. The runtime folder is not replaced. You can still update manually.

## How do I export a diagnostic report?
Open Help and choose Preview report. Review it before exporting a TXT file. The report excludes accounts, local paths, song names, queue links and stream URLs. Nothing is sent automatically. Describe what happened before sharing it on Issues.

## Can I launch the game from the app?
Use Open FH2 + Radio on Overview. It starts Azimuth and enables the current queue. If needed, choose azimuth.exe in Preferences. An already running game is not launched again. Opening the app alone still leaves the radio disabled.

## Why does selecting azimuth.exe fail?
Update to 0.7.3 and open the FH2 Radio.exe desktop window. Select the existing azimuth.exe, not a shortcut. Earlier versions incorrectly required an FH2 subfolder beside the launcher; that requirement is removed for selecting and launching Azimuth. If saving fails, the new message identifies a settings write problem: use a writable app folder and try again. A normal browser panel cannot show the desktop file picker. Artwork checks remain separate and still need the supported game UI archive. If it still fails, report the exact new message and app version on issue #2, without posting private paths.

## How do configuration profiles work?
Open Preferences → Configuration profiles. Enter a name and save your current preferences as a new profile. You can keep up to 50 profiles and load, update, rename or delete them. Loading asks for confirmation and disables the radio. The current queue and game files stay unchanged. Profiles include station/name, language, volume, repeat, recommendations, normalization, window/tray preferences, startup update checks and compact mode. Changing station/name still requires applying station identity separately with FH2 closed. Keep runtime/profiles.json when updating.

## Can I use a compact panel?
Use Compact mode above the main panel. It reduces spacing and hides the large player artwork while keeping playback and queue controls available. Full mode restores the normal layout. The view is saved automatically and included in configuration profiles.

## What is new in 0.6.0?
Favorites (up to 500), local listening history (up to 200 entries after five seconds of playback), reversible recommendation exclusions, repeat-current-track mode, next-source preparation, installed station identity checks and optional keyboard shortcuts. History can be cleared with confirmation; favorites and exclusions stay local. Manual queue entries play even when excluded from recommendations. Artist matching uses the channel ID when available, otherwise the displayed name.

## How do the keyboard shortcuts work?
Open Preferences → Keyboard shortcuts. Use Ctrl+Alt with a letter, number or F1-F12. All shortcuts are disabled by default. Commands act only while FH2 is focused, but their configured combinations are reserved by Windows while the app runs. Clear a field to disable its shortcut. Conflicting combinations are rejected.

## Why do I briefly hear the original radio?
Version 0.6.1 prepares radio source channels before selection. No original-radio fragment was heard during the tested station transitions, including pause/resume. If you still hear one, report the station, app/Azimuth versions and whether it happens on initial enable or later station switching.

## Why do some HUD characters differ from the app?
The game font does not support every character. Common unsupported punctuation is normalized and long HUD names are shortened. Original metadata stays intact in the app; the game font itself is not replaced.

## Should I restart FH2 when updating to 0.6.0?
Yes. Close FH2 and choose Quit app, replace the three app files while keeping runtime, then reopen FH2. The updated audio adapter cannot replace an older adapter that is already loaded in the game. This is separate from applying station name/logo changes, which also requires closing and reopening FH2.

## What are themed stations?
Two initial community soundtrack playlists are offered: Need for Speed: Most Wanted (2005) and Forza Horizon 5 - Horizon Bass Arena. Preview and import one into your queue. They are public third-party playlists, not official stations or bundled audio; contents and availability can change. Imports are local snapshots. No private playlists, Mix IDs or automatic live synchronization. The preview shows the first 30 titles and the total import count. Some removed/restricted videos may not play, and later-page metadata may refresh during playback.

## Does minimizing go to the tray?
Yes, starting in 0.6.1. Windows minimize and Minimize panel send the app near the clock, with its tray icon available even when Close to tray is disabled. Double-click the icon or choose Open Horizon Radio to restore the window. Quit app exits completely; closing X still follows your tray preferences.


## Are song titles cleaned automatically?
Yes. Version 0.7.0 removes common upload annotations such as Official Video, Official Audio, Lyrics and bracketed quality labels. Live, Remix, Acoustic and similar version information is retained. Ambiguous title text is kept rather than aggressively removed. The original provider title is retained locally; the app and HUD use the cleaned display title. There is no manual title editor.

## What happens when I enter an event?
After established free roam, detecting a supported event advances once to the next queued song. At the end of a multi-track queue, it returns to the first entry. A single-song queue continues. Leaving the event does not change songs. Pauses, focus changes and uncertain reads are not treated as event entry; opening the app inside an event establishes a baseline without skipping. Restarting an event without returning to free roam is not currently a separate trigger. The new trigger has automated transition coverage; actual event timing is not yet manually confirmed for this release.

## Can I share a whole station?
Expand Share a station and export its JSON file. The file contains its name, replacement slot, standard Horizon Radio logo identity and video links with metadata; it contains no music, credentials or game files. Preview before importing, choose Append or Replace, and optionally use the imported name and slot. Import stops playback. Artwork is not installed by import: apply station identity separately with FH2 closed, then reopen the game. Arbitrary custom logo files are not part of station presets.

## Does the queue check guarantee a video will play?
No. It checks duplicate video IDs and public metadata, not the full playback stream. A public metadata result is not a playback guarantee; network, access and rate-limit errors are marked uncertain. Checks have a 60-second work budget, with up to five seconds for an in-flight request; remaining entries stay unchecked. Select entries yourself and confirm removal. Queue edits invalidate old results.

## Can I clear or undo my queue?
Clear queue asks for confirmation and stops playback. Saved queues, favorites, history and settings remain. Undo clear restores the previous queue without enabling playback while the queue remains empty; adding new tracks or closing the app ends that undo opportunity. Removing the current song through the health check also stops playback.

## My game folder is named Anthem instead of FH2. Does artwork work?
Starting in 0.7.4, station identity reads data/azimuth.ini beside the selected azimuth.exe and resolves the selected title's folder entry. Relative paths are based on the launcher folder; absolute paths work too. Checking, applying and restoring use that folder's Mount/media/UI.zip. If a check fails, its attempted path appears locally in the panel; review/redact it before sharing screenshots. Do not rename folders or change Azimuth's config just for the radio. If a config exists but is invalid, the app stops rather than guessing another game folder.


## Identity check shows the path to azimuth.ini. What should I do?
Update to 0.7.5. Azimuth on Windows can write this file as UTF-16 with a byte-order mark; 0.7.4 read only UTF-8. The corrected reader accepts UTF-16 LE/BE with BOM and UTF-8 with or without BOM. Do not convert or edit the configuration as a workaround. If a check still fails, review the attempted path shown in the app before sharing it.

## How can I identify a playback failure?
Starting in 0.7.5, the player displays its underlying backend error alongside the translated failure message. Share the error text after removing private paths, URLs or account details. Do not post the full API state or queue. Exposing an error does not itself fix its underlying audio or network cause.

## An update installed, but restarting shows Failed to load Python DLL. What now?
Dismiss the error and open FH2 Radio.exe manually. The older updater can pass its temporary extraction state to the new process after that folder has been removed. Version 0.7.6 corrects future updater restarts by starting an independent instance. Updating from an older version still uses that older updater for the first restart, so a manual reopen may be needed once. Preserve runtime; do not delete your queue or install Python to work around this restart failure.

## Every track fails with Could not obtain audio (FileNotFoundError). What should I do?
Update to 0.7.7. A certificate resource required by the bundled Python runtime was missing from the Windows package, causing the YouTube dependency to fail during import before stream resolution. The corrected package includes that resource and keeps HTTPS certificate and hostname verification enabled. You do not need to install Python or Node, rename the game folder or edit the game's configuration. If playback still fails, share the displayed error after redacting private paths and URLs.

## Does Horizon Radio work with Azimuth 1.0.3?
Yes. Horizon Radio 0.7.7 was tested in game on October 28, 2026, and music playback was confirmed working. Update older Radio versions to 0.7.7, preserving runtime. The earlier FileNotFoundError was a Radio packaging issue corrected in 0.7.7. This confirms the tested FH2 1.0.0.64 setup; it is not a compatibility promise for future Azimuth releases.


Compatibility update — October 30, 2026: Horizon Radio 0.7.7 has been tested in game with Azimuth 1.0.4 and confirmed working. Azimuth 1.0.3 was previously confirmed on October 28. No new Radio release is needed.
