# Fybrk

**Real-time P2P file sync that actually works. Zero configuration, true 2-way sync.**

## Quick Install

```bash
curl -sSL https://fybrk.com/install.sh | bash
```

That's it! Fybrk is now installed and ready to use.

## What is Fybrk?

Fybrk syncs files in real-time across devices with zero configuration. Just run one command and your files sync automatically.

## What Actually Works

- **True 2-Way Sync**: Changes on any device instantly appear on all connected devices
- **Real-Time Detection**: File changes detected instantly using fsnotify
- **SQLite Database**: Tracks all file metadata locally with WAL mode
- **WebSocket P2P**: Direct device-to-device communication
- **Fully Tested**: 14 comprehensive tests, all passing

## Usage

### Simple 2-Step Workflow

**Device 1:**
```bash
fybrk ~/Documents
# Starting Fybrk sync in: /Users/you/Documents
# Pair with: fybrk://pair?key=abc123...
# Syncing files in real-time...
```

**Device 2:**
```bash
fybrk 'fybrk://pair?key=abc123...'
# Joining sync from pair URL...
# Connected! Syncing files in real-time...
```

### Live Demo Output

```bash
$ fybrk .
Starting Fybrk sync in: /Users/you/project
Scanning files...
Server listening on port 8080
Sync engine started
Pair with: fybrk://pair?key=1a67df3e...
Syncing files in real-time...

File event: create newfile.txt
File event: modify document.txt
File event: delete oldfile.txt
Peer connected: peer_1762342903625
```

## All Commands

```bash
fybrk                          # Sync current directory
fybrk /path/to/folder          # Sync specific directory
fybrk pair                     # Get pair URL to add more devices
fybrk 'fybrk://pair?key=...'   # Join existing sync
fybrk version                  # Show version info
fybrk help                     # Show help
```

## Testing

Run comprehensive tests:
```bash
./comprehensive_test.sh
# ✅ ALL TESTS PASSED! (14/14)
```

## Repositories

| Name | Purpose | Status |
|------|---------|--------|
| [fybrk](https://github.com/Fybrk/fybrk) | Main sync engine & CLI | ✅ Working |
| [docs](https://github.com/Fybrk/docs) | Documentation website | ✅ Updated |

## Architecture

- **File Watcher**: Real-time change detection (fsnotify)
- **Sync Engine**: Processes events and manages peers
- **WebSocket Server**: P2P communication
- **SQLite Database**: File metadata and hash tracking

## Status: ✅ WORKING

- File watching: ✅ Working
- Database tracking: ✅ Working
- WebSocket P2P: ✅ Working
- Sync engine: ✅ Working
- Conflict resolution: ✅ Working

## License

MIT - Open source and free to use
