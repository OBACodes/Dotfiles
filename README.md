1. Install Apple's Command Line Tools, which are prerequisites for Git and Homebrew.
`xcode-select --install`

2. clone repo into new hidden directory.

# Use SSH (if set up)...
git clone git@github.com:OBACodes/Dotfiles.git ~/.dotfiles

3. Create symlinks in the Home directory to the real files in the repo.
ln -s ~/.dotfiles/.zshrc ~/.zshrc
ln -s ~/.dotfiles/.gitconfig ~/.gitconfig
ln -s ~/.dotfiles/.tmux.config ~/.tmux.config

4. Install Homebrew, followed by the software listed in the Brewfile.
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Then pass in the Brewfile location...
brew bundle --file ~/.dotfiles/Brewfile

# ...or move to the directory first.
cd ~/.dotfiles && brew bundle

