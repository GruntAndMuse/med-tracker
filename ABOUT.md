# About — Med Tracker

## What it is

Med Tracker is a free, offline medication tracker that runs as a single HTML file on your phone. Take photos of your pills and bottle labels, get a big-button daily checklist, track doctor appointments, and keep a history of everything you've taken.

## Who it's for

It was built for a chemo patient — a friend's mom — whose pills were hard to keep track of. Chemo regimens are confusing: similar-looking white tablets, strict with-food/empty-stomach rules, morning vs. evening doses that must not be mixed up, nausea that doesn't follow a schedule.

But it's for anyone who needs to track medications simply: older adults, caregivers setting it up for a parent, anyone who "sucks at tech" and just wants big buttons that work.

## Why it exists

The paid medication apps (Medisafe, MyTherapy, Dosecast) all do the same core job — reminders and tracking — and they all monetize the same way: ads, premium tiers, and selling de-identified adherence data to pharma companies. The features people actually pay for are cloud sync and caregiver alerts — the exact features that require servers, accounts, and your health data leaving your device.

We built the thing those apps charge for, gave it away free, and refused the parts that compromise privacy.

## Private by design — not "HIPAA compliant"

You'll notice we never say "HIPAA compliant." That's deliberate, and it's a stronger claim than it sounds.

HIPAA only applies to hospitals, insurers, and their vendors. A personal tracker where data never leaves your phone isn't covered by HIPAA — and claiming "HIPAA compliant" when HIPAA doesn't apply is itself a deceptive-practice risk under the FTC Act.

So we don't claim it. Instead, the architecture makes the question irrelevant:

- **No login, no account, no password** — nothing to breach
- **No ads, no analytics, no tracking SDKs** — nothing phoning home
- **No cloud, no server** — there is nowhere for your data to go
- **Works fully offline** — after the first open, it never needs the internet

"Private by design" isn't a compliance badge. It's the absence of everything that could violate your privacy in the first place.

## Built by GruntAndMuse

GruntAndMuse is Dennis Avery's FOSS project shop: free, open-source tools built in the open, documented honestly, with security and privacy baked in from the start — not bolted on later. The entire app is one readable HTML file. Review it yourself; that's the point.

## What it is not

A reminder helper only. It does not give medical advice, diagnose, treat, cure, or recommend any medication. Always follow your doctor's instructions.
