# nv - Enhanced File Navigation Wrapper for lsd

`nv` is a smart wrapper for [lsd](https://github.com/lsd-rs/lsd) that provides a cleaner, more structured view of your directories. It automatically balances the density of information displayed by capping sub-entries based on the contents of the current folder, ensuring you get a quick overview without being overwhelmed.

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

Simply run `nv` in any directory:

```bash
nv
```

### Options

| Flag | Description |
|------|-------------|
| `-h`, `--help` | Show help message. |
| `-dt`, `--dotfiles` | Include hidden files (dotfiles) in the listing. |
| `-f`, `--full` | Disable item capping and show the full tree. |
| `-t`, `--depth N` | Set the tree recursion depth (Default: 2). |
| `--self-upgrade` | Fetch and install the latest version of `nv`. |

## Self-Upgrade

Keep `nv` up to date with a single command:

```bash
nv --self-upgrade
```

## License

This project is licensed under the **Apache-2.0** License.
