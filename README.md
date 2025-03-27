## Install ZSH
```bash
sudo apt install zsh \
-y
```
## Install oh-my-zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
## Install powerline10k
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
## Change default theme for zsh
```bash
sed -i 's/robbyrussell/powerlevel10k\/powerlevel10k/g' ~/.zshrc
```
## Restart terminal
```bash
zsh
```
Preferences:
- Lean
- Unicode
- 256 colors
- 24-h
- Two lines
- Disconnected
- No frame
- Compact
- Many icons
- Concise
- Transient Prompt - No
- Instant prompt - Verbose

If needed change default shell to zsh
```bash
chsh -s $(which zsh)
```
If needed restart powerline10k
```bash
p10k configure
```

## Install plugins
```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git \
${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting && \
git clone https://github.com/zsh-users/zsh-autosuggestions \
${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

## Add plugin names into .zshrc
```bash
sed -i 's/plugins=(git)/plugins=( git zsh-syntax-highlighting zsh-autosuggestions )/g' .zshrc
```
Reload zsh again
```bash
zsh
```

## Shell aliases
```bash
# Git aliases
alias ssh-login="eval $(ssh-agent) ; ssh-add"
alias gpatf="git pull --all --tags --force"
alias glg="git log --graph"
alias glga="git log --graph --all"
```

```bash
# Tmux aliases
alias tns="tmux new-session -s"
alias tat="tmux attach -t"
```

```bash
# Kubernetes aliases
alias k="kubectl"
```

```bash
# Terraform aliases
alias tf="terraform"
```

## Fonts
```bash
# Look for Code New Roman Nerd Font Complete Mono
https://www.nerdfonts.com/font-downloads
```
