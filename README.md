# Clipboard Sync Releases

Public release distribution for [Clipboard Sync](https://github.com/qiudaomao/clipboardSync) (closed-source app repo).

This repo holds only:

- `appcast.xml` — the Sparkle 2 update feed the macOS app polls (`SUFeedURL` in the app's `Info.plist` points at `raw.githubusercontent.com/qiudaomao/clipboardSyncRelease/main/appcast.xml`).
- GitHub Releases with the signed, zipped app builds.

It's kept public and separate from the source repo because Sparkle's default update feed fetch is unauthenticated and needs a public URL, without exposing the private source.

See `release_update.md` in the source repo for the full per-release procedure.
