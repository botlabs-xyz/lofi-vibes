---
layout: default
title: Station Workflows
description: Preset station, upload-channel, and station submission workflows for Lofi Vibes.
permalink: /station-workflows/
---

## Station Sources

Lofi Vibes uses `src/data/preset-stations.json` for the preset station menu shown by `/station`. The public station menu reads from that existing preset source; developers can validate and reload it without restarting the bot.

## Public Station Requests

Normal users can run `/submit-station` with:

- `name` required
- `url` required
- `country` optional
- `language` optional
- `tags` optional
- `homepage` optional
- `bitrate` optional
- `codec` optional

The bot validates basic fields, applies a per-user cooldown, stores a pending submission record, and posts a review embed to `STATION_REVIEW_CHANNEL_ID`.

Station requests are not sent to Radio Browser until a bot owner/developer approves them from the review channel.

## Review Channel

Set:

```env
STATION_REVIEW_CHANNEL_ID=PRIVATE_STATION_REVIEW_CHANNEL_ID_HERE
SUPPORT_GUILD_ID=SUPPORT_SERVER_ID_HERE
```

The review channel must be in the configured support server. Approve and Reject buttons are limited to configured bot owners/developers or their trusted roles.

## Preset Upload Channel

Set:

```env
STATION_UPDATE_CHANNEL_ID=PRIVATE_PRESET_UPLOAD_CHANNEL_ID_HERE
SUPPORT_GUILD_ID=SUPPORT_SERVER_ID_HERE
```

When a bot owner/developer uploads an attachment named `preset-stations.json` in that channel, Lofi Vibes:

- downloads the attachment
- parses and validates the JSON
- rejects invalid JSON without overwriting the current file
- backs up the current preset file to `src/data/backups/`
- writes the new preset file only after validation passes
- reloads the in-memory station cache
- replies with a success or error summary

## Developer Slash Commands

| Command | What it does |
| --- | --- |
| `/stations validate` | Loads and validates `src/data/preset-stations.json`. |
| `/stations reload` | Re-reads the preset JSON and replaces the in-memory station cache if valid. |
| `/stations list` | Shows the currently loaded preset stations with pagination. |

These commands are developer-only and only work in the configured support server.

## Developer Access Env

Use one or more of these:

```env
OWNER_ID=DISCORD_USER_ID_HERE
BOT_OWNER_IDS=DISCORD_USER_ID_HERE,SECOND_ID_HERE
BOT_DEVELOPER_IDS=DISCORD_USER_ID_HERE,SECOND_ID_HERE
BOT_OWNER_ROLE_ID=OWNER_ROLE_ID_HERE
BOT_DEVELOPER_ROLE_ID=DEVELOPER_ROLE_ID_HERE
```

## Preset JSON Notes

Keep station records complete and stable. Required validation checks include duplicate station names/IDs, missing fields, invalid URLs, and malformed JSON.

Use `/stations validate` before relying on a new monthly station refresh.
