---
layout: default
title: Privacy Policy
permalink: /privacy/
---

# Privacy Policy

**Effective Date:** April 24, 2026
**Last Updated:** April 24, 2026

Styledrobe ("we", "our", "the app") is built with privacy as a foundational principle. This policy explains what data exists, where it lives, and what we — the developers — can and cannot see.

## TL;DR

- We do **not** run servers that store your personal data.
- We do **not** collect analytics, identifiers, or behavioral data.
- We do **not** use third-party trackers, ad networks, or marketing SDKs.
- Your wardrobe items, photos, preferences, and AI feedback stay on **your iPhone** and (if you opt in to iCloud) sync through **your own iCloud account** — encrypted by Apple, inaccessible to us.

If you delete the app and don't use iCloud, your data is gone forever — including our ability to recover it. There is no backup with us, because there is no "us" in the backup.

---

## What data the app handles

### Data stored locally on your device

- **Wardrobe items**: photos, type (e.g. "Shirts"), color, date added
- **Saved outfits**: combinations of items, weather context, date
- **Style feedback**: which outfit pairings you liked or disliked
- **AI corrections**: when you correct an automatic tag (e.g. "this is Blouse, not Shirts")
- **App preferences**: language, appearance mode, notification settings
- **Subscription status**: managed by Apple StoreKit, we never see your payment info

This data is stored in Apple Core Data on-device. The developer (Berna Ozer) has no technical means to access it.

### Data synced via your iCloud (optional)

If you are signed into iCloud on your device, the items above sync to **your private iCloud database** so they survive app reinstalls and appear on your other Apple devices using the same Apple ID.

- The data is end-to-end encrypted by Apple ([Apple Platform Security documentation](https://support.apple.com/guide/security/welcome/web)).
- We have no access to your iCloud private database. Apple does not provide developers with this access.
- Even if we wanted to, we cannot retrieve, analyze, share, or sell your data. There is no API for it.
- You can delete this data anytime via Settings → Apple ID → iCloud → Manage Storage → Styledrobe.

### Data sent to Apple

- **WeatherKit**: To show weather-based outfit suggestions, the app sends your approximate location to Apple's WeatherKit service. Apple's policy applies. We never see this data.
- **Push Notification token**: If you enable notifications, Apple generates a device token. We do not currently use a notification server.

### Data sent to third parties

**None.** The app does not communicate with any servers controlled by us or any third party for the purpose of data collection.

The only outbound network requests are:
- Apple WeatherKit (above)
- Unsplash image search (for the "Style Feed" inspiration screen — only image queries, no personal data)
- Apple App Store (for subscription verification)

---

## What we do NOT do

- ❌ No analytics SDK (no Firebase Analytics, Mixpanel, Amplitude, etc.)
- ❌ No advertising SDK (no AdMob, Meta Audience Network, etc.)
- ❌ No marketing email — there is no signup, no email collection
- ❌ No "anonymized data sharing" with partners
- ❌ No model training on user data — our AI models are trained once on public datasets and never updated with your data
- ❌ No social login (no Apple ID, Google, Facebook auth)
- ❌ No user accounts at all

---

## AI and your data

Styledrobe uses on-device CoreML models for:
- Auto-tagging clothing type and color
- Outfit compatibility scoring

These models were trained on public fashion datasets (Mango Outfits, Polyvore, Fashion Product Images Dataset). They never receive your data for training purposes.

Personalization happens at inference time using your local feedback — the model itself is unchanged, but the scores you see are biased toward your taste based on your like/dislike history. This taste profile is local to your device.

---

## Children's privacy

Styledrobe is rated 4+ but is designed for adult/teen users. We do not knowingly collect data from anyone, regardless of age, because we do not collect data at all.

---

## Data retention and deletion

- **App uninstall + no iCloud**: All data deleted immediately when you remove the app.
- **App uninstall + iCloud sync enabled**: Data remains in your private iCloud until you delete it via your iCloud settings.
- **Subscription cancellation**: Apple manages this. We never see payment data.

---

## Your rights (GDPR / CCPA)

Because we do not collect personal data, most rights don't apply directly. But for completeness:

- **Right to access**: There is nothing on our end to access.
- **Right to deletion**: Delete the app + delete from iCloud (Settings → Apple ID → iCloud).
- **Right to portability**: Use Apple's standard data export from iCloud.
- **Right to object**: There is nothing to object to.

We cannot fulfill data subject requests for data we don't have.

---

## Changes to this policy

If this policy changes substantively, the updated version will be at this URL. The "Last Updated" date will reflect the change. Material changes will be highlighted in app release notes.

---

## Contact

For questions about this policy:
**[support@styledrobe.app](mailto:support@styledrobe.app)**

For privacy concerns related to Apple iCloud, refer to [Apple Privacy](https://www.apple.com/privacy/).
