# Omnius Releases

Official releases for **Omnius** — self-hosted streaming server and client apps.

## Server

### Docker (Recommended)

```bash
docker run -d \
  --name omnius \
  -p 8080:8080 \
  -e LICENSE_KEY=YOUR_LICENSE_KEY \
  -e ADMIN_PASSWORD=your_secure_password \
  -v omnius-data:/app/data \
  ghcr.io/omniusrepos/omnius-server:latest
```

Multi-arch image supporting `linux/amd64` and `linux/arm64`.

| Tag | Description |
|-----|-------------|
| `latest` | Latest stable release |
| `1.1.0` | Pinned version |

### Binary

Download server binaries from the [Releases](https://github.com/OmniusRepos/omnius-releases/releases) page.

| Platform | File |
|----------|------|
| Linux x86_64 | `omnius-linux-amd64` |
| Linux ARM64 | `omnius-linux-arm64` |
| macOS ARM64 | `omnius-darwin-arm64` |

```bash
chmod +x omnius-linux-amd64
./omnius-linux-amd64
```

The server runs on port `8080` by default and stores data in `./data/`.

### Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `LICENSE_KEY` | — | License key from [omnius.stream](https://omnius.stream) |
| `ADMIN_PASSWORD` | — | Admin panel password |
| `PORT` | `8080` | Server port |

## Client Apps

### Downloads

Check the [Releases](https://github.com/OmniusRepos/omnius-releases/releases) page for the latest builds.

| Platform | Format | Architecture |
|----------|--------|-------------|
| macOS | `.dmg` | Apple Silicon (arm64), Intel (x64) |
| Linux | `.AppImage`, `.deb`, `.rpm` | x64 |
| Windows | `.msi` | x64 |
| Android TV | `.apk` | arm64 / universal |

### Install

**macOS** — Download the `.dmg`, open it, and drag Omnius to Applications.

**Linux AppImage** (any distro):
```bash
chmod +x Omnius_*.AppImage
./Omnius_*.AppImage
```

**Debian/Ubuntu**:
```bash
sudo dpkg -i omnius_*.deb
```

**Windows** — Download and run the `.msi` installer.

**Android TV** — Sideload via ADB:
```bash
adb install -r omnius-*.apk
```

### Auto-Updates

The desktop app checks for updates automatically on launch. Updates are signed and verified before installation.

The server checks for updates from Settings > Update. Docker deployments show a redeploy notice instead.

## Issues

Found a bug or have a feature request? [Open an issue](https://github.com/OmniusRepos/omnius-releases/issues).

## Links

- [omnius.stream](https://omnius.stream) — Get a license key
- [Docker Image](https://ghcr.io/omniusrepos/omnius-server) — Container registry
