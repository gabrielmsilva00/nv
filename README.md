# nv - Enhanced File Navigation for the Terminal

`nv` is a smart wrapper for [lsd](https://github.com/lsd-rs/lsd) and `cd` that provides a cleaner, more structured view of your directories. It automatically balances the density of information displayed by capping sub-entries based on the contents of the current folder, ensuring you get a quick overview without being overwhelmed.

## Features

- **Smart Tree View**: Automatically limits deep directory listings to prevent terminal flooding.
- **Dynamic Capping**: The number of sub-items shown is calculated based on the directory size.
- **Clean Visuals**: Uses `lsd` for icons and colors, with custom tree formatting.
- **Self-Management**: Built-in commands to install and upgrade itself.

## Prerequisites

- **[lsd](https://github.com/lsd-rs/lsd)**: Must be installed and available in your PATH.
- **curl**: Required for self-installation and upgrades.

## Installation

You can install `nv` directly using curl:

```bash
curl -fsSL https://raw.githubusercontent.com/gabrielmsilva00/nv/main/nv | bash -s -- --self-install
```

### Installation Options
- `--local`: Install to `~/.local/bin` (default).
- `--usr`: Install to `/usr/local/bin` (requires sudo).
- `--root`: Install to `/root/.local/bin` (requires sudo).

Example:
```bash
curl -fsSL https://raw.githubusercontent.com/gabrielmsilva00/nv/main/nv | bash -s -- --self-install --usr
```

## Usage

After installing, restart your shell or run `source ~/.<shell>rc` (or the appropriate file for your shell) to apply the changes.

Simply run `nv` in any directory:

```bash
nv
```

### Options

| Flag | Description |
|------|-------------|
| `-h`, `--help` | Show help message. |
| `-a`, `-dt`, `--dotfiles` | Include hidden files (dotfiles) in the listing. |
| `-f`, `--full` | Disable item capping and show the full tree. |
| `-L`, `-t`, `--depth N` | Set the tree recursion depth (Default: 2). |
| `-r`, `--reverse` | Reverse sort order. |
| `-S` | Sort results by size. |
| `-X` | Sort results by extension. |
### Management Commands

| Command | Description |
|---------|-------------|
| `--self-upgrade` | Update `nv` to the latest version. |
| `--self-alias <file>` | Add the navigation alias to a specific RC file. |
| `--self-unalias` | Remove `nv` aliases from all detected shell config files. |
| `--self-uninstall` | Completely remove `nv` (binary and aliases). |

## Self-Upgrade

Keep `nv` up to date with a single command:

```bash
nv --self-upgrade
```

## License

This project is licensed under the **Apache-2.0** License.
