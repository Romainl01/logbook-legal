---
title: Privacy Policy — Logbook
---

# Privacy Policy

**Last updated: 11 November 2026**

## The short version

- **Your phone reads your cards first.** Logbook reads the card code on the device itself, using the text recognition built into your phone (Apple's on an iPhone, Google's ML Kit on Android), and a card read this way never leaves your phone. **Only when your phone cannot read a card** is its photo sent to a card-recognition service, CardSight AI, to identify it. We keep a copy of that photo for 90 days, in a private space under your account, to understand why your phone could not read it. Section 2.2.
- **Your collection is stored on your account**, on our servers, so that it survives a reinstall or a new phone. No other user of Logbook can read it, **unless you create a public profile to share it**.
- **If you share your collection**, you choose a nickname and a photo, and anyone holding your link sees that nickname, that photo, your cards and your wishlist, never what you paid for anything. A photo you add is checked by an automated moderation service (OpenAI) before it is published. You can make your account private or cancel the link at any time. Section 2.10.
- **If you subscribe and join the community**, what you post there (posts, replies, likes) is visible to the other subscribers, under your nickname and photo, next to the approximate value of your collection unless your account is private. Text is checked by an automated moderation service (OpenAI) before it is published, for inappropriate content, scams, advertising, mentions of other collection apps and posts in the wrong channel; a refused text is kept 30 days so that we can check the refusal, then deleted. You can report or block anyone. Section 2.11.
- **If you follow other collectors**, we record who you follow and since when. The people you follow see that you follow them, and if your account is public, the people who follow you see the cards and wishes you add, never what you paid. A private account shows none of it. Section 2.12.
- **Apart from your collection, the only thing we hold is your account:** your email address, and, if you use Sign in with Apple, the user identifier and the name Apple gives us, or, if you use Sign in with Google on Android, the account identifier and the name Google gives us.
- **On Android, Google is involved in four places**: Sign in with Google, the delivery of notifications (Firebase Cloud Messaging), payments (Google Play), and the on-device text recognition (ML Kit), which reads your cards on the phone and sends Google only technical usage metrics, never the picture or the text it read. Sections 2.1, 2.2, 2.5 and 2.9.
- **No advertising, no cross-app tracking, no data sold.** Logbook contains no advertising SDK and no advertising identifier, and it never follows you into other apps or websites.
- **If you write to us from the app**, your message reaches us with your app version, your device model and the size of your collection attached, so that a bug report can be acted on. The screen says so before you send. Section 2.7.
- **If you ask to be told when a card reaches a price**, your phone gives us a notification token so that we can reach it while the app is closed. That token identifies the installation, not you personally, and it is the only reason we hold it. We never use notifications for advertising, and turning them off in your phone's settings deletes nothing but our ability to reach you. Section 2.9.
- **We do measure how the app itself is used**, with a product analytics tool called PostHog: which screens you open, whether a scan succeeded, how long it took. It is tied to your account identifier so we can tell a returning visitor from a new one, and it carries no email address, no name, and none of the prices you enter. You can ask us to stop at any time and we will. Section 2.6 lists exactly what it sends.
- **You can delete your account at any time**, from the app, or without the app by writing to us, as explained at [logbooktcg.com/delete-account](https://logbooktcg.com/delete-account). Section 6.

The rest of this page explains the details.

## 1. Who is responsible for your data

Logbook is published by **Romain Lagrange**, an individual, based in France.

- Email: **logbook.ugc@gmail.com**

Romain Lagrange is the data controller for the processing described here, within the meaning of the EU General Data Protection Regulation (GDPR).

This policy covers the **Logbook** app on iOS (**Logbook: OP TCG Card Scanner** on the App Store, bundle identifier `com.romainl01.logbook`) and on Android (Google Play, package name `com.romainl01.logbook`), and the website **logbooktcg.com**. Where the two apps differ, this policy says so.

## 2. What we collect

### 2.1 Your account

To create an account, Logbook collects:

| Data | When | Notes |
|---|---|---|
| Email address | Sign-up with email, Sign in with Apple, or Sign in with Google | With Sign in with Google, it is the address of the Google Account you chose. With Sign in with Apple, if you choose "Hide My Email", we only ever receive an Apple relay address ending in `@privaterelay.appleid.com`. We never see your real address. |
| Password | Sign-up with email only | Stored only as a cryptographic hash by our authentication provider. We cannot read it. |
| Apple user identifier | Sign in with Apple only | An opaque identifier issued by Apple, specific to Logbook. |
| Google account identifier | Sign in with Google only (Android) | The identifier of your Google Account, issued by Google. It is how our authentication provider recognises you the next time you sign in. |
| Name | Sign in with Apple only | Apple offers your name on the first authorisation, and you can edit or decline it on Apple's own screen. If you provide it, we store it as your display name. Apple never gives it to us again, so if you decline it we simply have no name for you, and nothing in the app requires one. |
| Name | Sign in with Google only (Android) | The name on your Google Account, which Google includes in every sign-in. We store it as your display name, only if your account does not already have one. Google's sign-in also includes the address of your Google profile picture, which our authentication provider records with the other sign-in details; the app neither displays nor uses it. |
| Apple refresh token | Sign in with Apple only | Stored so that we can revoke your Apple authorisation when you delete your account, as Apple requires. It is not used for anything else. |

With Sign in with Google, we keep **no** Google token: nothing on our servers lets us act on your Google Account. That is why removing Logbook's access to it is asked from your phone when you delete your account (section 6).

That is the complete list. We do not ask for your date of birth, your phone number, your postal address or your payment details.

### 2.2 Card scans

**Your phone tries first, and most cards never leave it.** Logbook reads the card code directly on your device, using the text recognition built into your phone, and matches it against the card catalogue that ships inside the app. When that works, no photo is sent anywhere.

**On an iPhone**, that is Apple's on-device text recognition (Vision). **On Android**, it is Google's **ML Kit**: its text recognition, and its language identification, which tells a Japanese card from a Western one. The recognition models are built into the app, and Google states that ML Kit processes the image and the text entirely on the device and does not send them, or what it read in them, to Google. Google also states that ML Kit sends Google **metrics about its own performance and use**: the device's make, model and operating system version, the app's package name and version, an identifier per installation that is not meant to identify a user, the API's configuration (such as image format and resolution), input and output sizes, timings, event types and error codes, and, for language identification, the languages it identified. Google uses them, under its own terms, to measure, maintain and improve ML Kit and to detect misuse. They contain no picture, no card and nothing about your account, and we never receive them.

**When your phone cannot read the card, the photo is sent to identify it.** Since September 2026, a scan that fails on your device is sent, as a single resized photo, to our server and from there to **CardSight AI** (section 4), a service that recognises trading cards from an image. It is used to tell us which card is in the picture.

**Since 20 October 2026, we keep a copy of that photo, to understand why your phone could not read it.** Only photos of scans that already failed on your device are concerned: a card your phone reads never leaves it, as before. The copy is stored on our servers (Supabase, section 4), in a private space that only we can open, under your account identifier so that it can be deleted with your account. We look at these photos to improve recognition (a reflection on the card, a sleeve, a blurred shot, the wrong part of the image being read), and for nothing else: they are not shared, not published, and not used to train any third-party model. The photo shows what the camera saw, so it may include part of your hand or the surface the card was on; it carries no location and no camera metadata. We keep it for 90 days, then delete it automatically. If you would rather we did not keep it, write to us (section 11) and we will delete your photos and stop keeping new ones.

What we keep in addition is a technical record that a recognition request was made — when, from which part of the app, how long it took, and the card code that came back — so that we can limit how many such requests are made. That record carries your account identifier while you have an account, and loses it when you delete your account.

This only happens after a failed on-device read. If you are offline, or if the service is switched off or has reached its daily limit, nothing is sent and Logbook asks you to type the code in instead, exactly as before.

On your device, the photo stays in temporary storage, where the phone's system deletes it. Logbook does not save your scans to your photo library and does not ask for access to it.

Adding the recognised card to your collection is a separate step, and that step does reach our servers, as section 2.3 explains. What travels is the card's identity and the details you chose to record. The photograph is not part of it.

### 2.3 Your collection

Once you are signed in, your collection is stored on your account, on our servers, and kept in step with a copy on your device so the app works offline. It covers:

- your cards: which printing, how many, the condition and the grade if you recorded them, and the purchase price if you entered one;
- your sealed products: which product, which language, how many, the purchase price if you entered one;
- your wishlist.

**Why we do this.** Your collection survives a reinstall, a lost phone or a new device: you sign in and it comes back. This is a change made in August 2026. Before it, the collection existed only on the device and nothing could recover it.

**What it means for your privacy.** We hold a copy. Your rows are locked to your account in the database itself, so no other user of Logbook can read them, and we use them for nothing other than giving them back to you — with one exception you control: if you create a public profile, the cards, sealed products and wishlist on your shared page are read from these rows, as section 2.10 describes. They are deleted when you delete your account (section 6).

The price data is a separate matter and says nothing about you: the app downloads the same public price file as everybody else and caches it on your device.

### 2.4 Technical data

Like any app that connects to the internet, Logbook's requests carry technical connection data: your IP address, the time of the request, and basic device and network information. This applies when:

- your device fetches the daily price file from our public storage bucket;
- your device fetches card images from the third-party image CDN `static.dotgg.gg`, and set and sealed-product images from the third-party image CDN `tcgplayer-cdn.tcgplayer.com`;
- your device signs you in, refreshes its session, or syncs your collection with our database;
- the app asks our payments provider whether your subscription is active (section 2.5);
- the app sends the usage events described in section 2.6 to PostHog. We have turned off PostHog's location lookup, so your IP address is never turned into a city or a country, and no location is stored alongside those events.

The requests that carry your session are tied to your account by necessity: that is how the server knows whose collection to hand back. We do not build profiles from any of this, and we do not use it for anything beyond running and securing the service.

### 2.5 Subscriptions

Logbook is free up to a limited number of items in your collection, and paid above that. If you subscribe:

- **Apple or Google takes the payment.** On an iPhone, you pay through the App Store; on Android, through Google Play's billing system. We never see your card number, your billing address, or your Apple ID or Google Account password. None of it passes through us, and we store no payment method.
- **We use RevenueCat to know whether your subscription is active.** The app sends it the store's record of your purchase (the App Store transaction receipt on an iPhone, the Google Play purchase token on Android), the technical device and store information its SDK needs to match a purchase to a device, and, once you are signed in, your Logbook account identifier, so that a subscription bought on one device is recognised on the next. RevenueCat receives nothing else from us: not your email address, not your name, not your collection.

### 2.6 How you use the app

Since August 2026, Logbook measures how it is used, so that we can tell which parts work and which parts people abandon. This is done with PostHog, a product analytics tool. It is not advertising, and it does not follow you outside Logbook.

**What is sent.** One short record per meaningful action, carrying only what is needed to count it:

- **Screens you open**, named after the app's own routes (`/cards`, `/dashboard`).
- **Scans**: that you took a picture, whether a card was recognised, how long recognition took, the card's code and set, and whether you corrected our answer. When a card is **not** recognised, we also send why the reading failed — whether any text was found at all, how confident the recogniser was, and, if we read something shaped like a card code but could not match it to a card, that code. It lets us tell a blurred photo from a card missing from our catalogue. Since September 2026 we also send **how much light the camera had** at the moment you pressed the shutter — the exposure the lens settled on, and how much headroom the sensor had left — plus whether the torch was on and whether we had suggested turning it on. These are properties of the camera, of the same kind as a loading time; they describe the light in front of the lens and not the room you are in, and there is no image behind them. We send them because the scanner's own suggestion to turn the torch on has been wrong on every scan we could check, and the only way to place it correctly is to compare the light against whether the card was actually read. The photograph itself is never part of this: when a photo is sent for recognition, it goes to the service described in section 2.2 and never to PostHog.
- **Your collection changing**: that a card or a sealed product was added or removed, which one it was, and whether you recorded a purchase price.
- **The paywall**: that it was shown, which plan was highlighted, and whether a purchase completed, was cancelled or failed. The amount is the store's own public price for the plan (App Store or Google Play), not a payment detail.
- **Leaving for the marketplace**: that you tapped the buy line under a price to open that card's listing, which card it was, and which edition you were looking at. Which marketplace that is depends on the one you chose in Settings — **Cardmarket** or **TCGplayer**. We record it because we need to know whether the link is worth keeping, and whether we sent you to the right listing or only to a search. Neither marketplace is told that you came from Logbook, and neither receives anything about you from us: the tap simply opens your browser on a public page.
- **The rating question in Settings**: which of the two thumbs you tapped, and nothing else. We record it to see whether an unhappy answer actually turns into a message, so that we know if the form is worth keeping where it is. It is not a rating and it never reaches Apple or Google: a review you write on the App Store or on Google Play is between you and that store, and we cannot connect it to you here.
- **Notifications**: that we showed you our own explanation screen before your phone's system asked, that the system question was asked, and what you answered. When you open a notification, its kind (a price alert, a weekly summary…), its step in its series, and how many hours after it arrived. If you turn Logbook's notifications off in your phone's settings, the next time you open the app we record that it happened, the kind of the last notification this phone showed you, and how long before — which is the only way we can tell which of our notifications make people turn them off. And when you change a switch in **Settings → Notifications**, the new position of both switches. We record this because, on an iPhone, the system question can only be asked once in the life of an installation, so where we ask it is a decision we have to be able to judge.
- **Price alerts**: that you armed or removed an alert, whether it watches a rise or a fall, **how far your threshold sits from the price you were looking at, as a percentage**, which marketplace and which edition it was frozen against, and whether you opened the notification when it arrived. **The amount you typed is never sent**: a threshold is a figure you chose, and it is treated exactly like a purchase price — the percentage answers the same question about the product without carrying your number.
- **Your public profile and sharing** (since October 2026): that the profile step was shown, completed or skipped, and where it was opened from; whether a username you asked for was accepted, already taken or refused — **never the username itself**; whether your profile picture is one of our illustrations or a photo of yours, and whether our moderation accepted it — **never the picture**; that your profile page was opened; that you sent your link, whether your account was private at the time, and **which app your phone reports it was sent through** (Messages, WhatsApp, copy…), with nothing about the recipient; that you opened the QR code, made your account private or public, stopped sharing, or reported someone's page; and, when a shared collection opens in the app, whether it came from a link, which state it showed (a collection, an empty or private one, a link that no longer works) and whether it was your own; and on that page, that you switched between its collection and wishlist tabs, or searched it (how many characters and how many results, **never what you typed**). Since 30 October 2026, the same for a single card: that you opened the share sheet from a card's page, whether you sent the link or closed the sheet, which app your phone reports it was sent through, and whether you own that card; and, when a card link opens the app, that it arrived, whether you were signed in, and whether your version of the app knew that card. **The link itself, your username and the username, picture or value of anyone whose collection you look at are never sent.** We record this to know whether sharing brings anyone to Logbook, and whether the profile step is worth asking for.
- **Decks** (since October 2026): that you opened the Decks tab, a leader or a tournament decklist (which leader, and the size of the event in broad buckets), that you looked at the cards you are missing from a deck (with how much of it you already own, in broad buckets, never an amount), that you added those cards to your wishlist (how many), that you created (from scratch, from a tournament list, from a pasted list or as a copy, and which leader card it is built on), imported, completed, shared or deleted a deck; when you leave the deck builder, how many cards you added or removed, how many additions were refused by a rule, whether the deck is playable and its size in broad buckets; which kinds of rule a deck breaks when you open that list (for example its size or its colours, never which cards); that you reached the free limit of one deck, and from which button; and that you opened the rules or one of the official rule documents. The cards inside your decks are not sent; your decks stay on your device.
- **What brings you to Logbook** (since October 2026): the answers you tick, if any, to the introduction's first question (for example identifying your cards, tracking their value, getting price alerts or building decks), kept as a property of your analytics profile. We record this to know what new users come for and which features to put first.
- **Whether you play** (since October 2026): your answer to the introduction's question about the game (you play, you would like to learn, or you collect), kept as a property of your analytics profile.
- **Screenshots** (since October 2026): that you took a screenshot inside Logbook, and which screen you were on (its route, and the code of the card or set it showed). **The screenshot itself is never sent**, nor whether you shared it afterwards: the phone's system only tells the app that one was taken. We record this to learn which screens people capture to show others, so that those screens can get a proper share button.
- **Community moderation** (since October 2026): when a post or a reply you wrote is checked (section 2.11), our server records whether it was allowed, refused or could not be checked, the reason of a refusal (for example a scam or advertising), whether the check was in its trial mode that refuses nothing, and how long it took. **Never the text, nor the model's explanation.** We record this to know whether the check refuses people acting in good faith before it is allowed to refuse anyone.
- **Your account identifier**, so that two visits by the same person are not counted as two people. It is the same identifier described in section 2.1.
- **Which version of the app** you are running, whether it is a test build, and **which of the two marketplaces you chose** to see prices from. That last one is a setting, not a fact about you: it is what lets us read every measurement above separately for European and American users, which is the whole reason the choice exists.

**On our website, logbooktcg.com.** When someone opens a link to a shared collection in a browser, our server records that a link was opened, which of its states the page showed (a collection, an empty or private one, a link that no longer works) and the language it was displayed in. When someone opens a link to a shared card (since 30 October 2026), it records that it was opened, whether the card was found, and the language it was displayed in. When someone opens the home page, it records that the page was opened and the language it was displayed in. When someone opens the link in our social media profiles (logbooktcg.com/app), it records that it was opened, whether that happened inside the built-in browser of TikTok, Instagram or another app or in a regular browser, and whether the device is an iPhone, an Android phone or something else. When someone taps the App Store badge on the site, or is sent to the App Store by that link, it records that tap, whether it came from a shared collection, a shared card, the home page or that link, and on the home page which part of it (the top, the menu bar or the bottom). These records are made by our server, not by your browser. They carry no identifier for the visitor (each record gets a random one that is never reused), no IP address and no location. Since 15 October 2026 they also record where the visit came from: the domain of the referring site (for example `tiktok.com`, never the full address of the page), and the campaign labels (`utm_source`, `utm_medium`, `utm_campaign`) that we put on our own links. A record of a shared collection being opened also carries the random code of that link, so that we can tell which shared pages are visited most; it never carries the name of the person whose collection it is. Link previews generated by messaging apps are not counted. Since 8 November 2026, when someone taps the App Store badge on a shared collection, the App Store link carries that same random code as a campaign label, so that Apple's own statistics for developers can tell us how many downloads each shared page led to. Apple reports these as totals per code, and only for people who chose to share their analytics with app developers; it does not tell us who downloaded the app, and the code carries no name.

Since the same date, the site also runs **Vercel Web Analytics**, a small script from our hosting provider, to count visits. It sets no cookie and stores nothing on your device. It records the page address (for a shared collection, that includes the link's random code), the referring site, the country derived from the IP address, and the type of device, browser and operating system. To count a visitor once per day, it computes an identifier from the request that is discarded after 24 hours; it never stores the IP address. These figures are aggregated: we see totals per page, per referring site and per country, not individual visitors.

**What is never sent.** Your email address. Your name. The prices you enter for your own cards, whether you paid them or sold at them: those are sent as "a price was recorded", never as a figure. The total value of your collection leaves only as a broad band (for example "250 to 1000 euros"), never as an amount. No photograph, no advertising identifier, and nothing that follows you into another app.

**Why we do this.** Legitimate interest, Art. 6(1)(f): a project this small cannot otherwise tell whether the scanner works on real cards, or whether people give up before their first one. We have kept the data minimal precisely so that this basis is honest, and we treat it as measurement of the product rather than knowledge about you.

**How to object.** Because this rests on legitimate interest and not on your consent, you have the right to object to it (GDPR Art. 21). Write to **logbook.ugc@gmail.com** and we will stop collecting these events for your account and delete the ones already recorded. There is no switch inside the app: the app does not ask you, and it does not let you turn it off by yourself.

### 2.7 Feedback you send us

Settings has a **Send feedback** screen where you can report a bug, tell us a card or a price is wrong, or suggest something. Nothing here is collected unless you write a message and tap send.

**What is sent:**

- **Your message**, exactly as you wrote it, and which of the three kinds you picked.
- **Your account identifier**, so that we can reply to you and so that deleting your account also deletes what you sent (see section 5).
- **Context about your app and your phone**, gathered automatically so that a report is actually actionable: the app version and build number, whether it is a test build, your device model, its operating system version, and the language the app was displaying.
- **The size of your collection**: how many cards and how many sealed products you hold, and whether you have reached the limit of the free tier. This is what lets us tell a real bug from a limit working as designed. It is a count, never a list of what you own.

The screen states all of this on itself, above the send button, before you send anything.

**What is never sent.** Your photographs. Your cards themselves. Any price you entered for something you own. Your location.

**Where it goes.** The message is stored in our database (section 4, Supabase) and a copy is emailed to us so that we read it. The email is delivered by **Resend**, and it carries your email address in its reply-to field, which is what lets us answer you directly. If you would rather write to us without any of this context attached, email **logbook.ugc@gmail.com** instead: it reaches the same person.

**Why we do this.** Legitimate interest, Art. 6(1)(f): we cannot fix what we are not told about, and a report without a version number and a device model usually cannot be acted on at all. You are never asked for feedback and never prompted for it: every message here exists because somebody chose to write it.

### 2.8 Prices you report as wrong

Every card in the app carries a market price we did not set: it comes from Cardmarket, matched to the card by us, and the matching is sometimes wrong. On a card's price, the **?** opens a sheet explaining where the figure comes from, and at the bottom of that sheet you can tell us the price looks wrong. Nothing here is collected unless you pick a reason and tap send.

**What is sent:**

- **What you said is wrong with it**: which of the four reasons you picked, what you think the card is roughly worth if you chose to say, and your message if you wrote one.
- **Which card**, so that we know what to check: its code, its printing, and which of the two Cardmarket editions was on your screen.
- **The price we were showing you and where we got it**: the figures displayed, the Cardmarket listing we had matched the card to, whether that match was an estimate, and the date of the price file your app was using. This is what lets us reproduce what you saw instead of guessing at it, and it is the whole reason this form exists separately from the one in section 2.7.
- **Your account identifier**, so that we can come back to you if we need to and so that deleting your account also deletes what you sent (see section 5).
- **Context about your app and your phone**, exactly as listed in section 2.7: app version and build number, whether it is a test build, device model, operating system version, and the language the app was displaying.

The sheet states all of this on itself, above the send button, before you send anything.

**What is never sent.** Your collection. Your photographs. Any price you entered for something you own. Your location. The figure you give us here is what you think a card is worth on the open market, which is a public fact about a product; it is not, and is never confused with, what you paid.

**Where it goes.** The report is stored in our database (section 4, Supabase) and a copy is emailed to us by **Resend**, exactly as feedback is.

**Why we do this.** Legitimate interest, Art. 6(1)(f): a price we display wrongly is a defect in the product, and users holding the actual cards are the only people who can catch a whole class of them. A report without the card and the price file it came from cannot be acted on at all. You are never asked to report a price and never prompted to: every report here exists because somebody went looking for the form.

### 2.9 Notifications

Since September 2026, Logbook can tell you when a card reaches a price you chose, for the cards you asked us to watch. It can also send a summary of your collection and a few reminders, which have their own switch (see *Summaries and reminders* below). None of them is advertising, and none of them names a price or the subscription's cost.

To reach your phone while the app is closed, we have to hold three things about the installation itself.

**What is sent:**

- **A notification token.** It is issued by Apple on an iPhone, or by Google through Firebase Cloud Messaging on Android, and obtained through Expo, and it identifies **the installation of the app on that phone** — not you as a person. It is the address your device answers at; without it no notification can be delivered. It changes when you reinstall the app, and it stops working when you delete it.
- **The time zone of your phone**, refreshed each time you open the app. It exists for one reason: we never send anything before 9am or after 9pm, and the only clock that matters is the one in your pocket. Without it we would be sending on a server's hours, which for some of you would mean the middle of the night.
- **The language the app is displaying**, for the same kind of reason: the notification's text is written on our servers, not in the app, so without this it would arrive in English on a French phone.
- **Whether each kind of notification is on**, as you set it in Logbook's own Settings. Price alerts are decided on our servers, so that switch has to travel with the token — otherwise turning it off would change what the app says and not what the app does.
- **When you last opened the app**, refreshed at most once every ten minutes while you use it. It is a single date, overwritten each time, and it exists so that we space out what we send and never write to you when you have just been in the app.
- **Whether your subscription is active**, as RevenueCat reports it to the app (section 2.5), or that we do not know yet. It is a yes, a no or an unknown — never a price, a plan or a payment detail. When we do not know, we treat you as a subscriber, which means we write less, not more.
- **That you closed a paywall without subscribing**, where it was shown, and whether it was the free tier's 10-item limit that opened it. It is a date and those two facts, never a plan or a price, and it is what lets us decide whether a reminder about the subscription is worth sending — and when to stop.
- **That you opened a notification**, and when. It is recorded against the notification we sent, not against anything you were doing, and it is what tells our servers to slow down for someone who stops opening them.

**What a notification itself carries.** The card's code, and which way its price moved. **Never a figure**: not your threshold, not the price. That is a deliberate product decision and not an oversight — the app shows prices on a marketplace, a price basis and an edition that you chose and that live only on your phone, so any amount we wrote on your lock screen could contradict the one you read three seconds later when you opened the app.

**What is never sent.** Your email address, your name, your collection, your location. A notification token is not an advertising identifier: it cannot be read by any other app, it identifies nothing outside Logbook, and we never share it with anyone but the delivery services below.

**Where it goes.** The token is stored in our database (section 4, Supabase). To deliver a notification we hand it to **Expo**, whose push service relays it to **Apple's Push Notification service** on an iPhone, or to **Google's Firebase Cloud Messaging** on Android, which delivers it to your phone. Expo, and Apple or Google after it, therefore see the token and the text of the notification; they see no account of yours, because we identify the device and never the person.

**Summaries and reminders.** Besides the alerts you arm yourself, Logbook can send a summary on Sundays when your collection has moved, and a few reminders. They are governed by their own switch, **Summary and reminders**, independent from price alerts. If you stop opening the summaries, we slow them down to one a month, and the switch says so. Since November 2026, one of these reminders can tell you that **someone you follow, or who follows you, is looking for a card you own** (section 2.12); it carries that person's nickname and the card's name, and counts within the same limits as the other reminders.

**How to stop it.** Turn the switches off in Logbook's **Settings → Notifications**, or turn Logbook's notifications off in your phone's settings, which overrides everything. **Signing out releases the token immediately**, so a phone you have signed out of stops receiving anything for that account — this matters on a shared device. Deleting your account deletes the token with it. On an iPhone, the system only ever asks the question once, so refusing it the first time is a definitive answer as far as the app is concerned: only a trip to the iPhone's Settings can reopen it. On Android, a refusal can be asked again, and the phone's settings can change your answer at any time.

**Why we do this.** Performance of the service you asked for, Art. 6(1)(b): an alert you armed yourself cannot be delivered without an address to deliver it to.

### 2.10 Your public profile and shared collection

Since October 2026, you can share your collection with a link. **Nothing is shared until you create a public profile**, and creating one is optional: the rest of the app works the same without it.

**What you give us.**

- **A nickname**, which you choose (3 to 20 characters). If you skip the step, we generate one for you of the form `nakama-1234`. It is unique across Logbook and it is public: it is the name on your page.
- **A profile picture**, which is either one of the pirate illustrations that ship with the app, or a photo you choose from your library. When you choose a photo, the app only receives that one image, resized on your phone to 512 pixels; it does not get access to the rest of your library.

**The photo is checked before it is published.** A photo you add is sent from our server to **OpenAI's moderation service** (section 4), which tells us whether it contains violent, sexual or otherwise inappropriate content. That is its only use: it is sent without your name, your email or your account identifier, and under OpenAI's terms for its API, what we send is not used to train its models. **A photo that is refused is not stored anywhere**, and if the moderation service cannot be reached, the photo is not published either: you are asked to try again. An accepted photo is stored on our servers under a random file name that does not contain your account identifier.

**What anyone with your link can see.** Your page lives at `logbooktcg.com/c/` followed by a random code that we generate. It can be opened in the Logbook app by a signed-in user, or in any web browser, by **anyone who has the link**, so treat it the way you would treat any link you post. It shows:

- your nickname and your profile picture;
- your cards (which printing, which language, how many) and your unopened sealed products (which product, which language, how many), in the order you added them;
- your wishlist (since 11 October 2026): which printings you want, the edition you asked for if any, and when you added them;
- the market value of what is shown, worked out from the same public price file as everywhere else in the app.

**What it never shows**: your email, the name Apple or Google gave us, your account identifier, the price you paid for anything, whether you bought or pulled a card, its condition or grade, and products you have opened. **A private account shows neither your cards nor your wishlist.** Our server only ever releases the fields listed above; the rest never leaves the database.

The page is marked so that search engines do not index it, and the code in the link is long enough that it cannot reasonably be guessed. It is still a public page: anyone you send the link to can forward it.

**How to control it.**

- **Private account.** In your profile or in **Settings**, turn on *Private account*. Your page then shows only your nickname and your profile picture, and no card at all. Your link keeps working.
- **Cancelling the link.** In **Settings**, you can cancel your link. Anyone who opens the old link then sees that the collection is no longer available, and sharing again creates a new link with a new code.
- **Changing your nickname or photo.** At any time, from your profile. Replacing a photo with a pirate illustration deletes the photo from our servers.
- **Subscription.** If your subscription ends and your collection holds more items than the free plan allows, your page stops being shown until you subscribe again or come back within the free limit.

**Reporting a page.** A signed-in user can report someone else's page from the app, with an optional reason (up to 1,000 characters). We record who reported which page, when, and the reason, and we receive it by email so that a person reviews it. The page owner is not told who reported them. We may remove a nickname or photo that breaks our terms.

**On the website.** The page is served by our hosting provider, Vercel (section 4). Like any web server, it receives the visitor's IP address in order to answer; we use it only to limit how many pages a single address can request per minute, and we do not record it ourselves; Vercel's own request logs keep it briefly, under its policy. What our server records about visits is described at the end of section 2.6.

### 2.11 The community

Since October 2026, subscribers can join the Logbook community: channels by language where you can write posts, reply, and like posts and replies. **Nothing is published unless you write it**, and reading the community does not require you to post.

**What you give us, and who sees it.**

- **Posts and replies**: a title, a text, optionally a tag (such as « Question » or « Pull ») and a card from the catalogue. They are shown to **every subscriber** who opens the community, with your nickname and your profile picture (section 2.10), and the date.
- **Likes**: who liked what. Others see how many likes a post or a reply has, and whether they liked it themselves; they do not see a list of who liked it.
- **Acceptance of the community rules**, with its date, recorded the first time you write.
- **Blocks and reports**: who you blocked, and what you reported, with an optional reason. The person you block or report is not told. Blocking someone hides their posts and replies from you, and yours from them.
- **The value of your collection, next to your nickname**: the total market value of your collection as of the previous night, rounded (for example « 16.3k € »), or the word « New » when it is 100 or less. It is the same figure your public page shows (section 2.10), never what you paid. **If your account is private, no value and no « New » appears**, and the figure never leaves our servers.
- **Your public page**: tapping your nickname in the community opens your shared collection page (section 2.10). If you never shared it, a link is created the first time a subscriber taps your nickname. *Private account* still applies: a private page shows no card.

**Text is checked before it is published.** A post or a reply is sent from our server to **OpenAI** (section 4), twice at the same time: to its **moderation service**, which tells us whether it contains hateful, violent, sexual or otherwise inappropriate content, and to one of its **language models**, which tells us whether it is a scam or a payment arranged outside Cardmarket and Vinted, a mention of another collection app, advertising or self-promotion, or a post that belongs in another channel (in which case the app suggests the right one). Payment links and bank details of the kind that only a scam would post are recognised by our own server, without being sent anywhere. The text is sent with the channel and the language it was written in, without your name, your email or your account identifier, and under OpenAI's terms for its API, it is not used to train its models. The model only returns a verdict: the message you see when a text is refused is written by us, not by the model. If a check cannot be completed, nothing is published and you are asked to try again.

**What we keep about this check.** We record each decision (allowed or refused, the reason, and a one-line explanation written by the model for the person who reviews moderation) with your account identifier. **A refused text is kept for 30 days**, only so that a person can check the refusal was right, and is then deleted. A published text is not copied: the record points to the post or the reply. These records are never shown to other members, are deleted after 30 days, and go with your account when you delete it. While we measure how well this check works, it may run without refusing anything: your post is then published normally and only the record is kept.

**Reports.** A report reaches us by email so that a person reviews it. Content reported by three different people is hidden automatically until we have looked at it. We may remove content, and exclude from the community anyone who breaks its rules.

**Notifications.** When someone replies to your post, we may send you a notification (section 2.9), at most one per post every fifteen minutes. Its text contains the replier's nickname and the beginning of the reply.

**Deleting.** You can delete your own posts and replies at any time: they disappear for everyone. We keep a deleted post or reply internally, without showing it, so that a report about it can still be reviewed; it goes with your account when you delete it.

**Subscription.** If your subscription ends, you can no longer read or write in the community. What you wrote stays visible to subscribers, under your nickname, until you delete it or delete your account.

### 2.12 Following other collectors

Since November 2026, you can follow other Logbook members, from their page or by scanning the QR code of their profile. Following is free, needs nobody's approval, and you can stop at any time.

**What we record.** Who follows whom, and since when. Nothing else is stored: the numbers of followers, the activity and the matches described below are worked out from it, and from your collection and wishlist (section 2.3), each time they are shown. We also keep, **for one hour**, the time of each follow and unfollow, only to limit changes to 60 an hour so that nobody can flood someone with follow notifications.

**Who sees what.**

- **The person you follow sees that you follow them**: your nickname and profile picture appear in their list of followers, and in their club feed. Anyone can see how many followers a member has and how many people they follow; the lists of another member's followers are not shown.
- **If your account is public, the people who follow you see what you add**: in the club, grouped by session (« added 20 cards », « added 3 cards to their wishlist »), with the cards' market value and never what you paid; on a card's page, that you own it, how many copies and in which languages; on their own wishlist, that you own a card they want. This activity is only shown inside the club, which is reserved to subscribers (section 2.11).
- **A private account shows none of it**: no cards, no wishlist, no activity, no value. Because the activity is worked out when it is read, making your account private hides your past activity at once.
- **Blocking** someone in the community (section 2.11) also works here, in both directions: you can no longer follow each other, and neither of you appears to the other.
- **Notifications.** When someone you follow, or who follows you, adds to their wishlist a card you own, we may tell you so (section 2.9): only for a wish less than 48 hours old and made after you started following each other, once per person and per card, and never for a private account. It carries their nickname and the card's name.

**What is never shared.** Your email, your account identifier, what you paid for anything, and the list of people who follow someone else.

**Deleting.** Unfollowing removes the record immediately. Deleting your account removes every follow, in both directions.

**Why we do this.** Performance of the service you asked for, Art. 6(1)(b): following someone is a feature you use yourself, and it cannot work without recording who you follow.

## 3. Why we process it, and on what legal basis

| Purpose | Data | Legal basis (GDPR Art. 6) |
|---|---|---|
| Creating and running your account, letting you sign in | Email, password hash, Apple or Google identifier, name | Performance of a contract, Art. 6(1)(b) |
| Storing your collection so it survives a reinstall or a new phone, and keeping your devices in step | The collection data listed in section 2.3 | Performance of a contract, Art. 6(1)(b): this is the service |
| Revoking your Apple authorisation when you delete your account | Apple refresh token | Performance of a contract, Art. 6(1)(b), and our legitimate interest in meeting Apple's platform requirements, Art. 6(1)(f) |
| Selling a subscription, and recognising it on your other devices | Store transaction data (App Store or Google Play), your account identifier | Performance of a contract, Art. 6(1)(b) |
| Keeping the service available and secure (technical logs, abuse prevention) | Technical connection data | Legitimate interest, Art. 6(1)(f) |
| Improving card recognition, by looking at the scans it failed on | The photo of a failed scan, section 2.2 | Legitimate interest, Art. 6(1)(f): a recognition that fails without anyone seeing why cannot be fixed. You can object at any time, see section 2.2 |
| Understanding how the app is used, so we can improve it | The usage events listed in section 2.6 | Legitimate interest, Art. 6(1)(f). You can object at any time, see section 2.6 |
| Reading and answering feedback you send us | The message and context listed in section 2.7 | Legitimate interest, Art. 6(1)(f) |
| Correcting the prices we display when a user reports one as wrong | The report and context listed in section 2.8 | Legitimate interest, Art. 6(1)(f) |
| Showing your public profile and shared collection to the people who have your link | Nickname, profile picture, and the collection data listed in section 2.10 | Performance of a contract, Art. 6(1)(b): sharing is a feature you switch on |
| Checking a profile photo before publishing it, and handling reports | The photo, and the report listed in section 2.10 | Legitimate interest, Art. 6(1)(f): keeping public pages free of inappropriate content, and meeting App Store and Google Play requirements for user-generated content |
| Telling you when a card you asked us to watch reaches your price | The notification token, time zone and language listed in section 2.9 | Performance of a contract, Art. 6(1)(b): the alert is the service you asked for |

We do not process any special category data, and we do not use your data for automated decision-making with legal effects.

## 4. Who else is involved

We use a small number of service providers ("processors"). They act on our instructions and for no other purpose.

| Provider | Role | Where | Data involved |
|---|---|---|---|
| **Supabase, Inc.** (United States) | Hosts the accounts database, your collection, your public profile and profile photo, and our server functions | Project hosted in the EU (Paris, France) | Account data, collection data, nickname and profile photo |
| **RevenueCat, Inc.** (United States) | Tells the app whether your subscription is active, and validates App Store and Google Play purchases | United States | Store transaction data, your account identifier, device information |
| **Apple Inc.** | Sign in with Apple, App Store distribution, subscription payments, delivery of notifications to an iPhone | United States | Your Apple sign-in, your purchase, the notification token and text (section 2.9) |
| **Google LLC** (United States) | On Android: Sign in with Google, Google Play distribution, subscription payments (Google Play Billing), delivery of notifications (Firebase Cloud Messaging), and the on-device text recognition (ML Kit) | United States | Your Google sign-in, your purchase, the notification token and text (section 2.9), and ML Kit's technical usage metrics (section 2.2), which contain no picture and nothing about your account |
| **PostHog, Inc.** (United States) | Product analytics: tells us which screens are used and whether scans succeed | United States | The usage events listed in section 2.6, and your account identifier |
| **Resend (Plus Five Five, Inc.)** (United States) | Delivers the notification email when you send feedback, report a price, or report a shared page, from the app | United States | The feedback message and context listed in section 2.7, the price report listed in section 2.8, the page report listed in section 2.10, and your email address |
| **CardSight AI, Inc.** (United States) | Recognises a card from a photo when your phone could not read it (section 2.2) | United States | The photo of the card, sent without your name, email or account identifier |
| **OpenAI, L.L.C.** (United States) | Checks a profile photo (section 2.10) and the text of community posts and replies (section 2.11) before they are published: inappropriate content, and for text also scams, advertising, mentions of other collection apps and the channel it belongs in | United States | The photo you chose, or the text you wrote with its channel and language, sent without your name, email or account identifier. A refused photo is not stored by us; a refused text is kept by us for 30 days (section 5) |
| **Vercel Inc.** (United States) | Hosts our website, including the shared collection pages (section 2.10) | United States, served from the network location nearest the visitor | The visitor's IP address, as for any website; the content of a shared page while it is being displayed |
| **Expo (650 Industries, Inc.)** (United States) | Relays a notification from our servers to Apple's Push Notification service (iPhone) or Google's Firebase Cloud Messaging (Android) | United States | The notification token described in section 2.9, and the text of the notification. No account of yours: we address the device, never the person |

**Transfers outside the European Union.** All ten companies above are established in the United States. Our Supabase project itself runs in the European Union (Paris), so your account and your collection are stored on EU servers, but Supabase's American parent company can access them for support and operations. Subscription data goes to RevenueCat in the United States. Those transfers are covered by the standard contractual clauses and safeguards published by each of those providers.

Card images displayed in the app are loaded from the third-party CDN `static.dotgg.gg`, and images of sets and sealed products from the third-party CDN `tcgplayer-cdn.tcgplayer.com`. Both receive your IP address as part of any ordinary image request. Neither is a processor acting on our instructions: they are simply the hosts your device requests an image from.

**We never sell, rent or trade your data, and we never share it for advertising purposes.** We only disclose data where the law requires it.

## 5. How long we keep it

| Data | Retention |
|---|---|
| Account data (email, password hash, Apple or Google identifier, name) | For as long as your account exists. Deleted when you delete your account. |
| Apple refresh token | Same as above. Used once during deletion, to revoke the authorisation, then deleted. |
| Your collection, your sealed products, your wishlist | For as long as your account exists. Deleted when you delete your account. Removing a card removes it from your other devices too, and leaves behind only a marker saying it was removed, which is how your devices learn about the removal. That marker goes with the account. |
| Scan photos | A photo your phone could read never leaves it. A photo sent for recognition after a failed read (section 2.2) is kept for 90 days, then deleted automatically, and deleted with your account if you delete it sooner. |
| Nickname, profile photo, privacy setting, share link (section 2.10) | For as long as your account exists, or until you change them: a replaced photo is deleted, a cancelled link stops working immediately. All of it is deleted when you delete your account. |
| A photo refused by moderation | Never stored by us. |
| Moderation records of community text, including a refused text (section 2.11) | 30 days, then deleted. Deleted earlier with your account. |
| Community posts, replies and likes (section 2.11) | For as long as your account exists, or until you delete a post or a reply. A deleted post or reply is kept hidden, so that a report about it can still be reviewed, and goes with your account. |
| Community blocks, reports and rules acceptance (section 2.11) | For as long as both accounts exist. The notification email of a report stays in our mailbox. |
| Who you follow and who follows you (section 2.12) | Until you unfollow, or for as long as both accounts exist. The record of follow changes used for the hourly limit is deleted after an hour. |
| Reports of a shared page (section 2.10) | For as long as both accounts exist: a report is deleted when either the person who sent it or the person it concerns deletes their account. The notification email we received stays in our mailbox. |
| Subscription data at RevenueCat | For as long as RevenueCat needs it to recognise your subscription and honour a restore, in line with its own retention policy. A purchase record necessarily outlives a cancellation, otherwise restoring a subscription could not work. |
| Technical logs of our server functions | Short-lived, in line with Supabase's own log retention. They contain error messages and technical metadata. |
| The local copy on your device | Until you delete the app, or until you delete your account, which wipes it. |
| Feedback you sent (section 2.7) | For as long as your account exists: the record is attached to your account and is deleted with it. The notification email we received is a separate copy and stays in our mailbox, like any email anybody sends us. |
| Price reports you sent (section 2.8) | The same, and for the same reason: the record is attached to your account and is deleted with it, and the notification email is a separate copy that stays in our mailbox. |
| Notification token, time zone and language (section 2.9) | For as long as your account exists, and only while the installation is alive and signed in: signing out releases it. A token that Apple or Google tells us no longer exists — you deleted the app, or turned notifications off at the system level — is marked dead and stops being used. Deleting your account deletes it. |
| Usage events at PostHog (section 2.6) | Kept while they are useful for reading trends. They are not stored with your account, so deleting your account does not automatically erase them: ask us and we will delete them. |

## 6. Deleting your account

You can delete your account from inside the app: on **Home**, tap your profile picture at the top, then the gear (**Settings**), then **Delete account** in the **Account** section. No email, no form, no waiting period.

**Without the app.** If you no longer have the app, or no longer have a phone it runs on, write to **logbook.ugc@gmail.com** from the email address of your account (with Sign in with Apple or Sign in with Google, the address that sign-in uses), with the subject **"Delete my account"**. We then delete it, with everything listed below, and reply to confirm, within the one month the GDPR allows (section 7). The same instructions are on [logbooktcg.com/delete-account](https://logbooktcg.com/delete-account).

Deleting your account:

- permanently deletes your account and everything attached to it from our servers: email, password hash, Apple or Google identifier, name, Apple refresh token, your collection, your sealed products, your wishlist, your nickname, your profile photo and your share link (which stops working at once), and any feedback, price report or page report you sent from the app;
- revokes Logbook's Sign in with Apple authorisation with Apple, where applicable;
- with Sign in with Google, asks Google to remove Logbook's access to your Google Account. That request leaves from the phone you delete from, because we hold no Google token (section 2.1): if you delete from another phone, or by email, Logbook may still be listed among the apps connected to your Google Account, and you can remove it there yourself;
- **wipes your collection, your sealed products, your wishlist and all locally cached data from the device you are signed in on.**

It takes effect immediately and cannot be undone. There is no "deactivated" state and no soft delete: your data is not archived somewhere in case you come back.

**Deleting the app is not the same thing.** It removes the local copy from that device, but your account and your collection stay on our servers until you delete the account itself, and signing in again on any device brings the collection back.

**Deleting your account does not cancel a paid subscription.** A subscription is managed by the store you bought it from, not by us: an App Store subscription is cancelled in your Apple account settings, a Google Play subscription in the Play Store's **Subscriptions**. Do that first if you are subscribed.

## 7. Your rights

Under the GDPR you have the right to:

- **access** the data we hold about you;
- **rectify** it if it is inaccurate;
- **erase** it (see section 6: the in-app deletion does exactly this, and so does a request by email);
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
- **No notification you did not ask for.** Since September 2026 Logbook can notify you, and it only ever does so about a card you personally asked it to watch, at a price you personally typed. No promotion, no "come back", no advertising. Section 2.9 lists what a notification carries — and, as importantly, that it never carries a figure.
- **No cross-app tracking.** No attribution SDK, no third-party tracker, no advertising identifier. A notification token is not one of those: it is an address your own device answers at, it means nothing to any other app, and it identifies the installation rather than you. We do not follow you into other apps or websites, and we do not ask you to allow tracking, because there is nothing to allow. We do measure how Logbook itself is used, which is a different thing, and section 2.6 is explicit about it.
- **No profiling.** We do not build a profile of you and we do not enrich your data from other sources.
- **No data sales.** We do not sell your data, and we will never make selling it part of the business model. If this ever changes, it will require your explicit prior consent, and a new version of this policy.
- **No other use of your collection.** We store it so that you cannot lose it, and for nothing else: it is not shown to other users unless you create a public profile to share it (section 2.10), and then only the parts that section lists; it is not published as market data, and not sold. Holding a backup does mean we are technically able to read it, as is true of any service that stores anything on your behalf, and we do not look at it beyond keeping the service working.

## 9. Children

Logbook is not intended for children under 13, and we do not knowingly collect data from them. If you are below the age of digital consent in your country (15 in France), you need a parent or guardian to agree on your behalf. If you believe a child has created an account, contact us at **logbook.ugc@gmail.com** and we will delete it.

## 10. Changes to this policy

We may update this policy as the app evolves. The date at the top always reflects the most recent version, and significant changes will be announced in the app before they take effect.

**The 11 November 2026 version records one change: Logbook is coming to Android.** Section 1 now covers the Android app. Section 2.1 adds Sign in with Google (your Google Account's email, identifier and name), section 2.2 Google's ML Kit, which reads cards on the phone and sends Google technical usage metrics, section 2.5 Google Play's billing, and section 2.9 Firebase Cloud Messaging, which delivers notifications on Android. Google appears as a tenth company in section 4. Section 6 adds a way to delete your account without the app, by email, also published at logbooktcg.com/delete-account. Wording that only described an iPhone ("iOS Settings", "App Store") now covers both.

**The 8 November 2026 version records one change: the App Store badge on a shared collection carries that link's code.** Section 2.6 says what it is for (counting downloads per shared page in Apple's developer statistics), that Apple reports it only as totals, and that it carries no name.

**The 6 November 2026 version records one change: you can follow other collectors.** Section 2.12 says what we record (who follows whom, since when, and for one hour the time of each change), who sees what, that a private account shows nothing, and how blocking applies. Section 2.9 adds the reminder « someone is looking for a card you own », and section 5 its retention. No new processor is involved.

**The 21 October 2026 version records one change: community text is checked for more than inappropriate content.** Section 2.11 says what the second check looks for (scams and payments outside Cardmarket and Vinted, other collection apps, advertising, the wrong channel), that it is done by a language model from OpenAI (already in section 4), and that a refused text is now kept for 30 days so that a person can check the refusal — the previous version said refused text was not stored anywhere. Section 5 adds that retention, and section 2.6 the measurement of the check.

**The 20 October 2026 version records one change: the community shows the value of each member's collection next to their nickname.** Section 2.11 says what is shown (the previous night's total, rounded, or « New » up to 100), and that a private account shows nothing. No new data is collected: the figure is the one we already compute every night for your own value history.

**The 20 October 2026 version also records a second change: we now keep the photo of a scan your phone could not read.** Until now, that photo was sent to the recognition service and not stored. It is now kept for 90 days in a private space only we can open, so that we can see why recognition failed and fix it. Section 2.2 says what it may show, and how to ask us to delete it; section 5 says how long it is kept. A scan your phone reads still never leaves it.

**The 19 October 2026 version records one change: subscribers can join the community.** Section 2.11 lists what is published there and to whom, how text is moderated before it is published (OpenAI, already in section 4, now also checks community text), how blocking and reporting work, and how long it is all kept.

**The 15 October 2026 version records one change: the website now measures where its visitors come from.** Our server adds the referring domain and our own campaign labels to the visits it already counted, and the code of a shared link to the record of that link being opened. The site also runs Vercel Web Analytics, a cookieless visit counter from our hosting provider. The app itself is unchanged. Section 2.6 describes both.

**The 10 October 2026 version records one change: you can now share your collection.** It is optional and off until you create a public profile. Section 2.10 lists what a shared page shows (never what you paid), how to make it private or cancel the link, and how reports work. It adds two processors to section 4: OpenAI, which checks a profile photo before it is published, and Vercel, which hosts the website the shared pages are served from. It also corrects section 5, which still said scan photos never leave your phone after the 22 September version had changed that.

**The 22 September 2026 version records one change: a card your phone cannot read can now be sent to a recognition service.** Until now, recognition ran only on your device and a failed read meant typing the code in. Now, only after a failed read, the photo is sent to CardSight AI to identify the card (section 2.2), which adds a seventh processor to section 4. Cards your phone reads itself — most of them — still never leave it.

**The 20 September 2026 version records one change: the app can now send you notifications.** It could not before, and an earlier version of this policy did not mention them at all. What is new on our side is that we hold a notification token — an identifier for the installation of the app on your phone — together with your time zone and the app's language, and that a sixth processor (Expo) appears in section 4 because it is what relays a notification to Apple. Section 2.9 describes all of it, including the two things it is worth knowing without reading it: we never send anything before 9am or after 9pm in your own time zone, and a notification never carries a price figure. Nothing here happens unless you arm an alert yourself, and iOS asks its own question before any of it is possible.

The August 2026 version records four such changes. Card recognition became entirely on-device, so no photo is sent anywhere any more. Collections started being stored on your account rather than on the device alone, so we now hold a copy of something we previously did not. And the app began measuring its own use, described in section 2.6, which an earlier version of this policy said it did not do: that sentence was true when it was written and is not any more, and replacing it rather than quietly deleting it is the point of this paragraph. You can object to the measurement at any time by writing to us, as section 2.6 explains. And the app gained a feedback screen, described in section 2.7: it collects nothing unless you write a message and send it, and the screen itself lists what travels with it before you do. That is the announcement this paragraph would otherwise owe you: there is no way to reach it by accident. A second form of the same kind was added at the end of August, described in section 2.8: it lets you tell us a card's price is wrong, it sits behind the **?** on that card's price, and it too collects nothing unless you fill it in and send it. It carries more than the feedback screen does, because a price we cannot reproduce is a price we cannot fix, and section 2.8 lists every field of it.

## 11. Contact

Questions about this policy, or about your data: **logbook.ugc@gmail.com**.
