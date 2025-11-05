# Fybrk

Distributed personal cloud with end-to-end encryption.

## What is Fybrk?

Fybrk synchronizes files across your devices without relying on centralized cloud providers. Your data stays encrypted with keys that never leave your devices.

## Installation

```bash
git clone https://github.com/Fybrk/fybrk.git
cd fybrk
make build
```

## Usage

```bash
# Sync a directory
./bin/fybrk -path /path/to/sync -cmd sync

# Scan for changes
./bin/fybrk -path /path/to/sync -cmd scan

# List tracked files
./bin/fybrk -path /path/to/sync -cmd list
```

## Repositories

| Name | Purpose | Status |
|------|---------|--------|
| [fybrk](https://github.com/Fybrk/fybrk) | Sync engine & CLI tool | Complete |
| [docs](https://github.com/Fybrk/docs) | Documentation website | Complete - Live |
| [apps](https://github.com/Fybrk/apps) | Applications | In-progress |
| [plugins](https://github.com/Fybrk/plugins) | Third-party integrations | Planned |
| [examples](https://github.com/Fybrk/examples) | Code samples | Planned |

## Security

- AES-256-GCM encryption
- SHA-256 file integrity
- Local key management
- No telemetry

## License

MIT
