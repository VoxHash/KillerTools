# Contributing to KillerTools

Thanks for helping improve KillerTools!

## Code of Conduct
Please read and follow our [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

## Development Setup
```bash
# Clone
git clone https://github.com/VoxHash/KillerTools.git
cd KillerTools

# Install deps
poetry install
poetry install --with dev

# Set up pre-commit hooks
poetry run pre-commit install

# Run tests
poetry run pytest
```

## Branching & Commit Style
- Branches: `feature/…`, `fix/…`, `docs/…`, `chore/…`
- Conventional Commits: `feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `chore:`

## Code Quality
Before committing, run:
```bash
poetry run ruff check --fix killer_tools/ apps/ tests/
poetry run black killer_tools/ apps/ tests/
poetry run isort killer_tools/ apps/ tests/
poetry run mypy killer_tools/ apps/
```

## Pull Requests
- Link related issues, add tests, update docs
- Follow the PR template
- Keep diffs focused
- Ensure all tests pass

## Creating Plugins
See [docs/creating-plugins.md](docs/creating-plugins.md) for detailed plugin development guide.

## Release Process
- Semantic Versioning
- Update [CHANGELOG.md](CHANGELOG.md)

For more details, see the full [Contributing Guide](https://voxhash.github.io/KillerTools/contributing/).
