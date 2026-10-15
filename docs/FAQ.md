# Frequently asked questions

## Which versions are supported?
Windows x64, Azimuth 0.9.9 and FH2 1.0.0.64. Other builds are not confirmed.

## Why is there no sound?
Enable the radio in the app, return to FH2 and select the replacement station. Unpause the game and check both the app and game radio volumes. The default app volume is 65%. Other stations do not play your queue.

## What if a song fails or ends early?
Try selecting the track again. Video restrictions and availability can change. Version 0.4.1 checks later audio ranges before playback and does not treat interrupted streams as completed tracks. Report repeatable failures with the video link and app version.

## Does the audio use the game effects?
Yes. Audio is passed through the native game mixer. Festival speaker effects, pause/resume and station switching were confirmed in the tested installation.

## Can I use Spotify or a full YouTube playlist?
Not in this version. Add individual YouTube video links, one per line. Related recommendations can continue playback after your manual queue.

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
