---
layout: default
title: Setup
description: First-time setup for Lofi Vibes in Discord.
permalink: /setup/
---

## First-Time Setup

### 1. Invite Lofi Vibes

Use the configured bot invite link from your deployment:

[Invite Lofi Vibes]({{ site.cta_invite_url }})

### 2. Confirm Discord Permissions

Open **Server Settings -> Roles -> Lofi Vibes** and confirm the bot can view channels, send messages, use embeds, connect to voice, and speak.

### 3. Join A Voice Channel

Join the voice channel where the station should play.

### 4. Pick A Station

Run `/station`, choose a preset station from the dropdown, and Lofi Vibes will start or switch playback in your voice channel.

### 5. Keep Playback Running

Run `/24-7 mode:enable` if this server should recover radio playback and reconnect where possible.

## Local Setup

```bash
npm install
npm.cmd ls --depth=0
node --check src/index.js
```

Do not commit `.env`. Keep tokens, database URLs, and Lavalink credentials local to the deployment environment.

## Environment Example

Use placeholders like these in your local `.env` or hosting provider. Replace every value that ends in `_HERE`.

```env
DISCORD_TOKEN=BOT_TOKEN_HERE
PREFIX=!
CUSTOM_STATUS=lofi vibes & chill

DB_BACKEND=mongo
MONGODB_URI=MONGODB_CONNECTION_STRING_HERE
MONGODB_DB=lofibot
PORT=3000
DEFAULT_TIMEZONE=America/New_York

THEME_COLOR=#5865f2
COLOR=#5865f2
LOG_CHANNEL_ID=LOG_CHANNEL_ID_HERE

BOT_INVITE_LINK=BOT_INVITE_LINK_HERE
SUPPORT_SERVER_INVITE=SUPPORT_SERVER_INVITE_HERE
TOPGG_VOTE_INVITE_LINK=TOPGG_VOTE_LINK_HERE
SUPPORTER_STORE_LINK=SUPPORTER_STORE_LINK_HERE

NODE_NAME=Lofi Vibes
NODE_URL=LAVALINK_HOST_AND_PORT_HERE
NODE_AUTH=LAVALINK_PASSWORD_HERE
NODE_SECURE=false

RADIO_BROWSER_API_URL=https://all.api.radio-browser.info
RADIO_BROWSER_TIMEOUT_MS=10000

SPOTIFY_ID=SPOTIFY_CLIENT_ID_HERE
SPOTIFY_SECRET=SPOTIFY_CLIENT_SECRET_HERE
```

### Link Env Compatibility

Lofi Vibes preserves older env names where possible:

- `TOKEN` or `DISCORD_TOKEN`
- `INVITE` or `BOT_INVITE_LINK`
- `SUPPORT` or `SUPPORT_SERVER_INVITE`
- `VOTE` or `TOPGG_VOTE_INVITE_LINK`
- `SUPPORTER_STORE_LINK`, `SUPPORTER_STORE`, or `STORE`
- `SPOTIFYID` or `SPOTIFY_ID`
- `SPOTIFYSECRET` or `SPOTIFY_SECRET`
- `MONGODB_URI` or `MONGO_URI`
- `COLOR` or `THEME_COLOR`

## Optional Supporter Recognition

Supporter membership is optional recognition only. Configure supporter recognition privately in your deployment environment if you want supporter-aware badges/status messages to appear.

## Manual Test Checklist

- `/station` opens the station dropdown and switches stations without disconnecting the bot.
- `/24-7 mode:enable` saves the setting and recovers playback where possible.
- `/profile` renders a readable profile card.
- `/server-profile show` displays server defaults for users with Manage Server.
- `/submit-station` confirms the station request was sent for team review.
