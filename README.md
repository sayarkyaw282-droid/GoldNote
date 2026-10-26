# GoldNote Android PWA prototype

## What works in this prototype
- Create, edit, delete and search notes
- Categories: Personal, Business, Learning, Important
- Sort notes and add checklist tasks
- Speech-to-text where the browser supports Web Speech API (may require internet; offline transcription is device/browser dependent)
- Offline audio recording saved locally in IndexedDB, with playback, download, and delete controls
- JSON backup export and restore/import
- Optional PIN screen lock
- Black & gold responsive layout and basic PWA service-worker shell

## Important limitations
- Notes are stored in this browser/device's localStorage. Clearing site data can delete them.
- PIN lock is a simple screen lock, NOT encryption. Do not use it for sensitive client/medical records or passwords.
- Backup/restore is manual. Cloud sync is NOT implemented.
- Speech recognition depends on browser support, microphone permission, language availability, and often internet access. Offline speech-to-text is NOT guaranteed.
- Audio recordings are saved locally in this browser/device using IndexedDB and can play offline after they are saved. Clearing browser/site data can delete recordings. Audio files are not included in the JSON note backup yet; download important recordings separately.
- For Android installation as a PWA, host this folder on an HTTPS website, open it in Chrome, then choose "Install app" / "Add to Home screen". Opening the HTML directly as a file does not provide full PWA installation/offline support.

## Files
- index.html: app UI and logic
- manifest.webmanifest: PWA metadata
- sw.js: basic offline shell caching
