---
layout: default
title: Troubleshooting
description: Common Lofi Vibes issues and fixes.
permalink: /troubleshooting/
---

## Troubleshooting

### `/station` opens but no music starts

- Join a voice channel before selecting a station.
- Confirm Lofi Vibes can View, Connect, and Speak in that voice channel.
- Try a different preset station in case the upstream stream is offline.
- If the bot is already connected, selecting a new station should switch playback without disconnecting.

### 24/7 does not recover playback

- Run `/24-7 mode:enable` in the server.
- Start or select a station after enabling 24/7 if no active session exists yet.
- Confirm the saved voice channel still exists and the bot can access it.
- Check logs for reconnect or resume failure reasons.

### Slash commands are missing

- Confirm the bot is installed in server integrations.
- Wait a few minutes after command registration changes.
- Re-invite with the configured bot invite link if the app command scope is missing.

### `/submit-station` says submissions are not configured

Set `STATION_REVIEW_CHANNEL_ID` to a private review channel in the configured support server.

### Station upload is ignored

- Upload the file in `STATION_UPDATE_CHANNEL_ID`.
- Use the exact attachment name `preset-stations.json`.
- Confirm the uploader is a configured bot owner/developer or has a configured owner/developer role.
- Confirm the upload channel is inside `SUPPORTER_GUILD_ID` or `SUPPORT_GUILD_ID`.

## What To Send Support

- Server name and ID, if safe to share
- Command used
- Expected result
- Actual result
- Screenshot of channel/role permissions if relevant
- Any bot log line related to playback, station validation, or review-channel delivery

Support: [Support Server]({{ site.cta_support_url }})
