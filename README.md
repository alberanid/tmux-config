Installation
============

    git clone git://github.com/alberanid/tmux-config.git ~/.tmux
    ln -s ~/.tmux/tmux.conf ~/.tmux.conf
    cd ~/.tmux
    git submodule init
    git submodule update
    # now run tmux and press ctrl+a I


Requirements
============

tmux 1.9 or later. An unofficial Ubuntu 14.04 backport can be found here: https://launchpad.net/~pi-rho/+archive/ubuntu/dev


Main commands and shortcuts
===========================

**Windows:**
* **ctrl+a c** to create a window
* **ctrl+a X** to change window (where X is window's number)
* **ctrl+a ,** to rename a window

**Splits:**
* **ctrl+a v** split vertically
* **ctrl+a v** split horizontally
* **ctrl+a Left/Right/Up/Down** move to another split
* **ctrl+a ctrl+Left/Right/Up/Down** resize split

**Copy mode:**
* **ctrl+a [** enter copy mode (**ctrl+a PageUp** to move immediately)
* **ESC** quit copy mode

**Sessions:**
* **ctrl+a d** detach
* **tmux new [-s name]** start a new session
* **tmux a [-t name]** attach to a session
* **tmux ls** list sessions
* **kill-session -t name** kill a session


Author and license
==================

    Davide Alberani <da@erlug.linux.it> (C) 2016
    Released under the terms of the CC BY-SA license: https://creativecommons.org/licenses/by-sa/4.0/
