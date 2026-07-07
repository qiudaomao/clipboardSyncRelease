# Clipboard Sync Releases

Public release distribution for Clipboard Sync.

Home page: **[clipboardsync.fuzhuo.me](https://clipboardsync.fuzhuo.me)**

Found a bug or have a feature request? Please [open an issue](https://github.com/qiudaomao/clipboardSyncRelease/issues) on this repo.

This repo holds only:

- `appcast.xml` / `win-appcast.xml` — the Sparkle 2 / NetSparkle update feeds the apps poll.
- GitHub Releases with the signed, zipped/installer app builds.

## What is Clipboard Sync?

A native menubar/tray app for macOS and Windows that syncs your clipboard over the LAN via WebSocket. No cloud, no account — your devices talk directly to each other.

Key features:

1. Clipboard sync over LAN
2. Automatic text/image sync
3. Click to sync files
4. Clipboard history (last 10 items)
5. Password-based encryption (AES-GCM)
6. Mouse and keyboard sharing across devices

## Getting Started

1. Download the app for your platform from [clipboardsync.fuzhuo.me](https://clipboardsync.fuzhuo.me) (or from this repo's [Releases](https://github.com/qiudaomao/clipboardSyncRelease/releases)):
   - macOS: `clipboardSyncMac.zip`
   - Windows: `clipboardSyncWin-Setup.exe` (requires the .NET 8 Desktop Runtime x64; the installer will prompt if it's missing)
2. Install and launch the app on both machines you want to sync. It runs from the menu bar (macOS) or system tray (Windows).
3. On one machine, set the mode to **Server**. Its settings window/config form will show a LAN address like `ws://192.168.1.20:8787/` — note the host and port.
4. On the other machine, set the mode to **Client** and enter that server's LAN host and port. `127.0.0.1`/`localhost` are rejected for client mode — you must use the server's real LAN IP.
5. Set the **same sync password** on every device before starting. All clipboard and input-sharing traffic is encrypted with that password.

Once connected:

- Copying text or an image on one machine automatically syncs it to the other.
- To send files, copy them in Finder/Explorer, then choose **Send Files from Clipboard** from the menu/tray. Files are capped at 10 MB each.
- The **History** submenu keeps the last 10 clipboard items and lets you restore/resend any of them.

### Mouse & keyboard sharing (optional)

Input Sharing is off by default:

1. Enable it from Settings/Configure or the menu/tray.
2. Choose a direction: `Server -> Client` or `Client -> Server`.
3. Open **Screen Layout...** and drag each machine's screen rectangle to match how they physically sit relative to each other, so the cursor crosses over naturally.
4. On macOS, grant Accessibility/Input Monitoring permission when prompted — it's required for keyboard and mouse sharing to work.

## Auto-updates

Both apps check for updates automatically:

- macOS uses Sparkle 2 against `appcast.xml` in this repo.
- Windows uses NetSparkle against `win-appcast.xml` in this repo.

## Links

- Home page: https://clipboardsync.fuzhuo.me
- Issues / feature requests: https://github.com/qiudaomao/clipboardSyncRelease/issues
