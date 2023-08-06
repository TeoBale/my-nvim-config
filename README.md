<div align="center">
  <h1>My neovim config </h1>
</div>




## Requirements
+ Neovim >= v0.9
+ ripgrep
+ nodejs and npm
+ a brain (mandatory)
+ xrdb for xresources

## Installation
Clone repo to your nvim .config
```bash
git clone --depth 1 https://github.com/TeoBale/my-nvim-config ~/.config/nvim
```
Add mason to paht. ( Important to install LSP )

```zsh
# this is for zsh
export PATH=$PATH:~/.local/share/nvim/mason/bin
```
```zsh
source ~/.zshrc
```

## Keybinds for my config

| Keys        | Function          |
| ------------- |-------------|
| <kbd>CTRL</kbd> <kbd>h</kbd> / <kbd>j</kbd> / <kbd>k</kbd> / <kbd>l</kbd>  | Moving Window Focus Towards Left/Up/Down/Right |
| <kbd>CTRL</kbd> <kbd>b</kbd> | Open And Close NvimTree |
| <kbd>CTRL</kbd> <kbd>f</kbd> | Format Files With Built In Lsp |
| <kbd>CTRL</kbd> <kbd>\\</kbd> | Open And Close ToggleTerm |
| <kbd>LDR</kbd> <kbd>t</kbd> <kbd>t</kbd> | Open And Close ToggleTerm |
| <kbd>z</kbd> <kbd>R</kbd> | Open All Folds |
| <kbd>z</kbd> <kbd>M</kbd> | Close All Folds |
| <kbd>z</kbd> <kbd>c</kbd> | Close Fold Under Cursor |
| <kbd>z</kbd> <kbd>o</kbd> | Open Fold Under Cursor |


### Basic File Operations

| Keys        | Function          |
| ------------- |-------------|
| <kbd>LDR</kbd> <kbd>q</kbd> <kbd>q</kbd>  | Exit Neovim |
| <kbd>LDR</kbd> <kbd>q</kbd> <kbd>w</kbd> | Save And Exit Neovim |
| <kbd>LDR</kbd> <kbd>q</kbd> <kbd>s</kbd> | Save File |
| <kbd>LDR</kbd> <kbd>q</kbd> <kbd>f</kbd> | Format File |
| <kbd>LDR</kbd> <kbd>q</kbd> <kbd>x</kbd> | Close Current Buffer |

### Telescope

| Keys        | Function          |
| ------------- |-------------|
| <kbd>LDR</kbd> <kbd>f</kbd> <kbd>f</kbd>  | Basic File Picker |
| <kbd>LDR</kbd> <kbd>f</kbd> <kbd>g</kbd> | Search All Recently Visited Files |
| <kbd>LDR</kbd> <kbd>f</kbd> <kbd>r</kbd> | Search File By String |
| <kbd>LDR</kbd> <kbd>f</kbd> <kbd>c</kbd> | Cooler Colorscheme Picker |

### Hop

| Keys        | Function          |
| ------------- |-------------|
| <kbd>LDR</kbd> <kbd>h</kbd> <kbd>a</kbd>  | Search For Anywhere in the File |
| <kbd>LDR</kbd> <kbd>h</kbd> <kbd>c</kbd> | Search By A Single Character |
| <kbd>LDR</kbd> <kbd>h</kbd> <kbd>C</kbd> | Search By Two Characters |
| <kbd>LDR</kbd> <kbd>h</kbd> <kbd>l</kbd> | Search By Starting Of Line |
| <kbd>LDR</kbd> <kbd>h</kbd> <kbd>v</kbd> | Search Vertically |
| <kbd>LDR</kbd> <kbd>h</kbd> <kbd>w</kbd> | Search By Word |

### Grapple

| Keys        | Function          |
| ------------- |-------------|
| <kbd>LDR</kbd> <kbd>G</kbd> <kbd>g</kbd>  | Show All The Bookmarks |
| <kbd>LDR</kbd> <kbd>G</kbd> <kbd>t</kbd> | Toggle A Boookmark |
| <kbd>LDR</kbd> <kbd>G</kbd> <kbd>a</kbd> | Add A Bookmark |
| <kbd>LDR</kbd> <kbd>G</kbd> <kbd>r</kbd> | Delete A Bookmark |

### Other

| Keys        | Function          |
| ------------- |-------------|
| <kbd>LDR</kbd> <kbd>l</kbd> <kbd>l</kbd>  | Open Lazy Dashboard |
| <kbd>LDR</kbd> <kbd>l</kbd> <kbd>m</kbd> | Open Mason Dashboard |
| <kbd>LDR</kbd> <kbd>l</kbd> <kbd>c</kbd> | Show Available Code Actions |
| <kbd>LDR</kbd> <kbd>l</kbd> <kbd>s</kbd> | Open Symbols Outline |


## Custom Colorschemes

+ Make a new color scheme  `/lua/themes/schemes/scheme.lua` (copy the default colorscheme and change the colors) 
+ Make a colors file for it `/colors/scheme.lua`

```lua
-- /colors/scheme.lua
require("themes").setup({
  theme = "scheme",
  transparent_background = false
})
```

+ Set the color scheme in `lua/core/cfg.lua`

```lua
M.colorscheme = 'pop'
```
## Statusline Style
There are two prebuilt styles
+ To change the style edit `/lua/core/cfg.lua`

```lua
M.statusstyle = 'minimal' -- minimal | fancy
```
+ Reload Neovim



## Reference 
Credits to:
+ [kodo](https://github.com/chadcat7/kodo)
+ [dharmx](https://github.com/dharmx/nvim/)
+ [siduck](https://github.com/NvChad/NvChad)
