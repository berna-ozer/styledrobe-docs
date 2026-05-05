---
layout: default
title: Privacy Policy
permalink: /privacy/
---

# Privacy Policy

**Effective Date:** May 5, 2026
**Last Updated:** May 5, 2026

Styledrobe ("we", "our", "the app") is built with privacy as a foundational principle. This policy explains what data exists, where it lives, and what we — the developers — can and cannot see.

## TL;DR

- We do **not** run servers that store your personal data.
- We do **not** collect analytics, identifiers, or behavioral data for advertising.
- We do **not** use third-party trackers, ad networks, or marketing SDKs.
- Your wardrobe items, photos, preferences, calendar, wishlist, capsules and AI feedback stay on **your iPhone** and (if you opt in to iCloud) sync through **your own private iCloud account** — encrypted by Apple, inaccessible to us.
- Optional Community feed: only outfits you **explicitly tap "Share to Community"** are uploaded — anonymously, as a single composite image, to a public CloudKit database. Nothing else leaves your device.

If you delete the app and don't use iCloud, your data is gone forever — including our ability to recover it. There is no backup with us, because there is no "us" in the backup.

---

## What data the app handles

### Data stored locally on your device (and synced via your private iCloud)

The following items are stored in Apple Core Data on-device. If you have iCloud Sync enabled in Settings, they sync to **your private iCloud database** so they survive reinstalls and appear on your other Apple devices using the same Apple ID.

- **Wardrobe items**: photos (image binary stored in your private iCloud), type (e.g. "Shirts"), color, date added
- **Saved outfits**: combinations of items, weather context, occasion, date
- **Wear log / Calendar**: which outfits you marked as worn, on which days
- **Wishlist items**: photo, brand, type, color, price, URL, notes
- **Saved Capsules**: capsule name, included item references, generated combinations metadata
- **Style feedback**: which outfit pairings or colors you liked or disliked (used to personalize suggestions)
- **AI corrections**: when you correct an automatic tag (e.g. "this is Blouse, not Shirts")
- **Donate suggestions state**: which items you dismissed from the donate-suggestion list
- **App preferences**: language, appearance mode, haptics toggle, notification toggles
- **Subscription status**: managed by Apple StoreKit; we never see your payment info
- **Color Analysis result** (if you ran it): your detected season palette and recommendation set — derived locally from a selfie that is **never stored or transmitted**

The developer (Berna Ozer) has no technical means to access any of the above.

### iCloud private database

If you are signed into iCloud and iCloud Sync is enabled, the items above sync to **your private CloudKit database** (`iCloud.com.bernaozer.MyWardrobe`).

- The data is end-to-end encrypted by Apple ([Apple Platform Security documentation](https://support.apple.com/guide/security/welcome/web)).
- We have no access to your iCloud private database. Apple does not provide developers with this access.
- You can delete this data anytime via Settings → Apple ID → iCloud → Manage Storage → Styledrobe.

### Optional Community sharing (CloudKit public database)

Styledrobe includes an optional Community feed where users can share outfit ideas. **Nothing is shared automatically.** A post only appears in the community when you:
1. Generate or open an outfit
2. Tap **"Share to Community"** (a clearly labeled button)
3. Confirm in the share sheet (which lists what will be shared)

When you confirm, **only the following are uploaded** to a public CloudKit database (`iCloud.com.bernaozer.MyWardrobe`, public scope):

- A single **composite outfit image** (rendered card with your clothing photos placed together; not your raw clothing photos)
- Item types in the outfit (e.g. `["Tshirts", "Jeans"]`)
- Item colors (e.g. `["White", "Blue"]`)
- Occasion tag (if set, e.g. "casual")
- Weather context (if set, e.g. "warm")
- Compatibility score
- Your CloudKit user record ID (used so you can later delete or moderate your own posts)

What is **NOT** shared:
- ❌ Your name, email, Apple ID, profile, or display name
- ❌ Your raw individual clothing photos
- ❌ Your wardrobe inventory, calendar, wishlist, capsules, or feedback history
- ❌ Any item metadata beyond type/color
- ❌ Any device identifier or location

You can delete any of your own community posts at any time via the **"..." menu** on the post.

### Community moderation

To comply with App Store guidelines for user-generated content (UGC), Styledrobe includes:

- **Reporting**: Any user can report a post (Inappropriate, Spam, Nudity, Harassment, Copyright, Other). Reports are stored as `OutfitReport` records in the public CloudKit database.
- **Auto-hide**: Posts that receive a configurable threshold of reports are automatically hidden from all users' feeds.
- **Per-user mute**: Reporting a post locally hides it for you immediately, even before any community moderation occurs.

Reports include only the report reason, the reported post ID, and your CloudKit user record ID (for spam-protection — the same user cannot report the same post twice). No personal data is included.

### Data sent to Apple

- **WeatherKit**: To show weather-based outfit suggestions, the app sends your approximate location to Apple's WeatherKit service. Apple's policy applies. We never see this data.
- **Push Notification token**: If you enable notifications, Apple generates a device token for local notifications (morning reminder, unworn reminder, rain alert). All notifications are scheduled and delivered locally; we do not run a notification server.

### Data sent to third parties

The app makes outbound network requests **only** to:

- **Apple WeatherKit** (above)
- **Apple App Store / StoreKit** (subscription verification)
- **Apple CloudKit** (your private DB sync; community public DB if you share)
- **Open-Meteo** (`api.open-meteo.com`, free public weather API used as a fallback when WeatherKit is unavailable). Only your approximate latitude/longitude is sent — no identifier, no account.
- **Unsplash** (`api.unsplash.com`, image search for the "Style Feed → Inspiration" tab — only search keywords, no personal data)

We do not send your data to any analytics, advertising, marketing, or tracking service.

---

## What we do NOT do

- ❌ No third-party analytics SDK (no Firebase Analytics, Mixpanel, Amplitude, etc.)
- ❌ No advertising SDK (no AdMob, Meta Audience Network, etc.)
- ❌ No marketing email — there is no signup, no email collection
- ❌ No "anonymized data sharing" with partners
- ❌ No model training on user data — our AI models are trained once on public datasets and never updated with your data
- ❌ No social login (no Apple ID, Google, Facebook auth)
- ❌ No user accounts at all (Community uses your iCloud-managed CloudKit ID anonymously)

---

## On-device AI and your data

Styledrobe uses on-device CoreML models for:

- Auto-tagging clothing **type** (e.g. Shirts, Jeans) from a photo
- Detecting dominant **color** of an item
- Outfit **compatibility scoring** between items
- **Color Analysis** (optional, selfie-based palette detection)
- **Background removal** when adding items (Vision framework)

All of the above runs **entirely on your iPhone**. Photos used for these features (including any selfie used for Color Analysis) are processed in memory and **never transmitted** to us, Apple, or any third party.

The models were trained once on public fashion datasets (Mango Outfits, Polyvore, Fashion Product Images Dataset). They never receive your data for training purposes.

Personalization happens at inference time using your local feedback — the model itself is unchanged, but the scores you see are biased toward your taste based on your like/dislike history. This taste profile is local to your device.

---

## Children's privacy

Styledrobe is rated 4+ but is designed for adult/teen users. We do not knowingly collect data from anyone, regardless of age, because we do not collect data at all. The Community feed includes a reporting/moderation system to help keep content appropriate.

---

## Data retention and deletion

- **Local data**: Deleted immediately when you remove the app (if not synced to iCloud).
- **iCloud private data**: Remains in your private iCloud until you delete it via your iCloud settings, or via Settings → Reset All Data inside the app (which removes Wardrobe, Outfits, Wear Log, Wishlist, Capsules and propagates deletes to iCloud).
- **Community posts (public)**: You can delete any post you shared via the "..." menu on the post. Deleted posts are removed from CloudKit and from other users' feeds.
- **Subscription cancellation**: Apple manages this. We never see payment data.

---

## Your rights (GDPR / CCPA)

Because we do not collect personal data, most rights don't apply directly. But for completeness:

- **Right to access**: There is nothing on our end to access. Your data is in your iCloud account, accessible to you via Apple's standard tools.
- **Right to deletion**:
  - Delete the app + delete from iCloud (Settings → Apple ID → iCloud → Manage Storage)
  - Or use Settings → Reset All Data inside the app (wipes local + iCloud private DB)
  - For community posts: delete each via the "..." menu
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
