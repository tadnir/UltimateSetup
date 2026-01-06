# MacOS

## Brew
Run the updated command from [here](https://brew.sh/), should look like so:
```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"```

## Terminal
### Iterm2
https://iterm2.com/

#### Color Scheme
visit https://iterm2colorschemes.com

follow installation instructions and choose `schemes/zenwritten_dark.itermcolors`

After the import set the theme under Profiles > (Default Profile) > Colors > Color Preset

#### Look
Appearance > General:
 - change theme to 'minimal'
   
Appearance > Windows:
 - tick 'Hide Scrollbars'
   
Appearance > Tabs:
 - tick 'Show tab bar even when there is only one tab'
 - untick 'Stretch tabs to fill bar'
   
Appearance > Panes:
 - untick 'Show per-pane title bars'
   
Appearance > Dimming:
 - set 'Dimming amount' to 20

Profiles > (Default Profile) > Window:
 - New windows: '110 columns by 30 rows'

#### Important!
 - tick 'Unlimited scrollback' under Profiles > (Default Profile) > Terminal

#### Hot window
 - Keys > Hotkey > 'Create a dedicated Hotkey window'
 - Set Hotkey (recommanded Options+Command+C)
 - untick 'Pin hotkey window'
 - untick 'Automatically reopen on app reactivation'
 - tick 'Animate showing and hiding'
 - tick 'Floating window'
 - Go to hotkey profile
 - under window:
   - set transparancy to 0
   - set style to full screen
   - set screen to 'Screen with Cursor'
   - set space to 'All Spaces'

### zsh
Move to the brew zsh installation from the prebuilt, for easy updates.

```
brew install zsh
which zsh
chsh -s <brew zsh path>
```

### OMZ - Oh My Zsh
follow installation from [here](https://ohmyz.sh/), should be:
`sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

Plugins:
* git
* zsh-autosuggestions
* zsh-syntax-highlighting
* fzf
* zsh-eza
* zoxide

#### zsh-autosuggestions
`git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`

#### fzf
`brew install fzf`

#### zsh-syntax-highlighting
follow ohmyzsh instructions under [here](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)

#### Eza
`brew install eza`

```
git clone --depth=1 https://github.com/renovate-bot/z-shell-_-zsh-eza.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zsh-eza
```

### Zoxide
[Zoxide](https://github.com/ajeetdsouza/zoxide?tab=readme-ov-file#installation) is a better `cd` command, installation:
```
brew install zoxide
curl --create-dirs -O --output-dir ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zoxide https://raw.githubusercontent.com/ajeetdsouza/zoxide/refs/heads/main/zoxide.plugin.zsh
chmod -R 755 ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zoxide 
```

### Prompt
#### PowerLevel10k
follow from [here](https://github.com/romkatv/powerlevel10k), should be:
`git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`

Set in `~/.zshrc` the following: `ZSH_THEME="powerlevel10k/powerlevel10k"`

Then open a new terminal to configure p10k

### Sudo with touchid
taken from [here](https://apple.stackexchange.com/questions/259093/can-touch-id-on-mac-authenticate-sudo-in-terminal?newreg=e1fd0b41296e43c28e7632ada91dd0cb)
```
sed "s/^#auth/auth/" /etc/pam.d/sudo_local.template | sudo tee /etc/pam.d/sudo_local
```

## Vim
Base on [vimrc](https://github.com/amix/vimrc)

```
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
```

## Python
make sure your python is updated `python3 --version`

### pipx
manages python venvs for tools (e.g for utilities on the global path)
install from [here](https://github.com/pypa/pipx), should be `brew install pipx`


## Utilities
- Kubectl: `brew install kubectl`
- Tmux: `brew install tmux`
- [Terraform](https://developer.hashicorp.com/terraform/install):
  ```
  brew tap hashicorp/tap
  brew install hashicorp/tap/terraform
  terraform -install-autocomplete
  ```
- [GH (GitHub Cli)](https://cli.github.com/): 
  ```
    brew install gh
    gh auth login
    ```
 - [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html#:~:text=The%20following%20steps%20show%20how%20to%20install%20the%20latest%20version%20of%20the%20AWS%20CLI%20by%20using%20the%20standard%20macOS%20user%20interface%20and%20your%20browser.) - follow the GUI install for all users on the local machine
## Apps
- [Cursor](https://cursor.com/agents)
	- If installed power10k prompt you need to change the cursor terminal font:
	  settings -> VS Code Settings -> Features -> Terminal -> Font Family: put `MesloLGS NF`
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Caffeine - Always on display](https://www.caffeine-app.net/) - `brew install --cask caffeine`
- [AltTab](https://alt-tab-macos.netlify.app) - `brew install --cask alt-tab`
  Tip: you can configure Cmd+Tab to be the hotkey
- [Zoom](https://zoom.us/download)
- [Slack](https://slack.com/downloads/mac)
- [OBS - Screen recording](https://obsproject.com/download)
- [Raycast - Clipboard & Spotlight](https://www.raycast.com/)
- [Obsidian](https://obsidian.md/)
	- Configs:
		- settings -> files and links -> show all file types: on
		- settings -> editor -> readable file length: off
	- Plugins:
		- git - Adds a panel for committing and pulling changes if the vault is a git repo
- [Logitech Options+](https://www.logitech.com/en-us/software/logi-options-plus.html)
