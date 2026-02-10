# Omnius Releases

Official releases for the **Omnius** streaming app.

## Downloads

Check the [Releases](https://github.com/OmniusRepos/omnius-releases/releases) page for the latest builds.

| Platform | Format | Architecture |
|----------|--------|-------------|
| macOS | `.dmg` | Apple Silicon (arm64), Intel (x64) |
| Linux | `.AppImage`, `.deb`, `.rpm` | x64 |
| Windows | `.msi` | x64 |
| Android TV | `.apk` | arm64 / universal |

## Install

### macOS
Download the `.dmg`, open it, and drag Omnius to Applications.

### Linux
**AppImage** (any distro):
```bash
chmod +x Omnius_*.AppImage
./Omnius_*.AppImage
```

**Debian/Ubuntu**:
```bash
sudo dpkg -i omnius_*.deb
```

### Windows
Download and run the `.msi` installer.

### Android TV
Sideload the `.apk` via ADB:
```bash
adb install -r omnius-*.apk
```

## Auto-Updates

The desktop app checks for updates automatically on launch. Updates are signed and verified before installation.

## Issues

Found a bug or have a feature request? [Open an issue](https://github.com/OmniusRepos/omnius-releases/issues).

## Server

Omnius apps connect to a self-hosted Omnius server. See [omnius.stream/server](https://omnius.stream/server) for deployment instructions.
