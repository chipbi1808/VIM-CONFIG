# VIM-CONFIG

Personal Vim configuration using [vim-plug](https://github.com/junegunn/vim-plug) and [coc.nvim](https://github.com/neoclide/coc.nvim).

## Requirements

- Vim 8+ (or Neovim)
- `git`
- Node.js + npm (required by coc.nvim)
- `gcc` and `g++` (for the C/C++ compile mappings)

## Installation

Clone the repository into `~/.vim` and link the config file:

```bash
git clone https://github.com/chipbi1808/VIM-CONFIG.git ~/.vim
ln -s ~/.vim/.vimrc ~/.vimrc
```

Open Vim and install the plugins:

```vim
:PlugInstall
```

Restart Vim afterwards. Install language servers for coc as needed, for example:

```vim
:CocInstall coc-clangd
```

## What's included

| Path                 | Description                                  |
| -------------------- | -------------------------------------------- |
| `.vimrc`             | Settings, mappings and plugin declarations   |
| `autoload/plug.vim`  | vim-plug bootstrap (committed for convenience) |
| `coc-settings.json`  | coc.nvim settings                            |

`plugged/` and `config/` are git-ignored. Plugins are reinstalled with `:PlugInstall`.

## Key mappings

Leader key is `,`.

| Mapping            | Action                              |
| ------------------ | ----------------------------------- |
| `;`                | Enter command mode (`:`)            |
| `jk` / `kj`        | Escape insert mode                  |
| `Ctrl-H/J/K/L`     | Move between windows                |
| `j` / `k`          | Move by screen line                 |
| `F5` (C++ files)   | Compile with `g++ -std=c++17` and run |
| `F6` (C files)     | Compile with `gcc -std=c11` and run   |
| `F12`              | Toggle paste mode                   |

## Troubleshooting

- coc.nvim missing: run `:PlugInstall`, then check `node --version` (Node.js must be installed).
- Diagnostics: `:CocInfo` and `:CocCommand doctor`.
