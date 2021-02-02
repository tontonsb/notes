# Fish shell

## Installation

```sh
# apt-add-repository ppa:fish-shell/release-3
# apt update
# apt install fish
```

Change your default shell:

```bash
chsh -s /usr/bin/fish
```

Swap shells:

```sh
$ /bin/sh
$ /usr/bin/fish
$ /bin/dash
$ /usr/bin/zsh
$ /bin/bash
```

## Install Node & NPM

Set up [Fisher](https://github.com/jorgebucaran/fisher) if you don't have it yet:

```sh
curl https://git.io/fisher --create-dirs -sLo ~/.config/fish/functions/fisher.fish
```

Install [nvm.fish](https://github.com/jorgebucaran/nvm.fish) and get node & npm:

```sh
fisher install jorgebucaran/nvm.fish
nvm install latest
```

## Add to PATH

This only needs to be ran once and it's added permanently.

```sh
set -Ua fish_user_paths /home/juris/.composer/vendor/bin
```
