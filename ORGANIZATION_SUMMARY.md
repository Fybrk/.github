# Fybrk Organization

## Overview

Fybrk is a file synchronization system that operates without centralized cloud storage. Files are encrypted locally and synchronized peer-to-peer between your devices.

## Repository Structure

| Repository | Description | Status |
|------------|-------------|---------|
| [core](https://github.com/Fybrk/core) | Sync engine library | Complete |
| [cli](https://github.com/Fybrk/cli) | Command line interface | Complete |
| [docs](https://github.com/Fybrk/docs) | Documentation website | Complete - Live at docs.fybrk.com |
| [desktop](https://github.com/Fybrk/desktop) | Desktop application | In development |
| [plugins](https://github.com/Fybrk/plugins) | Third-party integrations | In development |
| [examples](https://github.com/Fybrk/examples) | Integration examples | In development |

## Current Implementation

The core library and CLI tool are functional. They provide:

- File chunking with SHA-256 hashing
- AES-256-GCM encryption
- SQLite metadata storage
- File system monitoring
- Basic synchronization logic

## Architecture

```
Desktop/CLI Applications
         ↓
    Core Library
         ↓
Storage + Sync + Watcher
```

## Development Status

**Complete:**
- Core synchronization engine
- File encryption and chunking
- Command line interface
- Documentation website with visual design
- Test suite (80%+ coverage)

**In Progress:**
- Multi-device networking
- Conflict resolution
- Desktop GUI

## Technical Details

- **Language:** Go 1.21+
- **Database:** SQLite
- **Encryption:** AES-256-GCM
- **Hashing:** SHA-256
- **Testing:** Comprehensive unit tests

## Getting Started

```bash
git clone https://github.com/Fybrk/cli.git
cd cli
make build
./bin/fybrk -path /your/directory -cmd sync
```

## Contributing

Each repository has its own contribution guidelines. Start with the core library for fundamental changes or the CLI for user interface improvements.
