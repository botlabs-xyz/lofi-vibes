---
layout: default
title: Commands
description: Lofi Vibes command reference.
permalink: /commands/
---

## Command Reference

Lofi Vibes is focused on live radio and station playback. Use `/help` in your server for the exact command list currently registered there.

### Radio And Playback

| Command | What it does |
| --- | --- |
| `/station` | Opens the preset station menu and switches to the selected station. |
| `/radio` | Plays a radio stream or station search result where supported. |
| `/play` | Starts playback from a supported query, URL, or saved flow. |
| `/search` | Searches for playable radio content. |
| `/popular` | Shows popular station options where available. |
| `/favorites` | Manages saved favorite stations. |
| `/pause` | Pauses the current playback session. |
| `/resume` | Resumes playback. |
| `/stop` | Stops playback and clears the active session. |
| `/nowplaying` | Shows the current station or stream. |
| `/queue` | Shows the current playback queue/session list where applicable. |
| `/volume` | Sets playback volume for the server. |
| `/sleep` | Sets a sleep timer for playback. |
| `/filters` | Applies supported audio filters. |
| `/hq` | Uses high-quality playback behavior where supported by the source. |

### Continuous Radio

| Command | What it does |
| --- | --- |
| `/24-7 mode:enable` | Keeps Lofi Vibes connected and attempts to recover the current or saved station. |
| `/24-7 mode:disable` | Stops automatic 24/7 recovery for the server. |

`/24-7` is the main continuous playback feature. Live stations already continue by nature, and 24/7 handles recovery when the bot needs to reconnect.

### Profiles And Server Settings

| Command | What it does |
| --- | --- |
| `/profile` | Shows a modern user profile card with level, XP, listening stats, favorite station, and trusted badges. |
| `/theme` | Updates user-facing color/theme choices where supported. |
| `/server-profile show` | Shows this server's Lofi Vibes settings. |
| `/server-profile color` | Sets or clears the server accent color. |
| `/server-profile default-station` | Sets or clears the server default preset station. |
| `/server-profile 24-7` | Sets the server 24/7 default. |
| `/server-profile volume` | Sets the server default volume. |
| `/server-profile dj-role` | Sets or clears the server DJ role. |
| `/server-profile reset` | Resets this server's Lofi Vibes settings. |

`/server-profile` requires the server owner, Manage Server permission, or bot owner/developer access.

### Station Requests

| Command | What it does |
| --- | --- |
| `/submit-station` | Sends a station request to the bot team review channel. |
| `/apply` | Legacy redirect that tells users to use `/submit-station`. |

Station requests are not sent directly to Radio Browser. They are reviewed first by the bot team.

### Utility And Support

| Command | What it does |
| --- | --- |
| `/help` | Shows bot help. |
| `/about` | Shows Lofi Vibes information. |
| `/info` | Shows bot/service information. |
| `/invite` | Shows the configured bot invite link. |
| `/support` | Shows the configured support server link. |
| `/language` | Shows language information. |
| `/setlanguage` | Changes language settings where permitted. |
| `/badge` | Lists, equips, or clears allowed custom profile badges. Reserved team/supporter badges are protected. |
### Developer And Staff

| Command | Access | What it does |
| --- | --- | --- |
| `/bot` | Bot owner/developer | Global Bot Appearance Manager. |
| `/stations reload` | Bot owner/developer in support server | Reloads preset stations from JSON without restarting. |
| `/stations validate` | Bot owner/developer in support server | Validates the preset station JSON. |
| `/stations list` | Bot owner/developer in support server | Shows the currently loaded preset stations. |
| `/radiostatus` | Staff/developer | Shows radio service status where configured. |
| `/servers` | Staff/developer | Shows server information where configured. |
| `/set` | Staff/developer | Maintains bot settings where configured. |

See [Station Workflows]({{ '/station-workflows/' | relative_url }}) for the preset JSON, upload-channel, and review-channel flows.
