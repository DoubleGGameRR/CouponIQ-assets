# CouponIQ store icons

Public brand icons used by the CouponIQ app. Each store is matched by its exact Firestore store ID and reviewed website domain, never by a fuzzy name match.

`manifest.json` records the source URL, acquisition method, SHA-256, dimensions and review date. Files are original PNG/JPEG/WebP site icons, not AI-generated or recreated brand marks. Domain favicon cache sources are identified explicitly. Icons marked `small-favicon` have limited resolution and should be replaced with a better official asset when available; they are not claimed to be high-resolution brand artwork.

## Updates

1. Verify the store's official domain and icon visually. Do not use affiliate redirect domains or search engines as brand identity.
2. Add a new content-hashed file under `logos/`; retain old files for existing app versions.
3. Update the manifest and check image decoding, duplicate hashes and store IDs.
4. Commit and push, then build URLs pinned to that commit: `https://cdn.jsdelivr.net/gh/DoubleGGameRR/CouponIQ-assets@COMMIT/logos/FILE`.
5. Use the application's guarded sync script to update only `stores/{id}.logoUrl`. Do not upload service credentials, database backups or private customer data here.

The app caches icons locally on Android/iOS and can fall back to the same immutable GitHub raw file when the CDN is unavailable. Firestore contains only the URL, not image bytes. Updating these URLs does not remove normal Firestore document read charges. GitHub/CDN are external services without an availability guarantee for this app.

Brand names and logos belong to their respective owners. Inclusion identifies the corresponding store and does not imply endorsement. This repository does not grant trademark rights to third parties.
