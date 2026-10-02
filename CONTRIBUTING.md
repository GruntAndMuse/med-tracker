# Contributing — Med Tracker

## The one rule

The entire app is **one HTML file** (`index.html`). Keep it that way.

No build step. No dependencies. No framework. No package manager. Anyone can open the file, read it, and understand what it does. That's a feature, not a limitation — it's what makes the privacy claim verifiable by a stranger in five minutes.

## Ground rules

1. **Keep it simple.** The user is an older adult on chemo who "sucks at tech." Big buttons, plain words, no jargon. If a feature needs a tutorial, it's too complicated.
2. **Keep it offline.** No network calls, no CDNs, no web fonts, no analytics. If your change adds anything that touches the network, it doesn't ship. (See SECURITY.md for how this is verified.)
3. **Keep it accessible.** Large touch targets (minimum ~64px), high contrast, no tiny text. Every new screen should be usable by someone with chemo-brain fog and shaky hands.
4. **No medical claims.** Never add anything that diagnoses, recommends doses, or suggests treatments. Reminder and tracking only. The disclaimer stays.
5. **One variable per change.** Change one thing, test it, then move on.

## How to contribute

1. Fork the repo.
2. Edit `index.html` directly.
3. Test on a real phone browser (or at minimum, Chrome DevTools mobile emulation). Tap through every screen you touched.
4. Open a PR describing what changed and why, in plain language.

## What we need most

- Real-world testing with actual medication routines (does the schedule logic hold up?)
- Accessibility feedback from older / low-vision users
- Translations (Spanish first)
- The Capacitor Android wrapper (see ROADMAP.md)

## License

All contributions under the MIT license, same as the project.
