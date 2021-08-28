# nvim setup guide

## nvim installation

Install neovimm from apt package manager

> sudo apt install neovim

## vim-plug plugin manager

Installation

[Download plug.vim](https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim)
and put it in the "autoload" directory.

#### Neovim

```sh
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

#### Vim

```sh
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

Then run :PlugInstall in nvim to install the plugins in nvim.

Run :checkhealth to check the dependancies in the nvim setup and install them.
For COC install node from the following link.
[node link](https://nodejs.org/en/download/)

Steps to download and install node in ubuntu

Step 1: Download latest or recommended node .tar.xz file from https://nodejs.org/en/

Step 2: Go to the directory in which (.tar.xz file) is downloaded.

Step 3: Update System Repositories

sudo apt update

Step 4: Install the package xz-utils

sudo apt install xz-utils

Step 5: To Extract the .tar.xz file

sudo tar -xvf name_of_file

In my case --> sudo tar -xvf node-v14.15.5-linux-x64.tar.xz

Step 6: sudo cp -r directory_name/{bin,include,lib,share} /usr/

In my case --> sudo cp -r node-v14.15.5-linux-x64/{bin,include,lib,share} /usr/

Step 7: Check the node version

node --version
Result In my case -> v14.15.5
