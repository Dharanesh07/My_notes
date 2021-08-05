# Github dotfiles setup

[reference for dotfiles setup](https://antelo.medium.com/how-to-manage-your-dotfiles-with-git-f7aeed8adf8b)

## Setup from scratch for the first time

1. create a .dotfiles folder, which we'll use to track your dotfiles
    > git init --bare $HOME/.dotfiles

2.  create an alias dotfilesso you don't need to type it all over again
    > alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'

3. set git status to hide untracked files
    > dotfiles config --local status.showUntrackedFiles no

4. add the alias to .bashrc (or .zshrc) so you can use it later
    > echo "alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'" >> $HOME/.bashrc


## Setup environment in a new computer

1. clone your github repository
    > git clone --bare https://github.com/USERNAME/dotfiles.git $HOME/.dotfiles

2. define the alias in the current shell scope
    > alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'

3.  checkout the actual content from the git repository to your $HOME
    > dotfiles checkout


# Github ssh key setup guide

1. Paste the text below, substituting in your GitHub email address.
    > ssh-keygen -t ed25519 -C "your_email@example.com"
This creates a new ssh key, using the provided email as a label.
    Generating public/private ed25519 key pair.

2. copy the public key from the .ssh directory and paste in the github account.

3. Start the ssh agent in the background ssh agent in the background
    > eval "$(ssh-agent -s)"

4. Add your ssh key to the ssh agent
    > ssh-add ~/.ssh/id_ed25519

# Github setup for fist time

1. create folder named git in .config directory and create a file named config in "~/.config/git/config"

2. Open a terminal/shell and type:
    > git config --global user.name "Your name here"
    
    > git config --global user.email "your_email@example.com"
    
    > git config --global color.ui true
    
    > git config --global core.editor emacs




