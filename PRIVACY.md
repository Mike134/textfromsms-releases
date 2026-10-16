# Privacy

TextFromSMS processes messages locally on your Android phone.

- SMS read permission is required for SMS/MMS exposed by Android. Contacts read permission is
  optional and resolves names locally. The app does not modify messages or contacts.
- The APK has no Internet permission, advertising, analytics, telemetry, account, or server upload.
- Local preferences contain hidden conversation identifiers, the Show hidden toggle, and message
  sort order. Search text is retained in the active screen/session rather than a saved preference.
- Exporting stages a text snapshot in private app cache. Old exports are removed on the next app
  start after 24 hours, except an export awaiting completion of Save. Android can clear cache sooner.
- Save writes to the location you select. Share grants temporary read access to the chosen export.
  Print gives the transcript to Android's print service. Your chosen cloud provider, sharing app,
  printer service, or PDF destination may store or upload its copy under its own policies.
- You manage saved files and copies held by other apps. Clearing TextFromSMS data or uninstalling
  removes its local preferences/cache; it does not erase exported copies elsewhere.
- The About download link opens your browser, which accesses GitHub under its own privacy policies.
- Bug reports you submit on GitHub are separate from the app. Once this repository is public,
  public issues and attachments are visible to anyone. Do not include private conversations.

RCS completeness is unverified. TextFromSMS is not a guarantee of complete message archival.
