### ⚡ KNVIM — Custom Neovim LazyVim Configuration

Personal Neovim configuration built on the LazyVim starter template, optimized for a minimal, high-performance coding experience with strong support for Java, JavaScript/TypeScript, and Python development.

---

### ✨ Highlights and Custom Features

- 🧭 **Minimalist UI**
  - ❌ **Disabled** statusline and command line: `cmdheight = 0`, `laststatus = 0`.
  - ❌ **Disabled** smooth scrolling and mouse support: `smoothscroll = false`, `mouse = ""`.
  - 🪄 Uses `incline.nvim` to show file name and status in the winbar.

- 🧩 **Efficient Tab and Buffer Management**
  - 📑 Uses `bufferline.nvim` with `mode = "tabs"` to manage Tab Pages.
  - ⏭️ `<Tab>` and `⇧<Tab>` mapped for quick Tab Page switching.

- 🧠 **Enhanced LSP and Code Insight**
  - 💡 **Inlay Hints** enabled globally.
  - ⚙️ Custom `tsserver` and `lua_ls` configurations to control inlay hint display and reduce noisy diagnostics.
  - 🗄️ Database management support with `vim-dadbod-ui`.

- 🛡️ **Safe Text Handling**
  - 🗑️ Deletion commands (`x`, `c`, `dd`) mapped to the black hole register `"_` to avoid clobbering the system clipboard.

---

### 🛠️ Installation

Requirements: Git and Neovim v0.10+ recommended.

#### 1. Backup Old Config

```bash
mv ~/.config/nvim{,.bak}
```

#### 2. Clone Repository

```bash
git clone https://github.com/kneknew/knvim ~/.config/nvim
```

#### 3. Launch Neovim

```bash
nvim
```

✅ Run `:checkhealth` after installation to ensure LSP servers and Treesitter parsers are functional.

---

### ⌨️ Custom Keymaps

#### File Explorer and Tab Management

| Keymap | Command | Function | Source |
| :--- | :--- | :--- | :--- |
| **`<Leader>f`** | `:NvimTreeToggle` | 📂 **Toggle** File Explorer | `keymaps.lua` |
| **`<Leader>t`** | `:NvimTreeFindFile` | 🔎 Open explorer and **locate** current file | `keymaps.lua` |
| **`te`** | `:tabedit` | ➕ Open a new empty Tab Page | `keymaps.lua` |
| **`tw`** | `:tabclose` | ❌ Close current Tab Page | `keymaps.lua` |

#### Window Management

| Keymap | Command | Function |
| :--- | :--- | :--- |
| **`ss`** | `:split` | ↕️ Horizontal split below |
| **`sv`** | `:vsplit` | ↔️ Vertical split right |
| **`sh/j/k/l`** | `<C-w>h/j/k/l` | 🔀 Move to window left/down/up/right |
| **`<C-S-h/l/k/j>`** | `<C-w><</>>/+/-` | 📐 Resize window width/height |

---

### 📝 Notes

- 🔄 LazyVim installs plugins automatically on first run.
- 🔧 Adjust LSP settings and inlay hints in your local config if you prefer fewer inline decorations.
- 🩺 Run `:checkhealth` after initial setup to confirm language servers and Treesitter parsers.

---

### 🙏 Acknowledgements

Built on top of the LazyVim starter configuration and extended with community plugins such as `incline.nvim`, `bufferline.nvim`, and `vim-dadbod-ui`.
