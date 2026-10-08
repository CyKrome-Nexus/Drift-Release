# Drift — Releases

Official distribution repository for **Drift**, live wallpapers for your desktop, from
CyKrome Nexus.

This repository hosts released binaries only. It contains no source code.

## Install

macOS and Linux can install from the terminal:

```bash
curl -fsSL https://github.com/CyKrome-Nexus/Drift-Release/releases/latest/download/install.sh | bash
```

Platform-specific installers are also attached to every release:

```bash
curl -fsSL https://github.com/CyKrome-Nexus/Drift-Release/releases/latest/download/install-mac.sh | bash
curl -fsSL https://github.com/CyKrome-Nexus/Drift-Release/releases/latest/download/install-linux.sh | bash
```

The macOS installer extracts the `.app.tar.gz` into `/Applications` and removes
Gatekeeper quarantine attributes. The Linux installer installs the AppImage under
`~/.local/share/Drift`, creates a desktop entry, and links `drift` into `~/.local/bin`.

## Download

Grab the latest build from the [**Releases**](../../releases/latest) page.

| Platform | File |
| --- | --- |
| macOS (Apple Silicon) | `Drift_<version>_aarch64.dmg` or `Drift_aarch64.app.tar.gz` |
| macOS (Intel) | `Drift_<version>_x64.dmg` or `Drift_x86_64.app.tar.gz` |
| Windows | `Drift_<version>_x64_en-US.msi` or `Drift_<version>_x64-setup.exe` |
| Linux | `Drift_<version>_amd64.AppImage`, `Drift_<version>_amd64.deb`, or `Drift-<version>-1.x86_64.rpm` |

Live wallpapers currently play on **macOS**. The Windows and Linux builds run the full
app; their wallpaper engines are on the way.

The phone apps ship through the App Store and Google Play, not from here.

## Updates

Drift updates itself. It checks this repository shortly after launch and offers the
update in-app when there is one. You can also check from *Settings → About → Check for
updates*.

Every update is cryptographically signed, and Drift verifies that signature before
installing anything. An update that has been tampered with in transit is rejected.

In-app updating covers the macOS app, the Windows installers and the Linux `.AppImage`.
The `.deb` and `.rpm` packages are owned by your system package manager, so those
installs do not self-update.

`latest.json` on each release is the update feed. It is metadata, not a download.

## First launch

Builds are not code-signed or notarised yet, so macOS and Windows will show an
"unidentified developer" / SmartScreen warning on first launch. (This is separate from
update signing above, which is always on.)

- **macOS:** right-click the app → *Open* → *Open*.
- **Windows:** *More info* → *Run anyway*.
