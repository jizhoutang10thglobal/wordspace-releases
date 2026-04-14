# Wordspace Releases

Public download mirror for [wordspace](https://github.com/wl1390/projectx) — the AI-era document editor.

Source code lives in a private repository. This repository only hosts the compiled installers so anyone can download without needing GitHub access to the source.

## Latest Downloads

- **macOS (Apple Silicon)** — [wordspace-mac-arm64.dmg](https://github.com/jizhoutang10thglobal/wordspace-releases/releases/latest/download/wordspace-mac-arm64.dmg)
- **Windows** — [wordspace-windows-setup.exe](https://github.com/jizhoutang10thglobal/wordspace-releases/releases/latest/download/wordspace-windows-setup.exe)

The links above always point to the latest release. See [all releases](https://github.com/jizhoutang10thglobal/wordspace-releases/releases) for version history.

## First Launch Notes

Wordspace is **not yet code-signed** (code signing is on the roadmap but not yet funded). Your OS will block the first launch — this is a known macOS / Windows behavior for unsigned apps downloaded from the internet, **not** a problem with the app itself.

### macOS — "App is damaged and can't be opened"

Modern macOS (Ventura / Sonoma / Sequoia) shows a misleading "damaged, move to trash" message for unsigned apps that were downloaded via a browser. **The app isn't actually damaged** — macOS is just being strict with the `com.apple.quarantine` attribute that browsers set on downloads.

**Workaround** — after dragging Wordspace to Applications, run this once in Terminal:

```bash
xattr -cr /Applications/wordspace.app
```

Then launch normally (double-click). You only need to do this once per install; future launches work without any extra step.

If you prefer to clear quarantine on the `.dmg` itself **before** installing:

```bash
xattr -cr ~/Downloads/wordspace-mac-arm64.dmg
```

Then open the `.dmg` and drag as usual.

### Windows — "Windows protected your PC"

SmartScreen warns about apps from unknown publishers:

1. Run the `.exe`
2. Click **More info** → **Run anyway**
3. Follow the installer

## Support / Issues

Source code is private. Please contact the wordspace team for support.
