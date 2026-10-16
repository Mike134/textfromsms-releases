# TextFromSMS User Guide

For version **1.0.0** · Updated October 16, 2026

## What TextFromSMS does

TextFromSMS lets you select a message conversation, preview its text, and then save, share, or
print it. It reads SMS and MMS messages that Android makes available to the app. It does not
change the original messages in Google Messages.

**Check important conversations against Google Messages before relying on an export.** RCS
messages may be missing even when the conversation appears in TextFromSMS. A tested conversation
matched Google Messages and the exported text file, but this does not establish
completeness for every conversation or device.

## Get started

TextFromSMS requires Android 11 or newer and has been tested on Android 16.
Download the APK from the [official TextFromSMS releases page](https://github.com/Mike134/textfromsms-releases/releases).
The app's **About TextFromSMS** button also links to this official location.

Install the release APK by opening it on your phone. If prompted, allow the browser or file
manager you are using to install apps from that source. For an existing TextFromSMS installation,
choose **Update** rather than uninstalling first. Updating from the private prototype to the signed
release candidate was confirmed working on Android 16. The release uses the same signing key as
that candidate. If Android reports a signing conflict, report it before uninstalling or clearing data.

1. Open **TextFromSMS** on your phone.
2. Tap **Read conversations**.
3. If Android requests SMS access, allow it so TextFromSMS can read your messages.
4. Tap a conversation in the list to open its preview.
5. Choose **Save .txt**, **Share**, or **Print**.

You do not need to make TextFromSMS your default messaging app.

### If Android restricts SMS permission after an APK download

Android may let you allow Contacts while keeping SMS disabled or showing **Restricted setting**
for an app installed from a browser. In that case:

1. Open **Settings → Apps → TextFromSMS**, or tap **App permission settings** in TextFromSMS.
2. On the app's main **App info** screen, open the **three-dot menu** at the top right.
3. Select **Allow restricted settings** and complete any identity confirmation on your phone.
4. Return to **Permissions → SMS** and choose **Allow**, or return to TextFromSMS and tap
   **Read conversations** to request SMS access again.

This is separate from allowing the browser to install APKs and from granting Contacts access.
It does not require uninstalling TextFromSMS. If that menu option is missing or SMS remains
unavailable, report the exact message to the project maintainer before reinstalling.
See [Android's restricted settings instructions](https://support.google.com/android/answer/12623953?hl=en).

## Display contact names

Contacts access is optional. To display saved names instead of phone numbers:

1. Tap **Use contact names (optional)** on the home screen or conversation list.
2. Allow Contacts access when Android asks.
3. Open a conversation to see the names in its message headers.

Saved names appear in the conversation list and incoming message headers when a matching contact
is available. Unmatched numbers remain as numbers. Your outgoing messages are labeled **You**.
You cannot customize that label in this version.

If you decline Contacts access, message reading and exporting still work with phone numbers.
Use **App permission settings** on the home screen to review or change permissions. After changing
a contact name or permission, return to the list and tap **Refresh**, then reopen the conversation.

## Choose and preview a conversation

The list shows conversations with the most recent messages first. Each entry includes:

- Contact names or phone numbers.
- The number of readable SMS and MMS messages.
- The date and time of its latest readable message.

Tap an entry to view its messages. The initial order is oldest first. Scroll to review the conversation.
Tap **Back to list** to choose another conversation. On the list, **Refresh** reads the available
conversations again, and **Home** returns to the starting screen.

### Search the conversation list

Use **Search name or phone number** above the list to find a conversation:

1. Type part of a contact's name or phone number. The list filters as you type.
2. Tap a matching conversation to open it.
3. Tap **Clear** beside the search box to show the full list again.

Names match regardless of capitalization or accents: for example, `jose` can match `José`.
Numbers match with or without spaces, parentheses, hyphens, or a leading plus sign, and you can
search just the last few digits. Phone numbers remain searchable when a saved contact name is
displayed. Group entries can match a displayed participant name or an available participant number.

Search filters conversation names and numbers, not message text, dates, or message counts. Hidden
conversations stay excluded unless **Show hidden conversations** is enabled. The search text stays
in place when you refresh, return from a preview, hide/restore an entry, or toggle Show hidden.
Tap Clear if you want to start a different search. Search text is not saved as an app preference.

### Change the message order

Tap the **sort-direction icon** to the right of **Conversation preview** to switch between
**Oldest first** (ascending date/time) and **Newest first** (descending date/time). The current
order appears beside the SMS/MMS counts. Each change returns the preview to the top, so in
Newest first mode the latest messages appear immediately.

The app remembers this choice for other conversations and after restarting. **Save .txt**,
**Share**, and **Print** use the displayed message order. To produce a chronological transcript,
select Oldest first before exporting. Changing order does not change any source messages.

The preview, saved text, and shared text use this format:

```text
Alex - 2026-10-15 09:00
Good morning.

You - 2026-10-15 09:05
Good morning! 😀
```

Timestamps use the phone's local time zone when the preview is generated. Multiline messages,
blank lines between messages, and Unicode text such as emoji are preserved. Long names or lines
may wrap to fit the screen in TextFromSMS, Word, or another viewer.

Pictures and other MMS media are represented by markers such as `[Attachment: image/jpeg]`.
The actual media files are not included. MMS subject headers, drafts, failed/outbox messages,
and MMS download notifications are not included in this version.

## Save a text file

1. Open the conversation and review its preview.
2. Tap **Save .txt**.
3. In Android's file picker, choose a folder or document location.
4. Keep the suggested filename or enter a different name ending in `.txt`.
5. Complete the save action in the picker.
6. Wait for **Text file saved.**

Open the file from your chosen location using a text viewer, Word, or another compatible app.
TextFromSMS does not automatically open it after saving. The file is plain UTF-8 text and contains
the same transcript as the preview, without an added title or message-count heading.

Cancelling the picker cancels that save. You can return to the preview and try again.

A saved file is a snapshot: it does not update when new messages arrive. To include newer
messages, tap **Refresh**, reopen the conversation, and save a new export.

## Share a conversation

1. Open the conversation and tap **Share**.
2. Choose a compatible app from Android's sharing menu, such as your email app.
3. Check that the conversation's `.txt` attachment is present.
4. Choose the recipient or destination and complete the action in that app.

You do not need to save a file first. Share prepares a text attachment directly from the preview.
TextFromSMS does not select a recipient or send the file automatically. You can dismiss the
sharing menu without sharing anything.

## Print or save as PDF

1. Open the conversation and tap **Print**.
2. Wait for Android's print preview to open.
3. For a paper copy, choose an available printer. To save a PDF, select **Preview mode**, open
   its **three-dot menu**, and choose **Save as PDF**. Some phones instead offer Save as PDF
   directly in the destination selector.
4. Review the pages and available print settings.
5. Complete the print or PDF save action in Android's screen.

Long conversations wrap across multiple pages. Printing uses a formatted document; **Save .txt**
and **Share** still produce plain text. Print-screen wording and available printers depend on
your phone's print service. You can back out of print preview to cancel.

Finish or cancel an existing print job before starting another one.

## Hide and restore conversations

Use hiding to keep unwanted conversations out of TextFromSMS's normal selection list. This is
a manual choice: the app cannot reliably identify Google Messages' deleted or blocked
conversations automatically.

### Hide an entry

1. In the conversation list, press and hold an entry.
2. Tap **Hide conversation** in its menu.

You can also open the conversation and tap **Hide conversation** in its preview.

### Show or restore a hidden entry

1. Enable **Show hidden conversations** above the list.
2. Hidden entries appear with a **[Hidden]** prefix. The number beside the toggle indicates how
   many currently available conversations you have hidden.
3. Press and hold a hidden entry and choose **Restore conversation**. Alternatively, open its
   preview and tap **Restore conversation**.
4. Turn off **Show hidden conversations** when you want to return to the normal filtered list.

With Show hidden enabled, the list includes both normal and hidden conversations. Hiding an
entry while this toggle is on leaves it visible with the [Hidden] marker. Hidden conversations
can still be opened and exported from this view.

The app remembers both your hidden choices and the toggle setting across restarts. If every
conversation is hidden, the toggle remains available so you can restore them. Hiding affects
only TextFromSMS's list: it does not delete, block, archive, or restore anything in Google
Messages. It is not a privacy lock.

## Privacy and stored files

- TextFromSMS reads messages and, if allowed, contact names. It does not send, edit, delete, or
  mark source messages read, and it does not modify contacts.
- The app has no Internet permission, advertising, analytics, or automatic uploads.
- Hidden choices are stored locally as conversation identifiers and a toggle setting. The app
  also stores your preferred message order. Clearing app data or uninstalling resets these choices.
- Saving and sharing create temporary text copies in the app's private cache. Copies older than
  24 hours are cleaned up on the next app start, except a copy awaiting completion of a save.
  Android may clear cached copies sooner.
- Files you save and copies received by other apps are separate from the temporary cache.
  Delete those copies yourself when you no longer need them. A cloud location or sharing app
  you choose may upload or synchronize the exported file.

## Troubleshooting

| What you see | What to try |
|---|---|
| Contacts can be allowed, but SMS is disabled or says Restricted setting | Follow **If Android restricts SMS permission after an APK download** above: **App info → three-dot menu → Allow restricted settings**, then grant SMS access. |
| SMS permission was not granted or messages cannot be read | Open **Home → App permission settings**, allow SMS access, and try **Read conversations** again. If Android refuses access, ask the project maintainer to check the installation. |
| Names appear as phone numbers | Allow Contacts access using **Use contact names (optional)** or **App permission settings**. Confirm the number is saved in Contacts, then refresh and reopen the conversation. |
| A conversation is missing from the list | Tap **Clear** beside the search box, turn on **Show hidden conversations**, and tap **Refresh**. A conversation containing only inaccessible messages may not appear. |
| Messages are missing from a preview or export | Compare with Google Messages. RCS and other messages Android does not expose may be unavailable; saving again cannot recover inaccessible messages. |
| A save fails or the export is no longer available | Reopen the conversation and try **Save .txt** again. Check free space and try another destination. A failed save may leave an incomplete file. |
| The saved file looks different in Word | Fonts and screen wrapping are controlled by the viewer. Compare the actual text, senders, and timestamps rather than line wrapping alone. |
| A sharing app is missing or cannot open the attachment | Choose another app that accepts `.txt` files, or save the file and attach it manually from that app. |
| Print preview will not open | Finish or cancel any existing job. Check that Android System WebView and a print service are available on the phone, then retry. |

For an important export, compare the first and last messages, several messages in the middle,
names, timestamps, and attachment markers with Google Messages before using the file as a record.
