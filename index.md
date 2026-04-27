---
layout: default
title: Afterparty Groovy Music Docs
description: Official setup guide, command reference, and troubleshooting help for Afterparty Groovy Music.
---

<section class="hero-card">
  <div class="section-kicker">Music Docs</div>
  <h2>What Afterparty Groovy Music Does</h2>
  <p>Afterparty Groovy Music brings smooth Discord music playback to your server with fast song search, direct URL support, queue tools, audio tuning, and interactive playback controls built for everyday listening.</p>

  <div class="hero-grid">
    <div class="stat">
      <strong>Fast playback</strong>
      Search or paste a link and start listening with <code>/play</code>.
    </div>
    <div class="stat">
      <strong>Queue tools</strong>
      Move, remove, loop, shuffle, clear, and review tracks without breaking the flow.
    </div>
    <div class="stat">
      <strong>Audio control</strong>
      Adjust volume, seek through tracks, and apply filters or equalizer settings.
    </div>
  </div>

  <nav class="anchor-nav" aria-label="Sections">
    <a href="#quick-start">Quick Start</a>
    <a href="#commands">Commands</a>
    <a href="#playback">Playback</a>
    <a href="#queue">Queue</a>
    <a href="#audio-controls">Audio Controls</a>
    <a href="#troubleshooting">Troubleshooting</a>
    <a href="#support">Support</a>
  </nav>
</section>

<h2 id="quick-start">Quick Start</h2>

<div class="card-grid">
  <div class="doc-card">
    <div class="section-kicker">Step 1</div>
    <h3>Invite the bot</h3>
    <p>Add Afterparty Groovy Music to your server with the Invite button above, then make sure it can join and speak in your voice channel.</p>
  </div>
  <div class="doc-card">
    <div class="section-kicker">Step 2</div>
    <h3>Join a voice channel</h3>
    <p>Join the voice channel where you want playback to happen. Most playback commands require you to be connected first.</p>
  </div>
  <div class="doc-card">
    <div class="section-kicker">Step 3</div>
    <h3>Start music</h3>
    <p>Use <code>/play</code> with a song name or direct URL. You can also use <code>/search</code> if you want to browse results first.</p>
  </div>
</div>

```text
/play never gonna give you up
/play https://youtu.be/dQw4w9WgXcQ
/queue
```

<h2 id="commands">Commands</h2>

<div class="command-grid">
  <div class="command-card">
    <div class="section-kicker">Playback</div>
    <strong>/play, /search, /pause, /resume</strong>
    <p>Start tracks, search results, and control active playback.</p>
  </div>
  <div class="command-card">
    <div class="section-kicker">Queue</div>
    <strong>/queue, /move, /remove, /clear, /shuffle, /loop</strong>
    <p>Manage what plays next and reshape the queue on the fly.</p>
  </div>
  <div class="command-card">
    <div class="section-kicker">Audio</div>
    <strong>/volume, /seek, /filters filter, /equalizers equalizer, /audio-output</strong>
    <p>Fine-tune playback level, position, and sound profile.</p>
  </div>
  <div class="command-card">
    <div class="section-kicker">Utility</div>
    <strong>/nowplaying, /join, /disconnect, /help, /support</strong>
    <p>See the current track, connect the bot, and get help quickly.</p>
  </div>
</div>

<h2 id="playback">Playback</h2>

- <code>/play</code> adds a track, playlist, or direct URL to the queue.
- <code>/search</code> is useful when you want to pick from results instead of queueing the first match.
- <code>/pause</code> and <code>/resume</code> control the current song without clearing the queue.
- <code>/skip</code>, <code>/previous</code>, and <code>/replay</code> help move around active playback quickly.
- <code>/stop</code> ends playback and clears the current session when you are finished.

<h2 id="queue">Queue</h2>

- <code>/queue</code> shows the active queue and what is coming next.
- <code>/move</code> reorders songs so you can bring something forward or push it back.
- <code>/remove</code> deletes a specific queued item.
- <code>/shuffle</code> randomizes the queue.
- <code>/loop</code> can repeat a song or keep the queue cycling depending on your selected mode.
- <code>/clear</code> wipes the queue if you want a fresh start.

<h2 id="audio-controls">Audio Controls</h2>

- <code>/volume</code> changes playback loudness.
- <code>/seek</code> jumps to a point in the current track.
- <code>/filters filter</code> applies playback effects.
- <code>/equalizers equalizer</code> adjusts the sound profile for different listening styles.
- <code>/audio-output</code> exposes playback output controls when supported.
- <code>/autoplay</code> and <code>/247</code> help keep music going for longer sessions.

<h2 id="troubleshooting">Troubleshooting</h2>

<div class="card-grid">
  <div class="tip-card">
    <h3>The bot is not joining</h3>
    <p>Check that the bot has permission to view, connect, and speak in the target voice channel. Also make sure you are in a voice channel before running playback commands.</p>
  </div>
  <div class="tip-card">
    <h3>No sound is playing</h3>
    <p>Try <code>/skip</code> or <code>/stop</code> followed by <code>/play</code>. If the issue persists, confirm your Lavalink node and hosting environment are online.</p>
  </div>
  <div class="tip-card">
    <h3>A search is not returning results</h3>
    <p>Use a direct URL if available, or try a more specific search phrase with artist and track name together.</p>
  </div>
  <div class="tip-card">
    <h3>Premium sources are unavailable</h3>
    <p>Spotify and Apple Music playback may require premium access depending on your deployment and entitlement setup.</p>
  </div>
</div>

<h2 id="support">Support</h2>

If you need help with setup or playback issues, use the Support button above to join the Afterparty support server. You can also browse the source on [GitHub](https://github.com/afteryparty/afterparty-groovy-music) or visit [Afterparty Bot Labs](https://afterpartylabs.xyz) for the wider bot lineup.
