---
title: Privacy Policy — Logbook
---

# Privacy Policy

**Last updated: 11 August 2026**

## The short version

- **Photos of your cards never leave your phone.** Logbook reads the card code on the device itself, using Apple's on-device text recognition. No picture is ever uploaded, and a scan works with no internet connection at all.
- **Your collection is stored on your account**, on our servers, so that it survives a reinstall or a new phone. No other user of Logbook can read it.
- **Apart from your collection, the only thing we hold is your account:** your email address, and, if you use Sign in with Apple, the user identifier and the name Apple gives us.
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
| Name | Sign in with Apple only | Apple offers your name on the first authorisation, and you can edit or decline it on Apple's own screen. If you provide it, we store it as your display name. Apple never gives it to us again, so if you decline it we simply have no name for you, and nothing in the app requires one. |
| Apple refresh token | Sign in with Apple only | Stored so that we can revoke your Apple authorisation when you delete your account, as Apple requires. It is not used for anything else. |

That is the complete list. We do not ask for your date of birth, your phone number, your postal address or your payment details.

### 2.2 Card scans

When you scan a card, no photo is sent anywhere.

Logbook reads the card code directly on your device, using Apple's on-device text recognition, and matches it against the card catalogue that ships inside the app. The identification is entirely local: it makes no network request, and it works in airplane mode. If the code cannot be read, Logbook asks you to type it in. There is no path, and no fallback, that uploads the picture.

The photo itself stays in your device's temporary storage, where iOS deletes it. Logbook does not save your scans to your photo library and does not ask for access to it.

Adding the recognised card to your collection is a separate step, and that step does reach our servers, as section 2.3 explains. What travels is the card's identity and the details you chose to record. The photograph is not part of it.

### 2.3 Your collection

Once you are signed in, your collection is stored on your account, on our servers, and kept in step with a copy on your device so the app works offline. It covers:

- your cards: which printing, how many, the condition and the grade if you recorded them, and the purchase price if you entered one;
- your sealed products: which product, which language, how many, the purchase price if you entered one;
- your wishlist.

**Why we do this.** Your collection survives a reinstall, a lost phone or a new device: you sign in and it comes back. This is a change made in August 2026. Before it, the collection existed only on the device and nothing could recover it.

**What it means for your privacy.** We hold a copy. Your rows are locked to your account in the database itself, so no other user of Logbook can read them, and we use them for nothing other than giving them back to you. They are deleted when you delete your account (section 6).

The price data is a separate matter and says nothing about you: the app downloads the same public price file as everybody else and caches it on your device.

### 2.4 Technical data

Like any app that connects to the internet, Logbook's requests carry technical connection data: your IP address, the time of the request, and basic device and network information. This applies when:

- your device fetches the daily price file from our public storage bucket;
- your device fetches card images from the third-party image CDN `static.dotgg.gg`;
- your device signs you in, refreshes its session, or syncs your collection with our database;
- the app asks our payments provider whether your subscription is active (section 2.5).

The requests that carry your session are tied to your account by necessity: that is how the server knows whose collection to hand back. We do not build profiles from any of this, and we do not use it for anything beyond running and securing the service.

### 2.5 Subscriptions

Logbook is free up to a limited number of items in your collection, and paid above that. If you subscribe:

- **Apple takes the payment.** We never see your card number, your billing address or your Apple ID password. None of it passes through us, and we store no payment method.
- **We use RevenueCat to know whether your subscription is active.** The app sends it the App Store transaction receipt, the technical device and store information its SDK needs to match a purchase to a device, and, once you are signed in, your Logbook account identifier, so that a subscription bought on one device is recognised on the next. RevenueCat receives nothing else from us: not your email address, not your name, not your collection.

## 3. Why we process it, and on what legal basis

| Purpose | Data | Legal basis (GDPR Art. 6) |
|---|---|---|
| Creating and running your account, letting you sign in | Email, password hash, Apple identifier, name | Performance of a contract, Art. 6(1)(b) |
| Storing your collection so it survives a reinstall or a new phone, and keeping your devices in step | The collection data listed in section 2.3 | Performance of a contract, Art. 6(1)(b): this is the service |
| Revoking your Apple authorisation when you delete your account | Apple refresh token | Performance of a contract, Art. 6(1)(b), and our legitimate interest in meeting Apple's platform requirements, Art. 6(1)(f) |
| Selling a subscription, and recognising it on your other devices | Store transaction data, your account identifier | Performance of a contract, Art. 6(1)(b) |
| Keeping the service available and secure (technical logs, abuse prevention) | Technical connection data | Legitimate interest, Art. 6(1)(f) |

We do not process any special category data, and we do not use your data for automated decision-making with legal effects.

## 4. Who else is involved

We use a small number of service providers ("processors"). They act on our instructions and for no other purpose.

| Provider | Role | Where | Data involved |
|---|---|---|---|
| **Supabase, Inc.** (United States) | Hosts the accounts database, your collection, and our server functions | Project hosted in the EU (Paris, France) | Account data, collection data |
| **RevenueCat, Inc.** (United States) | Tells the app whether your subscription is active, and validates App Store receipts | United States | Store transaction data, your account identifier, device information |
| **Apple Inc.** | Sign in with Apple, App Store distribution, subscription payments | United States | Your Apple sign-in, your purchase |

No card-recognition provider appears in this table any more, and that is not an omission. Recognition used to run through two external providers when a device could not read a card; since August 2026 it runs only on your device, so there is nobody left to send an image to.

**Transfers outside the European Union.** All three companies above are established in the United States. Our Supabase project itself runs in the European Union (Paris), so your account and your collection are stored on EU servers, but Supabase's American parent company can access them for support and operations. Subscription data goes to RevenueCat in the United States. Those transfers are covered by the standard contractual clauses and safeguards published by each of those providers.

Card images displayed in the app are loaded from the third-party CDN `static.dotgg.gg`, which receives your IP address as part of any ordinary image request.

**We never sell, rent or trade your data, and we never share it for advertising purposes.** We only disclose data where the law requires it.

## 5. How long we keep it

| Data | Retention |
|---|---|
| Account data (email, password hash, Apple identifier, name) | For as long as your account exists. Deleted when you delete your account. |
| Apple refresh token | Same as above. Used once during deletion, to revoke the authorisation, then deleted. |
| Your collection, your sealed products, your wishlist | For as long as your account exists. Deleted when you delete your account. Removing a card removes it from your other devices too, and leaves behind only a marker saying it was removed, which is how your devices learn about the removal. That marker goes with the account. |
| Scan photos | Never retained anywhere, by us or by anyone else, because they never leave your phone. |
| Subscription data at RevenueCat | For as long as RevenueCat needs it to recognise your subscription and honour a restore, in line with its own retention policy. A purchase record necessarily outlives a cancellation, otherwise restoring a subscription could not work. |
| Technical logs of our server functions | Short-lived, in line with Supabase's own log retention. They contain error messages and technical metadata. |
| The local copy on your device | Until you delete the app, or until you delete your account, which wipes it. |

## 6. Deleting your account

You can delete your account from inside the app, in **Settings → Account → Delete account**. No email, no form, no waiting period.

Deleting your account:

- permanently deletes your account and everything attached to it from our servers: email, password hash, Apple identifier, name, Apple refresh token, and your collection, your sealed products and your wishlist;
- revokes Logbook's Sign in with Apple authorisation with Apple, where applicable;
- **wipes your collection, your sealed products, your wishlist and all locally cached data from the device you are signed in on.**

It takes effect immediately and cannot be undone. There is no "deactivated" state and no soft delete: your data is not archived somewhere in case you come back.

**Deleting the app is not the same thing.** It removes the local copy from that device, but your account and your collection stay on our servers until you delete the account itself, and signing in again on any device brings the collection back.

**Deleting your account does not cancel a paid subscription.** An App Store subscription is managed by Apple, not by us, and has to be cancelled in your Apple account settings. Do that first if you are subscribed.

## 7. Your rights

Under the GDPR you have the right to:

- **access** the data we hold about you;
- **rectify** it if it is inaccurate;
- **erase** it (see section 6: the in-app deletion does exactly this);
- **restrict** or **object to** processing based on our legitimate interests;
- **data portability** for the data you provided to us.

**How to exercise them:** email **logbook.ugc@gmail.com**. We answer within one month.

Two practical notes, so you know what to expect:

- Deleting your account from the app is faster than writing to us, and achieves the same result.
- Data portability covers your collection as well as your account details, since we hold a copy of both. There is no export button in the app yet: ask us and we will send you your collection as a file.

If you believe your data is being handled improperly, you may lodge a complaint with the French data protection authority, the **CNIL** ([cnil.fr](https://www.cnil.fr)), or with the supervisory authority of the EU country where you live.

## 8. What Logbook does not do

To be explicit, because a lot of apps in this category do the opposite:

- **No advertising.** Logbook shows no ads and contains no advertising SDK.
- **No tracking.** No analytics, no attribution, no measurement SDK, no third-party tracker, no advertising identifier. We do not track you across apps or websites, and we do not ask you to allow tracking, because there is nothing to allow.
- **No profiling.** We do not build a profile of you and we do not enrich your data from other sources.
- **No data sales.** We do not sell your data, and we will never make selling it part of the business model. If this ever changes, it will require your explicit prior consent, and a new version of this policy.
- **No other use of your collection.** We store it so that you cannot lose it, and for nothing else: it is not shared with other users (Logbook has no social or publishing features), not published as market data, and not sold. Holding a backup does mean we are technically able to read it, as is true of any service that stores anything on your behalf, and we do not look at it beyond keeping the service working.

## 9. Children

Logbook is not intended for children under 13, and we do not knowingly collect data from them. If you are below the age of digital consent in your country (15 in France), you need a parent or guardian to agree on your behalf. If you believe a child has created an account, contact us at **logbook.ugc@gmail.com** and we will delete it.

## 10. Changes to this policy

We may update this policy as the app evolves. The date at the top always reflects the most recent version, and significant changes will be announced in the app before they take effect.

The August 2026 version records two such changes. Card recognition became entirely on-device, so no photo is sent anywhere any more. And collections started being stored on your account rather than on the device alone, so we now hold a copy of something we previously did not.

## 11. Contact

Questions about this policy, or about your data: **logbook.ugc@gmail.com**.
