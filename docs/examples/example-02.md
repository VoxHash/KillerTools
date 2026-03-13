# Example 2: Advanced Usage

Advanced examples and use cases.

## Batch Operations

```bash
# Find and remove duplicate files
killertools files find-duplicates /path/to/directory

# Bulk rename files
killertools files bulk-rename "old" "new"
```

## Crypto Operations

```bash
# Generate HMAC
killertools crypto hmac "message" "secret" "sha256"

# Base64 encode/decode
killertools crypto base64-encode "Hello, World!"
killertools crypto base64-decode "SGVsbG8sIFdvcmxkIQ=="
```

## DevTools Operations

```bash
# Format multiple files
killertools devtools format-json file1.json file2.json

# Validate JSON
killertools devtools validate-json file.json
```

## Configuration

Edit `~/.killertools/config.json`:

```json
{
  "theme": {
    "mode": "dark",
    "accent_color": "#7C3AED"
  },
  "ui": {
    "window_width": 1400,
    "window_height": 900
  }
}
```
