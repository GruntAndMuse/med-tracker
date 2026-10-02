# Roadmap — Med Tracker

Where this is going, and what we're deliberately not doing.

## Now (v1.x — current)

The single-file web app: pill + label photos, daily checklist with AM/PM color coding, with-food/empty-stomach badges, pill count with refill warnings, snooze, double-dose guard, appointment tracker, history log, JSON backup. Works on any phone browser, installable to home screen.

## Next

- **Polished app-store UI pass** — custom icon, splash screen, onboarding flow, refined visual design. The current UI is functional; the store version should look like a real product.
- **Android APK via Capacitor** — sideloadable debug APK first (for testing), then a signed release build. Hosted on GitHub Releases.
- **Google Play submission** — $25 one-time developer fee. Health apps declaration, data safety form (truthfully: no data collected), privacy policy URL, "not a medical device" disclaimer.
- **"As needed" (PRN) meds section** — separate from scheduled doses; logged with timestamp when taken. For pain/nausea meds that aren't on a fixed schedule.
- **Doctor visit summary** — one-tap clean summary of medications + adherence history to show or print for appointments. Built from the existing history log.

## Later

- **Apple App Store submission** — $99/year developer account, stricter review. May invoke Guideline 5.1.1(ix) (healthcare field, individual developer) — rebuttal ready: the app provides no healthcare services, only personal reminders.
- **Optional audio/push reminders** — via Capacitor, only if they can be done without any server or data transmission. If reminders require a backend, they don't ship.

## Deliberately not doing

These are rejections, not backlog. They conflict with the privacy architecture or the "don't feel like homework" principle:

- **Cloud sync / accounts** — requires servers; violates "nothing leaves your phone"
- **Caregiver/family alerts** — requires a backend; same reason
- **Drug interaction checker** — liability + needs a drug database; ask your pharmacist
- **Symptom/mood/measurement tracking** — the "feels like homework" problem; users stop opening the app
- **Gamification, streaks, points** — wrong tone for chemo; a missed dose is not a moral failure
- **Pharma integrations, coupons, data partnerships** — the trust-killer we're positioned against

If any of these ever get built, the privacy and legal analysis (see SECURITY.md, PRIVACY.md) must be redone from scratch.
