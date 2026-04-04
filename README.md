# DevBernas

A comprehensive development environment setup repository for macOS and Linux (Debian variants). This repository automates the installation and configuration of development tools, applications, and dotfiles.

## Overview

This repository provides automated setup scripts for:
- **Development tools**: VS Code, Neovim, Docker, Git, and more
- **Programming languages**: Node.js (via NVM), Go, Flutter, .NET, Ruby (via RVM)
- **Shell environment**: Zsh with Oh My Zsh, Spaceship theme, and Zinit plugins
- **Terminal tools**: Tmux, FZF, MongoDB tools
- **Applications**: Chrome, Spotify, DBeaver, Android Studio
- **Dotfiles**: Zsh configuration, fonts, and application configs

## Repository Structure

```
devbernas/
├── macos/          # macOS-specific setup
│   ├── run         # Main runner script
│   ├── dev-env     # Dotfiles deployment script
│   ├── .zshrc      # Zsh configuration
│   ├── .config/    # Application configurations
│   ├── .fonts/     # Fira Code fonts
│   └── runs/       # Individual tool installation scripts
├── linux/          # Linux (Debian) setup
│   ├── run         # Main runner script
│   ├── dev-env     # Dotfiles deployment script
│   ├── .zshrc      # Zsh configuration
│   ├── .config/    # Application configurations
│   ├── .fonts/     # Fira Code fonts
│   └── runs/       # Individual tool installation scripts
└── README.md
```

## Quick Start

### macOS

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/devbernas.git
   cd devbernas/macos
   ```

2. Run the main setup script:
   ```bash
   ./run
   ```

3. Deploy dotfiles:
   ```bash
   ./dev-env
   ```

### Linux (Debian/Ubuntu)

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/devbernas.git
   cd devbernas/linux
   ```

2. Run the main setup script:
   ```bash
   ./run
   ```

3. Deploy dotfiles:
   ```bash
   ./dev-env
   ```

## Available Tools

### macOS Tools

| Tool | Script | Description |
|------|--------|-------------|
| Zsh | `runs/zsh` | Shell with Oh My Zsh, Spaceship theme, Zinit plugins |
| VS Code | `runs/vscode` | Code editor |
| Neovim | `runs/neovim` | Terminal-based editor |
| Docker | `runs/docker` | Containerization platform |
| Git | `runs/git` | Version control |
| NVM | `runs/nvm` | Node.js version manager |
| Go | `runs/golang` | Go programming language |
| Flutter | `runs/flutter` | Flutter SDK |
| .NET | `runs/dotnet` | .NET SDK |
| RVM | `runs/rvm` | Ruby version manager |
| Tmux | `runs/tmux` | Terminal multiplexer |
| FZF | `runs/fzf` | Fuzzy finder |
| MongoSH | `runs/mongosh` | MongoDB shell |
| MongoDB Compass | `runs/mongodbcompass` | MongoDB GUI |
| Chrome | `runs/chrome` | Web browser |
| Android | `runs/android` | Android Studio |
| DBeaver | `runs/dbeaver` | Database tool |
| Redis | `runs/redis` | Redis tools |
| Another Redis | `runs/anotherredis` | Redis GUI |
| DevTools | `runs/devtools` | Xcode Command Line Tools |
| Love2D | `runs/love2d` | 2D game framework |
| OpenCode | `runs/opencode` | OpenCode CLI |

### Linux Tools

| Tool | Script | Description |
|------|--------|-------------|
| Zsh | `runs/zsh` | Shell with Oh My Zsh, Spaceship theme, Zinit plugins |
| VS Code | `runs/vscode` | Code editor |
| Neovim | `runs/neovim` | Terminal-based editor |
| Docker | `runs/docker` | Containerization platform |
| Git | `runs/git` | Version control |
| NVM | `runs/nvm` | Node.js version manager |
| Go | `runs/golang` | Go programming language |
| Flutter | `runs/flutter` | Flutter SDK |
| .NET | `runs/dotnet` | .NET SDK |
| RVM | `runs/rvm` | Ruby version manager |
| Tmux | `runs/tmux` | Terminal multiplexer |
| FZF | `runs/fzf` | Fuzzy finder |
| MongoSH | `runs/mongosh` | MongoDB shell |
| MongoDB Compass | `runs/mongodbcompass` | MongoDB GUI |
| Chrome | `runs/chrome` | Web browser |
| Android | `runs/android` | Android Studio |
| DBeaver | `runs/dbeaver` | Database tool |
| Redis | `runs/redis` | Redis server |
| Another Redis | `runs/anotherredis` | Redis GUI |
| Spotify | `runs/spotify` | Music streaming |
| GCM | `runs/gcm` | Git Credential Manager |
| Love2D | `runs/love2d` | 2D game framework |
| OpenCode | `runs/opencode` | OpenCode CLI |

## Usage

### Running Individual Scripts

You can run specific installation scripts by filtering:

```bash
# macOS
./run zsh      # Install only Zsh
./run vscode   # Install only VS Code

# Linux
./run zsh      # Install only Zsh
./run docker   # Install only Docker
```

### Dry Run Mode

Test what would be installed without making changes:

```bash
./run --dry
./dev-env --dry
```

### Updating Tools

Run the update script to keep tools current:

```bash
./runs/update
```

## Dotfiles Management

The `dev-env` script manages your dotfiles by:

1. Copying `.config/` directories to `$XDG_CONFIG_HOME`
2. Installing Fira Code fonts
3. Deploying shell configuration files (`.zshrc`, `.zshenv`, `.profile`)

### Customizing Dotfiles

1. Edit files in `macos/` or `linux/` directories
2. Run `./dev-env` to deploy changes

## Shell Features

The Zsh configuration includes:

- **Oh My Zsh**: Framework for managing Zsh configuration
- **Spaceship Prompt**: Minimalistic, powerful and extremely customizable Zsh prompt
- **Zinit**: Flexible and fast Zsh plugin manager
- **Plugins**:
  - `fast-syntax-highlighting`: Syntax highlighting
  - `zsh-autosuggestions`: Fish-like suggestions
  - `zsh-completions`: Additional completions

## Requirements

### macOS
- macOS 10.15 or later
- Homebrew (will be installed if missing)
- Internet connection

### Linux
- Debian-based distribution (Ubuntu, Debian, Mint, etc.)
- `sudo` access
- Internet connection

## Troubleshooting

### Permission Issues

If you encounter permission errors:
```bash
chmod +x run dev-env runs/*
```

### Script Failures

Run scripts individually to identify issues:
```bash
bash -x ./runs/zsh
```

### Resetting Environment

To reset your environment:
1. Remove installed tools manually
2. Delete `~/.oh-my-zsh`, `~/.nvm`, `~/.rvm`, `~/.local/share/zinit`
3. Re-run setup scripts

## Contributing

1. Fork the repository
2. Create a feature branch
3. Add your changes
4. Submit a pull request

## License

MIT License - feel free to use and modify for your own development environment.

## Author

Bernardo - Development environment automation for productive coding.
