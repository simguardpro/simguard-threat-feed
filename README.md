# SIMGUARD threat feed

Signed list of stalkerware package names and signing-certificate hashes.
The SIMGUARD Android app downloads it once a day and adds it to its built-in list.

- `stalkerware_feed.json` — the list
- `stalkerware_feed.json.sig` — ECDSA P-256 / SHA-256 signature (base64 DER) over the exact JSON bytes

The app rejects any file whose signature doesn't match, and any version that isn't newer than the one it has.
Edit only through `scripts/threat_feed/publish_feed.py` in the app repo.
