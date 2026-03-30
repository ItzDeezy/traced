# traced.

**flash · vanish · recreate**

A shape memory game. A shape flashes on screen briefly — then it's gone. Draw it from memory. See how close you got.

![traced. screenshot](https://traced.gg)

## play

Open `index.html` in your browser. No install, no backend, no account.

Or play online at **[traced.gg](https://traced.gg)**

## how it works

1. **watch** — a shape flashes for 0.5–3 seconds depending on difficulty
2. **draw** — recreate it freehand from memory
3. **score** — accuracy is measured by comparing your drawing against the original using overlap scoring (filled area + outline match)

## modes

| mode | description |
|------|-------------|
| **free play** | unlimited games, pick your difficulty |
| **daily** | same 5 shapes for everyone worldwide, once per day |
| **multiplayer** | host a lobby, share a 6-letter code, play together in real time |

## multiplayer

Uses **PeerJS** (WebRTC) — no backend required. The host's browser acts as the server.

- host generates a 6-letter room code
- guests join with the code
- everyone gets the same shapes (seeded RNG)
- configurable: difficulty, rounds (3/5/10), draw timer, max players
- live leaderboard between rounds + final rankings

## settings

- **easy** — 3 second flash, simple 4-point shapes, centered
- **medium** — 1.5 second flash, 6-point irregular shapes, some position variance
- **hard** — 0.5 second flash, 8-point complex shapes, anywhere on canvas

## tech

Single HTML file. No framework, no build step, no dependencies except:
- [DM Mono](https://fonts.google.com/specimen/DM+Mono) — font (Google Fonts CDN)
- [PeerJS 1.4.7](https://peerjs.com) — WebRTC for multiplayer (Cloudflare CDN)

Everything else is vanilla JS + Canvas API.

## features

- dark / light mode (persists via localStorage)
- mute button
- per-round replay viewer — see original vs your drawing side by side
- persistent stats: best score, avg, streak, games played, sparkline
- daily streak counter
- "new best!" badge on personal records
- animated countdown ring
- keyboard shortcuts: `Space` to advance, `Escape` to exit, arrow keys in replay

## self-hosting

Just put `index.html` on any static host. GitHub Pages works perfectly:

1. create a repo, add `index.html`
2. Settings → Pages → deploy from main branch
3. done — multiplayer works across devices once hosted

## license

MIT — see [LICENSE](LICENSE)

## credits

Built by [(ItzDeezy)](https://github.com/itzdeezy)
