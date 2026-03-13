# Usage Guide

Learn how to use KillerTools effectively.

## Command Structure

```bash
killertools [command] [options]
```

## Commands

### List Plugins
```bash
killertools list-plugins
```

### Launch Interfaces
```bash
killertools tui   # Terminal UI
killertools gui   # Graphical UI
```

### Plugin Commands
Each plugin has its own commands. Use `--help` to see available options:

```bash
killertools files --help
killertools crypto --help
killertools devtools --help
```

## Examples

### Files Plugin
```bash
# Hash a file
killertools files hash /path/to/file

# Find duplicates
killertools files find-duplicates /path/to/directory
```

### Crypto Plugin
```bash
# Generate UUID
killertools crypto uuid

# Hash text
killertools crypto hash "your text here"
```

### DevTools Plugin
```bash
# Format JSON
killertools devtools format-json file.json

# Test regex
killertools devtools regex-test "\d+" "123abc"
```

## Configuration

See [Configuration Guide](configuration.md) for details.

## Advanced Usage

- [CLI Reference](cli.md)
- [Examples](examples/)
- [Architecture](architecture.md)
