# Changelog — KillerTools

All notable changes to KillerTools will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.1.2] - 2026-03-12

### Added
- Comprehensive documentation structure in docs/
- ROADMAP.md for project milestones
- DEVELOPMENT_GOALS.md for technical goals
- SUPPORT.md for support information
- Expanded documentation with getting-started, quick-start, installation, usage, configuration, CLI, architecture, API, troubleshooting, and FAQ guides
- Improved plugin discovery to check for plugin instances first
- Enhanced CLI integration for TUI and GUI commands
- Modernized CI/CD release workflow with cross-platform binary builds

### Changed
- Updated documentation structure and organization
- Improved CI/CD workflows
- Enhanced .gitignore with comprehensive patterns
- Updated plugin discovery logic to prioritize plugin instances over classes

### Fixed
- Fixed CLI `tui()` and `gui()` commands to actually launch applications
- Fixed type annotations in GUI closeEvent handler
- Removed unused imports (QTimer, Path) from GUI module
- Removed print statements from devtools plugin in favor of silent parsing

### Removed
- Removed GITHUB_TOPICS.md (topics should be managed via GitHub UI)
- Removed MERGE_SUMMARY.md (temporary documentation)
- Removed unused simple_cli.py

## [0.1.1] - 2024-12-19

### Added
- Image Generator plugin with OpenAI DALL-E integration
- Git change tracking in devtools plugin
- Utilities directory with templates and scripts

### Changed
- Enhanced devtools plugin with git tracking functionality

## [0.1.0] - 2024-12-19

### Added
- **Core Architecture**: Plugin-based architecture with dynamic loading
- **Multiple Interfaces**: CLI, TUI, and GUI applications
- **Cross-Platform Support**: Windows, macOS, and Linux compatibility
- **Theme System**: System theme detection with manual switching
- **Settings Management**: Pydantic-based configuration with .env support
- **Rich Output**: Beautiful terminal output with Rich library
- **Icon System**: Custom SVG logo with multi-format export

### Core Features
- **Plugin Registry**: Dynamic plugin discovery and registration
- **Settings Persistence**: Configuration saved to ~/.killertools/config.json
- **Theme Detection**: Automatic system theme detection (Windows/macOS/Linux)
- **Logging System**: Rich console output with file logging
- **Type Safety**: Full type hints with mypy support
- **Code Quality**: Ruff, Black, isort, and pre-commit hooks

### Plugins
- **Files Plugin**: File hashing, duplicate detection, size formatting
- **Crypto Plugin**: Hash functions, UUID generation, Base64 encoding
- **DevTools Plugin**: Regex testing, README badge generation, JSON/YAML/TOML formatting

### User Experience
- **CLI Interface**: Rich command-line interface with Typer
- **TUI Interface**: Textual-based terminal user interface
- **GUI Interface**: PyQt6-based graphical interface
- **Theme Support**: Light, dark, and system theme modes
- **Cross-Platform**: Consistent experience across all platforms

### Technical Implementation
- **Poetry**: Modern Python dependency management
- **PyQt6**: Cross-platform GUI framework
- **Textual**: Modern terminal user interface
- **Typer**: Modern CLI framework with Rich integration
- **Pydantic**: Data validation and settings management
- **Rich**: Beautiful terminal output and progress bars

### Project Structure
- **Modular Design**: Clean separation of concerns
- **Plugin Architecture**: Easy to extend with new tools
- **Type Safety**: Full type hints throughout
- **Testing**: Comprehensive test suite with pytest
- **Documentation**: MkDocs Material with comprehensive guides
- **CI/CD**: GitHub Actions for testing and releases

---

[Unreleased]: https://github.com/VoxHash/KillerTools/compare/v0.1.2...HEAD
[0.1.2]: https://github.com/VoxHash/KillerTools/compare/v0.1.1...v0.1.2
[0.1.1]: https://github.com/VoxHash/KillerTools/compare/v0.1.0...v0.1.1
[0.1.0]: https://github.com/VoxHash/KillerTools/releases/tag/v0.1.0
