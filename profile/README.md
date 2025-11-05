# Fybrk

**State-of-the-art P2P file sync with internet-wide connectivity and zero-trust security.**

## What is Fybrk?

Fybrk synchronizes files across your devices anywhere in the world without relying on centralized cloud providers. Your data stays encrypted with keys that never leave your devices.

## ✨ Key Features

- **🌐 Internet-Wide Sync**: Works across different networks, not just local
- **📱 QR Code Pairing**: Beautiful terminal QR codes for instant device pairing
- **🔒 Zero-Trust Security**: End-to-end encryption with no central servers
- **🚀 Production Quality**: Auto-reconnection, error handling, performance monitoring

## Get started quickly

```bash
curl -sSL https://fybrk.com/install.sh | bash
```

## Or build from source

```bash
git clone https://github.com/Fybrk/fybrk.git
cd fybrk
make build
```

## Usage

### Simple 3-Step Workflow

**Device A (has files):**

```bash
fybrk ~/Documents init    # Initialize folder for sync
fybrk ~/Documents pair    # Generate QR code for pairing
fybrk ~/Documents sync    # Start real-time sync
```

**Device B (wants to sync):**

```bash
fybrk pair-with '<QR-CODE-DATA>'  # Join from QR code (works over internet!)
fybrk ~/local/path sync           # Start syncing
```

### All Commands

```bash
fybrk <path> init         # Initialize directory for sync
fybrk <path> sync         # Start real-time synchronization (default)
fybrk <path> pair         # Generate QR code to pair with other devices
fybrk pair-with '<data>'  # Join sync network from QR code
fybrk <path> list         # List all tracked files and their status
```

## Repositories

| Name | Purpose | Status |
|------|---------|--------|
| [fybrk](https://github.com/Fybrk/fybrk) | Main sync engine & CLI | ✅ Production Ready |
| [docs](https://github.com/Fybrk/docs) | Documentation website | ✅ Live at fybrk.com |

## Security

- **AES-256-GCM encryption** with SHA-256 integrity
- **Local key management** - keys never leave your devices
- **Zero-trust architecture** - no data on external servers
- **Temporary rendezvous** - QR codes expire in 10 minutes
- **Real STUN protocol** for secure NAT traversal

## License

MIT - Open source and free to use
