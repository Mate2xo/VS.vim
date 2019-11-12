# VSCode for Vim

## What's this?

A simple, ready-to-use basic Vim IDE setup for web development with pre-configured plugin management. It's an attempt to bring VSCode's feel into Vim, as VSCode can unfortunately get very laggy sometimes.

## Set up

* Check with `$ vim --version` if you have `+ruby` and `+python3` support. If not, install and use either `vim-athena` or `vim-gnome` (this last one seems to be launchable via `$ vim.gtk3`)
* python3 should be installed, as well as `pynvim`(`$ pip3 install --user pynvim`) for Deoplete plugin
* Clone this repo in your `~/` folder (I don't know how Vim works on Windows)
* Open any file with Vim, and use the `:PackUpdate` command
* Restart Vim

If you want to use some Ruby/Rails plugins added to this basic setup, switch your cloned `~/.vim` folder to the `ruby-rails` branch

## What's included

* [minpac plugin manager](https://github.com/k-takata/minpac): just put the repo names of the plugins you want in `.minpac.vim`, and run `:PackUpdate`, and/or `:PackClean` to delete plugins that are not listed there.
* vimrc tuned to feel like a fresh install of VSCode
* essentials:
  * [auto-pair](https://github.com/jiangmiao/auto-pairs): auto-close {[("")]}
  * [vim-surround](https://github.com/tpope/vim-surround): quickly change surrounding {[("")]}
* search plugins:
  * [NERDTree](https://github.com/scrooloose/nerdtree) (file explorer). Access with `<Ctrl> <Shift> e`, documentation: `:help nerdtree`
  * [CtrlP](https://github.com/ctrlpvim/ctrlp.vim): Access fuzzy file search with `<Ctrl> p`, documentation: `:help ctrlp`
* linting: [ALE](https://github.com/dense-analysis/ale), linting manager
  * Will use whatever linter is already installed on your machine, out-of-the-box most of the time.
  * If your local project has no linting setup, ALE will fetch your global linter configuration (if it exists)
  * Add options to `ale_fixers` options in `vimrc` to activate auto-formatting
  * documentation: `:help ale`
* Autocompletion : [deoplete](https://github.com/Shougo/deoplete.nvim)
  * [Language-Client-neovim](https://github.com/autozimu/LanguageClient-neovim) is used to connect deoplete and Language Servers
  * Javascript LSP use javascript-typescript-langserver npm package;

## Contributions

Any suggestions would be very welcome

