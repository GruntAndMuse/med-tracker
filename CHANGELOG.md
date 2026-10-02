# Changelog — Med Tracker

All notable changes to this project. Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [1.0.0] — 2026-10-02

First public release.

### Added
- Medication list with **pill photo + bottle label photo** per med (user-taken; pills can look alike, the label tells them apart)
- **Daily checklist** — big tap-to-check dose cards, grouped under ☀️ Morning / 🌙 Evening headers with color coding so AM and PM doses can't be confused
- **With-food / empty-stomach / either** badges on every dose card
- **Pill count tracking** with low-stock refill warnings (⚠️ at 7 or fewer remaining)
- **Snooze** — "remind me in 30 min / 1 hour" per dose, for when nausea doesn't follow a schedule
- **Double-dose guard** — warns before letting you check off a med already taken in the last 2 hours
- **Tap-to-enlarge photo viewer** — compare the pill in your hand against the saved photo
- **Doctor appointment tracker** — upcoming and past visits with date, time, doctor, notes
- **History log** — every checked-off dose with timestamp, grouped by day
- **JSON backup** — export everything to a file, import it back
- **Privacy panel** — in-app plain-English statement of the privacy architecture
- Medical disclaimer (reminder helper only, not medical advice)

### Privacy architecture
- No login, no account, no ads, no analytics, no network calls
- All data in on-device localStorage; works fully offline after first load
- Single self-contained HTML file — the entire app is auditable by reading it
