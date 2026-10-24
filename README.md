# ⚡ velo

**A blazing-fast terminal file manager written in Rust.**

[![CI](https://github.com/quantumnic/velo/actions/workflows/ci.yml/badge.svg)](https://github.com/quantumnic/velo/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<p align="center">
  <em>Think ranger/lf/nnn — but faster, with better UX.</em>
</p>

## ✨ Features

- 🖥️ **Three-pane layout** — parent dir | current dir | file preview
- ⌨️ **Vim keybindings** — hjkl navigation, gg/G, dd, yy, pp, and more
- 🎨 **Syntax-highlighted previews** — powered by syntect
- 📂 **File operations** — copy, move, delete (to trash), rename, create
- 🔍 **Fuzzy filtering** — real-time search with `/`
- 📊 **Git integration** — status icons (modified, staged, untracked) inline
- 🔖 **Bookmarks** — mark directories with `m`, jump with `'`
- 📋 **Bulk selection** — select multiple files with Space
- 🔄 **Sorting** — by name, size, date, extension (toggle with `s`)
- 👁️ **Hidden files toggle** — show/hide dotfiles with `.`
- 🔗 **Symlink display** — shows `→ target` for symbolic links
- 🗂️ **Breadcrumb path bar** — full path navigation at top
- 📊 **Status bar** — file count, selection count, sort mode
- ⚙️ **Configurable** — `~/.config/velo/config.toml`
- 🚀 **Opens files** — system default opener (xdg-open / open)

## 📸 Screenshots

*Coming soon — velo is a TUI application. Run it in your terminal!*

## 📦 Installation

### From source (cargo)

```bash
cargo install --git https://github.com/quantumnic/velo
```

### Homebrew (macOS)

```bash
brew tap quantumnic/tap
brew install velo
```

### From source (manual)

```bash
git clone https://github.com/quantumnic/velo
cd velo
cargo build --release
cp target/release/velo /usr/local/bin/
```

## ⌨️ Keybindings

| Key | Action |
|-----|--------|
| `h` / `←` | Go to parent directory |
| `l` / `→` / `Enter` | Enter directory / open file |
| `j` / `↓` | Move cursor down |
| `k` / `↑` | Move cursor up |
| `gg` | Jump to top |
| `G` | Jump to bottom |
| `/` | Fuzzy filter (type to search, Esc to cancel) |
| `Space` | Toggle selection |
| `dd` | Delete selected (to trash) |
| `yy` | Yank (copy) selected |
| `pp` | Paste yanked files |
| `r` | Rename file |
| `n` | Create new file |
| `N` | Create new directory |
| `s` | Cycle sort mode (name → size → date → extension) |
| `.` | Toggle hidden files |
| `m` + key | Set bookmark |
| `'` + key | Jump to bookmark |
| `q` / `Ctrl+C` | Quit |

## ⚙️ Configuration

Create `~/.config/velo/config.toml`:

```toml
show_hidden = false
sort_by = "name"  # name, size, date, extension

[colors]
directory = "blue"
file = "white"
symlink = "cyan"
selected = "yellow"

[keybinds]
# Custom keybinds (coming in v0.2.0)
```

## ⚡ velo vs the rest

| Feature | velo | ranger | lf | nnn |
|---------|------|--------|----|-----|
| Language | Rust 🦀 | Python | Go | C |
| Startup time | ~5ms | ~200ms | ~10ms | ~5ms |
| Three-pane | ✅ | ✅ | ✅ | ❌ |
| Syntax preview | ✅ | plugin | ❌ | ❌ |
| Git integration | ✅ | plugin | ❌ | ❌ |
| Fuzzy filter | ✅ | ❌ | ✅ | ✅ |
| Trash support | ✅ | ✅ | ❌ | ✅ |
| Config file | ✅ | ✅ | ✅ | ❌ |
| Bookmarks | ✅ | ✅ | ✅ | ✅ |
| Vim keybinds | ✅ | ✅ | ✅ | partial |

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Ensure tests pass (`cargo test`)
4. Ensure code is clean (`cargo fmt && cargo clippy -- -D warnings`)
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

Copyright (c) 2026 Nicola Spieser
