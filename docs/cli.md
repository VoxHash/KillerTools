# CLI Reference

Complete command-line interface reference for KillerTools.

## Global Commands

### `killertools --help`
Show help message.

### `killertools list-plugins`
List all available plugins.

### `killertools tui`
Launch the Terminal User Interface.

### `killertools gui`
Launch the Graphical User Interface.

### `killertools version`
Show version information.

## Plugin Commands

### Files Plugin
```bash
killertools files hash <file>
killertools files find-duplicates <directory>
killertools files bulk-rename <pattern> <replacement>
```

### Crypto Plugin
```bash
killertools crypto hash <text> [--algorithm ALGORITHM]
killertools crypto uuid
killertools crypto ulid
killertools crypto base64-encode <text>
killertools crypto base64-decode <text>
```

### DevTools Plugin
```bash
killertools devtools format-json <file>
killertools devtools format-yaml <file>
killertools devtools format-toml <file>
killertools devtools regex-test <pattern> <text>
```

## Options

### Global Options
- `--verbose` - Enable verbose logging
- `--theme <mode>` - Set theme mode (system/light/dark)

## See Also

- [Usage Guide](usage.md)
- [Examples](examples/)
