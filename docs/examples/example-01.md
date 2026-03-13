# Example 1: Basic Plugin Usage

Learn how to use KillerTools plugins.

## List Plugins

```bash
killertools list-plugins
```

## Use Files Plugin

```bash
# Hash a file
killertools files hash /path/to/file

# Find duplicate files
killertools files find-duplicates /path/to/directory
```

## Use Crypto Plugin

```bash
# Generate UUID
killertools crypto uuid

# Hash text
killertools crypto hash "Hello, World!"
```

## Use DevTools Plugin

```bash
# Format JSON file
killertools devtools format-json file.json

# Test regex pattern
killertools devtools regex-test "\d+" "123abc456"
```

## Launch GUI

```bash
killertools gui
```

Then select a plugin from the sidebar.
