# Quick Start

Get KillerTools up and running in minutes.

## Installation

```bash
# Using pipx (recommended)
pipx install killertools

# Or using pip
pip install killertools
```

## Basic Usage

```bash
# Show help
killertools --help

# List plugins
killertools list-plugins

# Run a plugin
killertools files --help
killertools crypto --help
```

## Launch Interfaces

```bash
# Terminal UI
killertools tui

# Graphical UI
killertools gui
```

## Example: File Hashing

```bash
# Use the files plugin to hash a file
killertools files hash /path/to/file
```

## Example: Generate UUID

```bash
# Use the crypto plugin
killertools crypto uuid
```

## Configuration

Configuration is stored in `~/.killertools/config.json`. See [Configuration Guide](configuration.md) for details.

## Next Steps

- [Getting Started Guide](getting-started.md)
- [Usage Guide](usage.md)
- [Examples](examples/)
