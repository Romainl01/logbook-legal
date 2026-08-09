---
title: Privacy Policy — Logbook
---

# Privacy Policy

**Last updated: 9 August 2026**

## The short version

- **Your collection never leaves your phone.** Logbook stores your cards, your wishlist and their values on your device only. We have no copy of them.
- **The only thing we hold is your account:** your email address, and — if you use Sign in with Apple — the user identifier and the name Apple gives us.
- **No advertising, no tracking, no analytics, no data sold.** The app contains no third-party tracking or measurement SDK of any kind.

The rest of this page explains the details.

## 1. Who is responsible for your data

Logbook is published by **Romain Lagrange**, an individual, based in France.

- Email: **logbook.ugc@gmail.com**

Romain Lagrange is the data controller for the processing described here, within the meaning of the EU General Data Protection Regulation (GDPR).

This policy covers the iOS app **Logbook: OP TCG Card Scanner** (bundle identifier `com.romainl01.logbook`).

## 2. What we collect

### 2.1 Your account

To create an account, Logbook collects:

| Data | When | Notes |
|---|---|---|
| Email address | Sign-up with email, or Sign in with Apple | With Sign in with Apple, if you choose "Hide My Email", we only ever receive an Apple relay address ending in `@privaterelay.appleid.com`. We never see your real address. |
| Password | Sign-up with email only | Stored only as a cryptographic hash by our authentication provider. We cannot read it. |
| Apple user identifier | Sign in with Apple only | An opaque identifier issued by Apple, specific to Logbook. |
| Name | Sign in with Apple only | Apple offers your name on the first authorisation, and you can edit or decline it on Apple's own screen. If you provide it, we store it as your display name. Apple never gives it to us again, so if you decline it we simply have no name for you — nothing in the app requires one. |
| Apple refresh token | Sign in with Apple only | Stored so that we can revoke your Apple authorisation when you delete your account, as Apple requires. It is not used for anything else. |

That is the complete list. We do not ask for your date of birth, your phone number, your postal address or your payment details.

### 2.2 Card scans

When you scan a card, one of two things happens.

**Most of the time, nothing is sent anywhere.** Logbook reads the card code directly on your device using Apple's on-device text recognition. The photo never leaves your phone, and the scan works without an internet connection.

**If your device cannot read the card**, and only then, Logbook sends a resized copy of the photo (JPEG, longest side 1024 px) to our server function, which forwards it to a card-recognition provider and returns the list of candidate cards. Specifically:

- The photo is sent to our `identify` function hosted on **Supabase**, which does not store it — it holds the image in memory for the duration of the request and returns only card codes.
- The function forwards the image to **Ximilar** (the primary recognition provider) and, where configured, to **CardSight AI** as a second opinion.
- Ximilar's published terms state that prediction images are processed in memory and not stored. We have no independent way of verifying what each provider does with an image after we send it, and we do not claim otherwise — please refer to their own policies, linked in section 4.
- Our function's logs record error messages only. They never contain your photo.

The photo itself stays in your device's temporary storage, where iOS deletes it. Logbook does not save your scans to your photo library and does not ask for access to it.

### 2.3 What stays on your device, and never reaches us

The following is stored locally on your phone only, and we have no access to it:

- your collection (cards, quantities, condition, grade, purchase price if you enter one);
- your wishlist;
- the price data downloaded to value your collection.

**Please be aware of the consequence:** because we hold no copy, your collection is not backed up by us. If you lose your phone or reinstall the app, it is gone. Cloud backup of collections is planned but does not exist today.

### 2.4 Technical data

Like any app that connects to the internet, Logbook's requests carry technical connection data — your IP address, the time of the request, and basic device/network information. This applies when:

- your device fetches the daily price file from our public storage bucket;
- your device fetches card images from the third-party image CDN `static.dotgg.gg`;
- a scan falls back to the `identify` function.

We do not build profiles from this data and we do not link it to your account.

## 3. Why we process it, and on what legal basis

| Purpose | Data | Legal basis (GDPR Art. 6) |
|---|---|---|
| Creating and running your account, letting you sign in | Email, password hash, Apple identifier, name | Performance of a contract — Art. 6(1)(b) |
| Revoking your Apple authorisation when you delete your account | Apple refresh token | Performance of a contract — Art. 6(1)(b), and our legitimate interest in meeting Apple's platform requirements — Art. 6(1)(f) |
| Identifying a card you scanned, when your device cannot read it | Photo of the card | Performance of a contract — Art. 6(1)(b): you asked for the card to be identified |
| Keeping the service available and secure (technical logs, abuse prevention) | Technical connection data | Legitimate interest — Art. 6(1)(f) |

We do not process any special category data, and we do not use your data for automated decision-making with legal effects.

## 4. Who else is involved

We use a small number of service providers ("processors"). They act on our instructions and for no other purpose.

| Provider | Role | Where | Data involved |
|---|---|---|---|
| **Supabase, Inc.** (United States) | Hosts the accounts database and our server functions | Project hosted in the EU (Paris, France) | Account data; scan photos in transit only |
| **Ximilar, s.r.o.** (Czech Republic) | Card recognition, primary provider | European Union | Scan photos sent for recognition |
| **CardSight AI, Inc.** (Maine, United States) | Card recognition, optional second opinion | United States | Scan photos sent for recognition |
| **Apple Inc.** | Sign in with Apple, App Store distribution | United States | Your Apple sign-in |

**Transfers outside the European Union.** Ximilar is established in the EU, so no transfer takes place for the primary recognition path. Supabase, CardSight AI and Apple are established in the United States: sending a scan photo or storing account data with them can involve a transfer outside the EU, covered by the standard contractual clauses and safeguards published by each of those providers.

Card images displayed in the app are loaded from the third-party CDN `static.dotgg.gg`, which receives your IP address as part of any ordinary image request.

**We never sell, rent or trade your data, and we never share it for advertising purposes.** We only disclose data where the law requires it.

## 5. How long we keep it

| Data | Retention |
|---|---|
| Account data (email, password hash, Apple identifier, name) | For as long as your account exists. Deleted when you delete your account. |
| Apple refresh token | Same as above. Used once during deletion, to revoke the authorisation, then deleted. |
| Scan photos | Not retained by us. Held in memory for the duration of the request only. |
| Technical logs of our server functions | Short-lived, in line with Supabase's own log retention. They contain error messages and technical metadata, never your photos. |
| Your collection and wishlist | Kept on your device for as long as you keep them, or until you delete the app. |

## 6. Deleting your account

You can delete your account from inside the app, in **Settings → Account → Delete account**. No email, no form, no waiting period.

Deleting your account:

- permanently deletes your account and all associated data from our servers (email, password hash, Apple identifier, name, Apple refresh token);
- revokes Logbook's Sign in with Apple authorisation with Apple, where applicable;
- **wipes your collection, your wishlist and all locally cached data from the device you are signed in on.**

It takes effect immediately and cannot be undone. There is no "deactivated" state and no soft delete: your data is not archived somewhere in case you come back.

Note that because your collection only ever existed on your device, deleting the app also removes it, whether or not you delete your account first.

## 7. Your rights

Under the GDPR you have the right to:

- **access** the data we hold about you;
- **rectify** it if it is inaccurate;
- **erase** it (see section 6 — the in-app deletion does exactly this);
- **restrict** or **object to** processing based on our legitimate interests;
- **data portability** for the data you provided to us.

**How to exercise them:** email **logbook.ugc@gmail.com**. We answer within one month.

Two practical notes, so you know what to expect:

- Deleting your account from the app is faster than writing to us, and achieves the same result.
- Data portability concerns almost nothing here: the only data we hold is your email address and, where applicable, your name and Apple identifier — we will send them to you on request. Your collection is on your device and was never ours to export. An in-app export feature does not exist yet.

If you believe your data is being handled improperly, you may lodge a complaint with the French data protection authority, the **CNIL** ([cnil.fr](https://www.cnil.fr)), or with the supervisory authority of the EU country where you live.

## 8. What Logbook does not do

To be explicit, because a lot of apps in this category do the opposite:

- **No advertising.** Logbook shows no ads and contains no advertising SDK.
- **No tracking.** No analytics, no attribution, no measurement SDK, no third-party tracker, no advertising identifier. We do not track you across apps or websites, and we do not ask you to allow tracking, because there is nothing to allow.
- **No profiling.** We do not build a profile of you and we do not enrich your data from other sources.
- **No data sales.** We do not sell your data, and we will never make selling it part of the business model. If this ever changes, it will require your explicit prior consent — and a new version of this policy.
- **No access to your collection.** We could not sell it, share it or lose it even if we wanted to, because we do not have it.

## 9. Children

Logbook is not intended for children under 13, and we do not knowingly collect data from them. If you are below the age of digital consent in your country (15 in France), you need a parent or guardian to agree on your behalf. If you believe a child has created an account, contact us at **logbook.ugc@gmail.com** and we will delete it.

## 10. Changes to this policy

We may update this policy as the app evolves — in particular when cloud backup of collections is introduced, which will change what we store. The date at the top always reflects the most recent version. Significant changes will be announced in the app before they take effect.

## 11. Contact

Questions about this policy, or about your data: **logbook.ugc@gmail.com**.
