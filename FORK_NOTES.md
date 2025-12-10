# Fourteen Fork - Changes and Safety Notes

## Package Rename

This is a fork of `prompt-toolkit-action-completer` renamed to `fourteen-prompt-toolkit-action-completer` to safely publish without conflicting with the original package.

## Installation

```bash
pip install fourteen-prompt-toolkit-action-completer
# or
uv add fourteen-prompt-toolkit-action-completer
```

## Changes from Original

### New Features
- **Dynamic Attribute Chaining**: You can now chain decorators like `@completer.hello.world.action("ping")` without explicitly calling `.group()` for each level
- Support for `Empty` parameter type for help-only completions

### Improvements
- Enhanced `__getattr__` on `ActionGroup` and `ActionCompleter` for ergonomic decorator chaining
- Better support for sharing action groups across modules

## Publishing to PyPI

This repository includes a GitHub Actions workflow for publishing to PyPI:

1. **Set up PyPI trusted publishing**:
   - Go to https://pypi.org/manage/account/publishing/
   - Add a new publisher for GitHub Actions
   - Owner: `Fourteen-IP`
   - Repository: `prompt-toolkit-action-completer`
   - Workflow: `publish.yml`

2. **Publish via GitHub Actions**:
   - Go to Actions tab → "Publish to PyPI" → "Run workflow"
   - Optionally specify a version number (otherwise uses version from `pyproject.toml`)
   - The workflow will build and publish to PyPI using trusted publishing

## Original Project

Original project by Stephen Bunn: https://github.com/stephen-bunn/prompt-toolkit-action-completer

## License

ISC License (same as original)
