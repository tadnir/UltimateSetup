# Ubuntu

## Apt & base packages
sudo apt update
sudo apt install curl wget vim git openssh-server


## Shell
### Zsh
sudo apt install zsh
chsh -s $(which zsh)
sudo chsh -s $(which zsh)

### OMZ
https://ohmyz.sh/
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

Plugins:
* git
* zsh-autosuggestions
* fzf

### fzf
https://github.com/junegunn/fzf#using-linux-package-managers
sudo apt install fzf


### zsh-autosuggestions
https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md#oh-my-zsh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions


### Prompt - PowerLevel10k
https://github.com/romkatv/powerlevel10k

`git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`

Set in `~/.zshrc` the following: `ZSH_THEME="powerlevel10k/powerlevel10k"`

Then open a new terminal to configure p10k

Install fonts from here:
`https://github.com/romkatv/powerlevel10k#manual-font-installation`


## Vim
https://github.com/amix/vimrc

```
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
```

