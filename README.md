# tmux-config

Personal tmux setup with:

- Prefix remapped from Ctrl+b to Ctrl+a
- TPM plugin manager
- Catppuccin theme (currently macchiato)
- tmux-resurrect for save/restore
- Mouse support and sane pane/window defaults

## Installation

Clone and link:

```bash
git clone --recurse-submodules https://github.com/alberanid/tmux-config.git ~/.tmux
ln -s ~/.tmux/tmux.conf ~/.tmux.conf
```

If you already cloned without submodules:

```bash
cd ~/.tmux
git submodule update --init --recursive
```

Then start tmux and run:

- Ctrl+a I to install/update TPM plugins

## Requirements

- tmux 3.2+ recommended (Catppuccin works best on modern tmux)
- A Nerd Font is recommended for full icon rendering in the status line

## Main Commands And Shortcuts

The default prefix Ctrl+b is remapped to Ctrl+a.

### Layout (tmux-resurrect)

- Ctrl+a Ctrl+s: save current layout (windows, splits, paths, ...)
- Ctrl+a Ctrl+r: restore saved layout

### Windows

- Ctrl+a c: create a window
- Ctrl+a X: switch to window number X
- Ctrl+a ,: rename current window

### Splits And Pane Navigation

- Ctrl+a v: split vertically
- Ctrl+a s: split horizontally
- Ctrl+a h/j/k/l: move to pane left/down/up/right
- Alt+h/j/k/l: move between panes without prefix
- Ctrl+a Ctrl+Left/Right/Up/Down: resize current pane
- Ctrl+a Space: cycle pane layouts

### Copy Mode

- Ctrl+a [: enter copy mode
- Ctrl+a PageUp: enter copy mode and scroll immediately
- Ctrl+a ]: paste copied text
- Esc: quit copy mode

Note: copy selection keys inside copy mode depend on your tmux key-table mode and terminal.

### Session Basics

- Ctrl+a d: detach session
- tmux new -s name: start a named session
- tmux a -t name: attach to a named session
- tmux ls: list sessions
- tmux kill-session -t name: kill a session

## Included Plugins

Configured in tmux.conf:

- tmux-plugins/tpm
- catppuccin/tmux (v2.3.0)
- tmux-plugins/tmux-resurrect (v4.0.0)

## Extra Defaults In This Config

- Mouse mode enabled
- 256-color + RGB terminal features for tmux/xterm
- Large history buffer (50000 lines)
- Reload config with Ctrl+a r

## Author And License

Davide Alberani <da@erlug.linux.it> (C) 2016-2026

Released under CC BY-SA 4.0:
https://creativecommons.org/licenses/by-sa/4.0/
