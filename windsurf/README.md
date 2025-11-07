# Windsurf Configuration

This directory contains Windsurf editor configuration files.

## Files

- **settings.json** - Editor settings and preferences
- **keybindings.json** - Custom keyboard shortcuts
- **extensions.txt** - List of installed extensions
- **README.md** - This file

## Installation

The installation script will automatically create symlinks:

- `~/.dotfiles/windsurf/settings.json` → `~/Library/Application Support/Windsurf/User/settings.json`
- `~/.dotfiles/windsurf/keybindings.json` → `~/Library/Application Support/Windsurf/User/keybindings.json`

## Updating Configuration

To update the configuration in this repository with your current Windsurf settings:

```bash
cp ~/Library/Application\ Support/Windsurf/User/settings.json ~/.dotfiles/windsurf/settings.json
cp ~/Library/Application\ Support/Windsurf/User/keybindings.json ~/.dotfiles/windsurf/keybindings.json
```

## Extensions

To export your current extensions list:

```bash
windsurf --list-extensions > ~/.dotfiles/windsurf/extensions.txt
```

To install all extensions from the list:

```bash
cat ~/.dotfiles/windsurf/extensions.txt | xargs -L 1 windsurf --install-extension
```

> **Note:** The `windsurf` CLI is located at `~/.codeium/windsurf/bin/windsurf`
