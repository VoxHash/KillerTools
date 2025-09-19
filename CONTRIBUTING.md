# 🤝 Contributing to KillerTools

Thank you for your interest in contributing to KillerTools! We're excited to work with the community to make KillerTools even better! 🛠️✨

## 🎯 How to Contribute

### 🐛 Bug Reports
Found a bug? Help us fix it!
1. Check if the issue already exists
2. Use our [bug report template](.github/ISSUE_TEMPLATE/bug_report.md)
3. Provide detailed information about the bug
4. Include steps to reproduce
5. Specify your platform and KillerTools version

### ✨ Feature Requests
Have an idea for KillerTools? We'd love to hear it!
1. Check if the feature is already requested
2. Use our [feature request template](.github/ISSUE_TEMPLATE/feature_request.md)
3. Describe the feature clearly
4. Explain the use case and benefits
5. Consider if it fits KillerTools' plugin architecture

### 💻 Code Contributions
Want to contribute code? Awesome! Here's how:

#### 🚀 Getting Started
1. **Fork the repository**
2. **Clone your fork**
   ```bash
   git clone https://github.com/your-username/KillerTools.git
   cd KillerTools
   ```

3. **Set up the development environment**:
   ```bash
   # Install dependencies
   poetry install
   
   # Install development dependencies
   poetry install --with dev
   
   # Set up pre-commit hooks
   poetry run pre-commit install
   ```

4. **Create a new branch** for your feature:
   ```bash
   git checkout -b feature/amazing-feature
   ```

## 📝 Development Guidelines

### 🎨 Code Style

We use several tools to maintain code quality:

- **Ruff**: For linting and formatting
- **Black**: For code formatting
- **isort**: For import sorting
- **mypy**: For type checking

Run these before committing:
```bash
poetry run ruff check --fix killer_tools/ apps/ tests/
poetry run black killer_tools/ apps/ tests/
poetry run isort killer_tools/ apps/ tests/
poetry run mypy killer_tools/ apps/
```

### 🧪 Testing

- Write tests for new features
- Ensure all tests pass: `poetry run pytest`
- Aim for high test coverage
- Use descriptive test names
- Test across all interfaces (CLI, TUI, GUI)

### 📚 Documentation

- Update documentation for new features
- Add docstrings to all public functions
- Update README.md if needed
- Add type hints to all functions
- Update plugin documentation

## 🔌 Creating Plugins

### Plugin Structure

Create a new plugin in `killer_tools/plugins/your_plugin/`:

```
killer_tools/plugins/your_plugin/
├── __init__.py
├── plugin.py
└── tests/
    └── test_plugin.py
```

### Plugin Implementation

```python
from killer_tools.core.plugin import Plugin
from rich.console import Console
from typing import Any, Optional
from PyQt6.QtWidgets import QWidget
from textual.app import App

class YourPlugin(Plugin):
    name = "your_plugin"
    summary = "Description of your plugin"
    version = "1.0.0"

    def run_cli(self, console: Console, **kwargs: Any) -> None:
        """Run the plugin in CLI mode."""
        console.print("Your plugin CLI implementation")

    def tui_view(self) -> Optional[App]:
        """Return a Textual app for TUI mode."""
        return None

    def gui_widget(self) -> Optional[QWidget]:
        """Return a PyQt6 widget for GUI mode."""
        return None

# Create plugin instance
plugin = YourPlugin()
```

### Plugin Registration

Add your plugin to the `__init__.py` file:

```python
from killer_tools.plugins.your_plugin.plugin import YourPlugin

__all__ = ["YourPlugin"]
```

## 🎯 Contribution Areas

### 🔧 Core Development
- Plugin system improvements
- Interface enhancements (CLI, TUI, GUI)
- Performance optimizations
- Bug fixes
- Code refactoring

### 🎨 User Interface
- UI/UX improvements
- Theme enhancements
- Accessibility features
- Responsive design
- Visual improvements

### 🔌 Plugin Development
- New plugin creation
- Plugin API improvements
- Plugin testing
- Plugin documentation
- Plugin examples

### 🛠️ Developer Tools
- Build system improvements
- Testing enhancements
- Documentation updates
- CI/CD improvements
- Development tools

### 🌍 Cross-Platform
- Platform-specific features
- Build system improvements
- Package management
- Distribution
- Platform testing

## 🐛 Bug Reports

When reporting bugs, please include:

1. **Clear description** of the issue
2. **Steps to reproduce** the problem
3. **Expected behavior** vs actual behavior
4. **Environment details** (OS, Python version, etc.)
5. **Error messages** or logs if applicable

## 💡 Feature Requests

When suggesting features:

1. **Check existing issues** first
2. **Describe the use case** clearly
3. **Explain the benefits** to users
4. **Consider implementation** complexity

## 📋 Pull Request Process

1. **Ensure your code** follows our style guidelines
2. **Add tests** for new functionality
3. **Update documentation** as needed
4. **Run all checks** locally before submitting
5. **Write a clear description** of your changes
6. **Link to related issues** if applicable

### PR Checklist

- [ ] Code follows style guidelines
- [ ] Tests pass locally
- [ ] Documentation updated
- [ ] Type hints added
- [ ] No breaking changes (or documented)
- [ ] Changelog updated (if needed)

## 🏷️ Release Process

Releases are handled automatically via GitHub Actions when tags are pushed:

```bash
# Create and push a new tag
git tag -a v1.0.0 -m "Release v1.0.0"
git push origin v1.0.0
```

## 🧪 Testing Guidelines

### 🔍 Unit Tests
```bash
poetry run pytest
```

### 🎯 Plugin Tests
```bash
# Test specific plugin
poetry run pytest tests/test_plugins.py::test_files_plugin

# Test all plugins
poetry run pytest tests/test_plugins.py
```

### 🖥️ Interface Tests
```bash
# Test CLI
poetry run killertools --help

# Test TUI (when implemented)
poetry run killertools tui

# Test GUI (when implemented)
poetry run killertools gui
```

### 🏗️ Build Tests
```bash
# Test build process
make build

# Test on Windows
.\build.ps1
```

## 📝 Commit Convention

We use [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes
- `refactor`: Code refactoring
- `test`: Test additions/changes
- `chore`: Build process or auxiliary tool changes

### Examples:
```
feat(plugin): add new crypto plugin
fix(cli): resolve typer compatibility issue
docs: update README with new features
style: format code with black
refactor(ui): improve theme system
test: add plugin tests
chore: update build scripts
```

## 🎨 KillerTools Design Guidelines

When contributing to KillerTools' design or features:

### ✅ Do:
- Maintain plugin architecture philosophy
- Keep interfaces clean and intuitive
- Focus on functionality over decoration
- Ensure cross-platform compatibility
- Keep performance as priority
- Follow the existing code style

### ❌ Don't:
- Break the plugin system
- Add unnecessary complexity
- Remove essential functionality
- Ignore platform standards
- Compromise performance
- Break existing interfaces

## 🚀 Release Process

### 📅 Release Schedule
- **Patch releases**: As needed for bug fixes
- **Minor releases**: Monthly for new features
- **Major releases**: Quarterly for significant changes

### 🏷️ Versioning
We use [Semantic Versioning](https://semver.org/):
- `MAJOR.MINOR.PATCH`
- Example: `0.1.0` → `0.1.1` → `0.2.0`

## 🎉 Recognition

### 🌟 Contributors
- Contributors will be listed in the README
- Special recognition for significant contributions
- KillerTools will thank you! 🛠️✨

### 🏆 Contribution Levels
- **Bronze**: 1-5 contributions
- **Silver**: 6-15 contributions  
- **Gold**: 16-30 contributions
- **Platinum**: 31+ contributions

## 📞 Getting Help

### 💬 Community
- **GitHub Issues**: Ask questions and share ideas
- **Discussions**: Report bugs and request features
- **Pull Requests**: Submit code contributions

### 📚 Resources
- [README](README.md) - Project overview
- [Changelog](CHANGELOG.md) - Version history
- [Documentation](docs/) - Complete guides
- [Plugin API](docs/plugin-api.md) - Plugin development

## 📋 Checklist for Contributors

Before submitting a PR, make sure:

- [ ] Code follows the style guidelines
- [ ] Tests pass locally
- [ ] Documentation is updated
- [ ] Changes are tested across all interfaces
- [ ] Plugin functionality is verified
- [ ] Cross-platform compatibility is maintained
- [ ] Commit messages follow the convention
- [ ] PR description is clear and detailed
- [ ] Related issues are linked
- [ ] KillerTools' design philosophy is maintained

## 🎯 Quick Start for New Contributors

1. **Read the documentation**
2. **Set up the development environment**
3. **Look for "good first issue" labels**
4. **Start with small contributions**
5. **Ask questions if you need help**
6. **Have fun contributing!**

## 🛠️ KillerTools Philosophy

KillerTools is designed with these core principles:

- **Plugin-First**: Everything is a plugin, easy to extend
- **Cross-Platform**: Consistent experience across all platforms
- **Professional**: High-quality implementation and user experience
- **Efficient**: Fast, responsive, and resource-efficient
- **Integrated**: Seamless integration with developer workflows
- **Reliable**: Stable, consistent, and dependable
- **User-Friendly**: Intuitive and easy to use

When contributing, please keep these principles in mind and help us maintain KillerTools' high standards!

---

## 🤖 A Message from the KillerTools Team

"Hey there, future contributor! We're super excited that you want to help make KillerTools even better! Whether you're fixing bugs, adding features, or improving the user experience, every contribution helps us create the best developer toolkit possible.

Don't be afraid to ask questions - we're here to help! And remember, coding is like magic... but with more debugging!

Let's build something amazing together! ✨"

---

**Made with ❤️ by VoxHash and the amazing community**

*KillerTools is ready to work with you!* 🛠️✨
