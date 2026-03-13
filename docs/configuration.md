# Configuration

Configure KillerTools to your preferences.

## Configuration File

Configuration is stored in `~/.killertools/config.json`.

## Settings

### Theme
```json
{
  "theme": {
    "mode": "system",
    "accent_color": "#7C3AED",
    "font_family": "system"
  }
}
```

**Theme modes:**
- `system` - Automatically detect OS theme
- `light` - Force light theme
- `dark` - Force dark theme

### UI Settings
```json
{
  "ui": {
    "window_width": 1200,
    "window_height": 800,
    "sidebar_width": 250,
    "show_tooltips": true,
    "animations": true
  }
}
```

### Logging
```json
{
  "logging": {
    "level": "INFO",
    "file_logging": true,
    "max_file_size": 10,
    "backup_count": 5
  }
}
```

## Environment Variables

- `KILLERTOOLS_THEME_MODE` - Override theme mode
- `OPENAI_API_KEY` - For AI/image plugins
- `KILLERTOOLS_LOG_LEVEL` - Override log level

## Plugin Settings

Plugin-specific settings are stored in `plugin_settings`:

```json
{
  "plugin_settings": {
    "files": {
      "default_hash": "sha256"
    }
  }
}
```

## See Also

- [Usage Guide](usage.md)
- [CLI Reference](cli.md)
