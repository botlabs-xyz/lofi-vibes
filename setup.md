---
layout: default
title: Setup
description: First-time setup for Lofi Vibes in Discord.
permalink: /setup/
---

## First-Time Setup

### 1. Invite Lofi Vibes

Use the official invite link:

[Invite Lofi Vibes]({{ site.cta_invite_url }})

### 2. Confirm Discord Permissions

Open **Server Settings -> Roles -> Lofi Vibes** and confirm the bot has the permissions needed for text and voice channels.

Recommended permissions:

- View Channels
- Send Messages
- Embed Links
- Read Message History
- Use Slash Commands
- Connect
- Speak

If a specific voice channel has permission overrides, check that Lofi Vibes can view, connect, and speak there too.

### 3. Join A Voice Channel

Join the voice channel where you want Lofi Vibes to play.

### 4. Run `/station`

Run `/station`, choose a preset station from the dropdown, and Lofi Vibes will start playing in your voice channel.

Selecting a different station from the dropdown should switch playback without needing to disconnect the bot.

### 5. Enable `/24-7` If Wanted

Run `/24-7 mode:enable` if you want Lofi Vibes to stay connected and recover the active or saved station when possible.

Run `/24-7 mode:disable` if you no longer want continuous recovery for the server.

### 6. Optional `/server-profile` Setup

Server owners and members with Manage Server can use `/server-profile` to configure server-level defaults.

Useful options:

- `/server-profile color` sets or clears the server accent color.
- `/server-profile default-station` sets or clears the default preset station.
- `/server-profile volume` sets the default volume.
- `/server-profile dj-role` sets or clears the DJ role.
- `/server-profile show` shows the current server settings.
- `/server-profile reset` resets the server settings.

These settings affect this server only. They do not change the global bot profile.

### 7. Submit Station Requests

Use `/submit-station` if you want to suggest a station for review.

Station suggestions are reviewed by the Lofi Vibes team before they are accepted.
