# Install zsh
```
sudo apt install zsh
```
# Install oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

# Install powerlevel10k theme
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

# Configure zsh
```
nano ~/.zshrc
```
# Add the following lines to ~/.zshrc:
#
# Set theme
```
ZSH_THEME="powerlevel10k/powerlevel10k"
```
#
# Set plugins
```
plugins=(
  you-should-use
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
  fzf
)
```
#
# Set aliases
```
alias c="code ."
alias ll="ls -1a"
alias ..="cd ../"
alias ..l="cd ../ && ll"
alias p10kc="p10k configure"
alias de="cd ~/Desktop"
alias ep="echo \$PATH"
alias zshrc='code ~/.zshrc'
alias topten="history | commands | sort -rn | head"
alias myip="curl http://ipecho.net/plain; echo"
alias dirs='dirs -v | head -10'
alias usage='du -h -d1'
alias uz="source ~/.zshrc"
alias sshdir="cd ~/.ssh"
alias runp="lsof -i "
alias md="mkdir "
alias ..='cd ..'
alias ...='cd ../..'
alias python='python3.10'
alias ni="npm install"
alias nig="npm install --global "
alias gag="eval '\$(ssh-agent -s)'"
alias gss="ssh-add --apple-use-keychain ~/.ssh/id_ed25519"
alias gls="ssh -T git@github.com"
alias gcm="git checkout master"
alias gs="git status"
alias gpull="git pull"
alias gf="git fetch"
alias gfa="git fetch --all"
alias gf="git fetch origin"
alias gpush="git push"
alias gd="git diff"
alias ga="git add ."
alias gb="git branch"
alias gbr="git branch remote"
alias gfr="git remote update"
alias gbn="git checkout -B "
alias grf="git reflog"
alias grh="git reset HEAD~" # last commit
alias gac="git add . && git commit -a -m "
alias gsu="git gpush --set-upstream origin "
```
```
source ~/.zshrc
```
# Install you-should-use plugin
```
git clone https://github.com/MichaelAquilina/zsh-you-should-use.git $ZSH_CUSTOM/plugins/you-should-use
```
# Install zsh-autosuggestions plugin
```
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```
# Install zsh-syntax-highlighting plugin
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```
# Install fzf
```
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```
# Configure GitHub
```
ssh-keygen -t ed25519 -C "ayushkmr484@gmail.com"
eval `ssh-agent -s`
ssh-add ~/.ssh/id_ed25519
gls
```

# Set timezone
```
sudo timedatectl set-timezone Asia/Kolkata
sudo timedatectl set-ntp true
timedatectl
```