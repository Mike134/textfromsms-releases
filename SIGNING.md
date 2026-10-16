# Official APK signing

Official release certificate SHA-256:

```text
5a156b4dfdfa3dd99d6f8a76033e685ac17eb419b737a6585a653a249a3a47cb
```

Public certificate: [textfromsms-release.pem](signing/textfromsms-release.pem).
Package name: `com.mike134.textfromsms`.

With Android SDK Build Tools installed, run:

```text
apksigner verify --verbose --print-certs TextFromSMS-1.0.0.apk
```

Verify that the signature is valid and the signer certificate SHA-256 equals the value above.
Release assets include SHA256SUMS with file checksums. For example, in PowerShell:

```powershell
Get-FileHash .\TextFromSMS-1.0.0.apk -Algorithm SHA256
```

Compare the result to SHA256SUMS obtained from the official release page. A checksum alone is
not proof of origin if both it and the APK came from an untrusted location.

The APK is non-debuggable and signed with the dedicated release key, also used for 1.0.0-rc1.
It includes Android v3 proof of signing-key rotation from the private prototypes. Updating a
prototype to the signed candidate was confirmed working on Android 16. If an update reports a
conflict, report it before uninstalling. Prototype certificate SHA-256, for identifying that
upgrade path only:

```text
f5d116447e904a599747ac60911062631a6a3d48d5ebbcccc6b92a9401b244ab
```

The release key is kept outside GitHub. Public certificate files contain no private key.
