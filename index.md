---
layout: default
title: Lofi Vibes
description: Free-first live radio for Discord study rooms, chill hangouts, and background listening.
---

## Live Radio For Discord

Lofi Vibes is a free-first Discord radio bot built around live stations, cozy server listening, and low-friction voice channel controls. Pick a station, settle into a voice channel, and let the music keep the room moving.

<div class="doc-grid">
  <div class="doc-card">
    <h3>Start Listening</h3>
    <p>Use <code>/station</code> to browse preset radio stations and switch streams instantly.</p>
    <p><a href="{{ '/commands/' | relative_url }}">View Commands</a></p>
  </div>
  <div class="doc-card">
    <h3>Keep It Running</h3>
    <p>Use <code>/24-7</code> when a server wants Lofi Vibes to stay connected and recover playback when possible.</p>
    <p><a href="{{ '/troubleshooting/' | relative_url }}">Playback Help</a></p>
  </div>
  <div class="doc-card">
    <h3>Server Style</h3>
    <p>Use <code>/server-profile</code> to set server-level accent color, default station, volume, and 24/7 defaults.</p>
    <p><a href="{{ '/setup/' | relative_url }}">Setup Guide</a></p>
  </div>
</div>

## Free-First Model

All normal radio and music features are free. Optional supporter membership is community recognition only and helps cover hosting, uptime, development, and community support.

Supporter membership does not lock normal playback, station switching, profiles, server settings, or 24/7 behavior.

## Core Features

- Live preset station menu with `/station`
- Continuous playback recovery with `/24-7`
- Modern user profile cards with listening stats and trusted badges
- Server-level customization with `/server-profile`
- Public station request flow with `/submit-station`
- Developer station reload, validation, and upload workflows
- Optional supporter recognition without feature gates

## Project Links

<div class="cta">
  <a class="btn primary" href="{{ site.cta_invite_url }}" target="_blank" rel="noopener noreferrer">Invite Lofi Vibes</a>
  {% if site.topgg_url %}
    <a class="btn secondary" href="{{ site.topgg_url }}" target="_blank" rel="noopener noreferrer">Vote on Top.gg</a>
  {% endif %}
  <a class="btn secondary" href="{{ site.cta_support_url }}" target="_blank" rel="noopener noreferrer">Support Server</a>
  {% if site.cta_store_url %}
    <a class="btn secondary" href="{{ site.cta_store_url }}" target="_blank" rel="noopener noreferrer">Supporter Store</a>
  {% endif %}
  <a class="btn secondary" href="{{ site.cta_website_url }}" target="_blank" rel="noopener noreferrer">Afterparty Bot Labs</a>
</div>
