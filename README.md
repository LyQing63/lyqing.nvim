# ☄️ Mars.nvim

[English](README.md) | [中文](README_zh.md)

Personal Neovim and tmux configuration with a focus on modern development experience, AI-assisted coding, and productivity.
Based on [Kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim).

![Screenshot](Screenshot.png)

## 📦 Installation

### Prerequisites

- **Neovim** ≥ 0.10 (recommended: 0.11+)
- **Git**
- **A Nerd Font** (for icons)
- **Node.js** (for LSP servers)
- **ripgrep** (for telescope grep)

### Quick Install

```bash
git clone https://github.com/MarsWang42/my-dev-config.git ~/Code/my-dev-config
cd ~/Code/my-dev-config
./install.sh
```

The install script will:
- Create symlinks in `~/.config/nvim` and `~/.config/tmux`
- Backup any existing configs (with timestamps)

---

## ✨ Features

### 🤖 AI-Powered Development

| Plugin | Description | Key Bindings |
|--------|-------------|--------------|
| **[claudecode.nvim](https://github.com/coder/claudecode.nvim)** | Claude Code integration for AI pair programming | `<leader>cc` toggle, `<leader>cs` send selection |
| **[nvim-gemini-companion](https://github.com/gutsavgupta/nvim-gemini-companion)** | Gemini AI integration | `<leader>gg` toggle |
| **[supermaven-nvim](https://github.com/supermaven-inc/supermaven-nvim)** | Fast AI code completion | Auto-suggests as you type |

**Claude Code keybindings:**
- `<leader>cc` - Toggle Claude Code terminal
- `<leader>cf` - Focus Claude terminal
- `<leader>cr` - Resume previous conversation
- `<leader>cs` - Send visual selection to Claude
- `<leader>cb` - Add current buffer to context
- `<leader>ca` / `<leader>cd` - Accept/Deny diff suggestions

**Gemini keybindings:**
- `<leader>gg` - Toggle Gemini sidebar
- `<leader>gc` - Switch to AI session
- `<leader>ga` / `<leader>gd` - Accept/Deny diff

---

### 🔍 Navigation & Search

| Plugin | Description | Key Bindings |
|--------|-------------|--------------|
| **[telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)** | Fuzzy finder for files, grep, and more | `<C-p>` files, `<leader>sg` grep |
| **[leap.nvim](https://github.com/ggandor/leap.nvim)** | Lightning-fast motion anywhere on screen | `e` to leap, `E` cross-window |
| **[grug-far.nvim](https://github.com/MagicDuck/grug-far.nvim)** | Find and replace across files | `<leader>gs` |

**Telescope shortcuts:**
- `<C-p>` / `<leader>sf` - Find files
- `<leader>sg` - Live grep
- `<leader>sw` - Grep current word
- `<leader><leader>` - Find buffers
- `<leader>/` - Fuzzy search in current buffer

---

### 📂 Git Integration

| Plugin | Description | Key Bindings |
|--------|-------------|--------------|
| **[neogit](https://github.com/NeogitOrg/neogit)** | Magit-like Git UI | `<leader>ng` |
| **[gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim)** | Git decorations and hunk actions | `]c` / `[c` navigate hunks |
| **[diffview.nvim](https://github.com/sindrets/diffview.nvim)** | Enhanced diff viewer | Via Neogit |

**Gitsigns shortcuts:**
- `<leader>hs` - Stage hunk
- `<leader>hr` - Reset hunk
- `<leader>hp` - Preview hunk
- `<leader>hb` - Blame line
- `<leader>hd` - Diff against index

---

### 🛠️ LSP & Code Intelligence

- **Auto-configured LSPs** via Mason: Go, TypeScript, Python, Lua, and more
- **Format on save** with conform.nvim (stylua, prettier, gofumpt, etc.)
- **Diagnostics** with inline virtual text and floating windows

**LSP keybindings:**
- `grn` - Rename symbol
- `gra` - Code actions
- `grd` - Go to definition
- `grr` - Find references
- `gO` - Document symbols
- `L` - Show line diagnostics

---

### 🎨 UI & Quality of Life

| Plugin | Purpose |
|--------|---------|
| **[tokyonight.nvim](https://github.com/folke/tokyonight.nvim)** | Colorscheme with transparent background |
| **[mini.nvim](https://github.com/echasnovski/mini.nvim)** | Statusline, surround, and text objects |
| **[which-key.nvim](https://github.com/folke/which-key.nvim)** | Keybinding hints popup |
| **[neo-tree.nvim](https://github.com/nvim-neo-tree/neo-tree.nvim)** | File explorer (`<C-e>`) |
| **[todo-comments.nvim](https://github.com/folke/todo-comments.nvim)** | Highlight TODO/FIXME/etc |
| **[vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator)** | Seamless navigation between vim and tmux |

---

## ⌨️ Key Bindings Summary

| Key | Action |
|-----|--------|
| `<Space>` | Leader key |
| `jk` | Escape (insert/terminal mode) |
| `;` | Command mode (`:`) |
| `tn` / `tj` / `tk` | New tab / Next / Previous |
| `<C-h/j/k/l>` | Navigate splits (tmux-aware) |
| `e` / `E` | Leap motion |

---

## 📁 Structure

```
.
├── install.sh          # Installation script
├── nvim/
│   ├── init.lua        # Entry point
│   └── lua/mars/
│       ├── options.lua     # Vim options
│       ├── keymaps.lua     # Global keybindings
│       └── plugins/        # Plugin configurations
│           ├── lsp.lua
│           ├── telescope.lua
│           ├── gitsigns.lua
│           └── ...
└── tmux/
    └── tmux.conf       # Tmux configuration
```

---

## 📝 License

MIT
