# TextFromSMS

<img src="assets/TextFromSMS.png" alt="TextFromSMS icon" width="128" height="128">

Export a message conversation to readable text, share it, or print it.

**[Official downloads](https://github.com/Mike134/textfromsms-releases/releases)** ·
[User guide](TextFromSMS%20User%20Guide.md) · [Privacy](PRIVACY.md) · [Signing](SIGNING.md)

## Download version 1.0.0

Select **TextFromSMS-1.0.0.apk** under Assets on
[the release page](https://github.com/Mike134/textfromsms-releases/releases/tag/v1.0.0).
Android 11 or newer is required. Basic use was reported successful on two phones of the same
model running Android 16. Updating from the private prototype to the signed release candidate
was also confirmed working. Other devices and Android versions have not yet been verified.

## Features

- Choose an SMS/MMS conversation and search by contact name or number.
- Optionally use saved contact names; outgoing messages are labeled You.
- Hide unwanted entries locally and restore them later.
- Preview oldest first or newest first.
- Save UTF-8 text, share a text attachment, print, or save PDF through Android's print service.
- Process messages locally with no Internet permission, advertising, or analytics.

**RCS completeness is unverified.** Messages Android does not expose can be missing.
Compare important exports against your messaging app. Photos and other MMS media appear as
attachment markers; the media itself, MMS subjects, drafts, and failed/outbox messages are excluded.

## Install

1. Download the official APK on your phone and open it. Allow installation from your browser or
   file manager if Android asks. Developer mode and USB debugging are not needed.
2. For an existing installation, choose Update. Do not uninstall first. If Android reports
   a signing conflict, report it before clearing data or uninstalling.
3. Open TextFromSMS and tap Read conversations. Grant SMS access; Contacts access is optional.
4. If SMS is greyed out or says Restricted setting: open App info, use the three-dot menu →
   Allow restricted settings, authenticate, then allow SMS in Permissions.
5. Choose a conversation, check its preview, and use Save .txt, Share, or Print.

For PDF on phones that show Preview mode: select it, then use its three-dot menu → Save as PDF.
Other print services may offer Save as PDF directly.

## Official copies and support

This repository is the official downloads and documentation location maintained by **Mike134**.
Application source remains private. Use the APK from Releases and see [SIGNING.md](SIGNING.md)
for the certificate fingerprint. Checksums detect file changes; the official signing certificate
identifies a release. The app's About button links back here.

Report reproducible problems using [Issues](https://github.com/Mike134/textfromsms-releases/issues).
Include app version, Android version, phone model, installation method, and steps to reproduce.
**Do not post message exports, contact names/numbers, authentication codes, or private screenshots.**
This is a small project; support response times are not guaranteed.

See [distribution terms](LICENSE.md) and [third-party notices](THIRD_PARTY_NOTICES.md).
