# Security — Med Tracker

## Architecture: there is nothing to attack

Med Tracker is a single self-contained HTML file. It has:

- **Zero network calls.** No `fetch`, no `XMLHttpRequest`, no beacons, no CDN links, no web fonts, no third-party scripts. The only URL in the file is a user-clicked link to this repo.
- **Zero telemetry.** No analytics, no crash reporters, no ad SDKs.
- **Zero accounts.** No login, no password, no session — nothing to steal.
- **Local-only storage.** All data (medications, photos as compressed JPEG data-URLs, dose log, appointments) lives in the phone browser's `localStorage`. Nothing is transmitted anywhere, because there is nowhere to transmit it to.

## How to verify

This is the part that matters. Don't take our word for it:

1. **Read the file.** It's one HTML file, ~32KB. Search for `fetch(`, `XMLHttpRequest`, `sendBeacon`, `http` — you'll find only the repo link.
2. **Disconnect from the internet and use it.** Every feature works: adding meds, taking photos, checking off doses, appointments, history, backup. If it phones home, it can't — there's no home.
3. **Watch the network tab.** Open DevTools → Network, use the app, confirm zero requests.

## Threat model

| Threat | Status |
|---|---|
| Server breach exposing health data | **Impossible** — there is no server |
| Third-party SDK leaking data | **Impossible** — there are no third-party SDKs |
| Account takeover | **Impossible** — there are no accounts |
| Data sold to advertisers | **Impossible** — data never leaves the device |
| Device theft / loss | **User's responsibility** — mitigated by the JSON backup export (More → Save Backup). Keep the backup somewhere safe. |
| Browser data cleared | **Possible** — clearing site data wipes localStorage. Mitigated by the JSON backup export. |
| Malicious modified copy | **Possible** — only use copies from this repo or the official app stores. The single-file design makes tampering visible to anyone who reads it. |

## What would change this

Adding cloud sync, caregiver sharing, analytics, crash reporting, push-notification services, or any third-party SDK would invalidate this entire document. Per the roadmap's "deliberately not doing" list, those features are rejected. If that ever changes, this file gets rewritten from scratch first.

## Reporting issues

Open a GitHub issue. If you find a network call we missed, that's a critical bug — report it immediately.
