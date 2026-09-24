# Notetaker updates

This repository holds the builds of Notetaker, a macOS menu bar app that transcribes and takes
notes of meetings on the Mac. The source is in a private repository.

- **Install:** download the newest `Notetaker-*.dmg` from
  [Releases](https://github.com/fskroes/notetaker-updates/releases), open it, and drag Notetaker
  to Applications. macOS 26 or later, Apple Silicon.
- **Updates:** after the first install, Notetaker updates itself. It reads `appcast.xml` in this
  repository once a day, downloads a new version in the background, and asks once to restart.
  It never restarts during a recording.

Every build is signed with a Developer ID, notarized by Apple, and signed again with the
Sparkle update key. The app refuses an update whose signature does not match its key.
`scripts/release.sh` in the source repository writes every file here. Do not edit
`appcast.xml` by hand.
