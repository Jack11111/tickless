# Tickless

**No clock. Just instinct.**

Tickless is a browser timing game built around one simple challenge: memorize a target time, watch the stopwatch for the first three seconds, then continue blind and stop it as close to the target as possible.

## Current build

This repository contains the v1 release candidate as a single dependency-light `index.html`.

Included modes and systems:

- Calibration
- Daily Five
- Blind
- Sudden Death
- Rush
- Double Tap
- Friend Challenge
- Progressive targets and Final Lock
- Lives, combos, scoring, achievements, XP, and cosmetics
- Time DNA player profiling
- Shareable challenge links
- Mobile, mouse, and keyboard controls
- CatalystPlay leaderboard integration hooks

## Run locally

Serve the repository with any static web server. For example:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

Opening the raw HTML file inside some app file-previewers may block JavaScript. Test it through a normal browser or static web host.

## Catalyst Play integration

Primary platform analytics use the single game identity `tickless`. Ranked modes use separate score board IDs so incompatible scoring systems never share a leaderboard:

- `tickless-calibration`
- `tickless-daily`
- `tickless-sudden`
- `tickless-rush`

Tracked first-party events include game load/open/start, mode selection, round completion, run completion, leaderboard opens, achievements, sharing, challenges, onboarding, and session end. Source / UTM attribution and the shared Catalyst Play player ID come from the Catalyst Game SDK.

`preview.html` is the lightweight animated card used by the Catalyst Play homepage.

## Hosting

The game is fully static and can be hosted with GitHub Pages or another static host.

CatalystPlay leaderboard IDs are reserved in the build as:

- `tickless-calibration`
- `tickless-daily`
- `tickless-sudden`
- `tickless-rush`

Until Catalyst Play is connected, leaderboard data is clearly labeled as a local preview. The intended production hostname is `https://tickless.catalystplay.net/`.

## Status

Release candidate for public playtesting. Final production sign-off should follow hosted mobile/browser QA and live CatalystPlay leaderboard validation.
