# Troubleshooting

Common issues and solutions.

## Installation Issues

### Module Not Found
**Problem**: `ModuleNotFoundError` when running commands.

**Solution**: Ensure all dependencies are installed:
```bash
pip install --upgrade killertools
# or
poetry install
```

### Permission Denied
**Problem**: Permission errors on installation.

**Solution**: Use `pipx` or virtual environment:
```bash
pipx install killertools
```

## Runtime Issues

### Plugin Not Found
**Problem**: Plugin not discovered.

**Solution**: 
- Check plugin is in `killer_tools/plugins/`
- Verify plugin has `plugin` instance
- Run `killertools list-plugins` to verify

### GUI Not Launching
**Problem**: GUI fails to start.

**Solution**:
- Check PyQt6 is installed: `pip install PyQt6`
- Verify display configuration (Linux)
- Check system requirements

### Theme Not Applying
**Problem**: Theme not working correctly.

**Solution**:
- Check `~/.killertools/config.json`
- Verify theme mode setting
- Try manual theme selection

## Configuration Issues

### Settings Not Saving
**Problem**: Settings not persisting.

**Solution**:
- Check `~/.killertools/` directory permissions
- Verify JSON syntax in config file
- Check disk space

## Getting More Help

- [FAQ](faq.md)
- [GitHub Issues](https://github.com/VoxHash/KillerTools/issues)
- [Support](https://github.com/VoxHash/KillerTools/discussions)
