# MacOS

## Iterm2
https://iterm2.com/

### Color Scheme
visit https://iterm2colorschemes.com

follow installation instructions and choose `schemes/zenwritten_dark.itermcolors`

## Brew
https://brew.sh/

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`


## zsh
Move to the brew zsh installation from the prebuilt, for easy updates.

`brew install zsh`

`which zsh`

`chsh -s <brew zsh path>`


## OMZ - Oh My Zsh
https://ohmyz.sh/

`sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

Plugins:
* git
* zsh-autosuggestions
* zsh-syntax-highlighting
* fzf
* zsh-eza

### zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

### fzf
`brew install fzf`

### zsh-syntax-highlighting
follow ohmyzsh instructions under https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md

## PowerLevel10k
https://github.com/romkatv/powerlevel10k

`git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`

Set in `~/.zshrc` the following: `ZSH_THEME="powerlevel10k/powerlevel10k"`

Then open a new terminal to configure p10k


## Vim
https://github.com/amix/vimrc

```
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
```

## Eza

`brew install eza`

```
git clone --depth=1 https://github.com/renovate-bot/z-shell-_-zsh-eza.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zsh-eza
```


## Python

### pipx
https://github.com/pypa/pipx
