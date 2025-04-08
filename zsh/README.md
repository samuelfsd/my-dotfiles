export ZSH="$HOME/.oh-my-zsh"

ZSH_THEME="clean"

plugins=(git zsh-nvm ssh-agent zsh-autosuggestions zsh-syntax-highlighting gitfast)

source $ZSH/oh-my-zsh.sh

# alias ohmyzsh="mate ~/.oh-my-zsh"

alias dev="cd ~/workspaces"

# pnpm

export PNPM*HOME="/home/samu/.local/share/pnpm"
case ":$PATH:" in
  *":$PNPM_HOME:"*) ;;
\_) export PATH="$PNPM_HOME:$PATH" ;;
esac

# pnpm end

# bun completions

[ -s "/home/samu/.bun/_bun" ] && source "/home/samu/.bun/\_bun"

# bun

export BUN_INSTALL="$HOME/.bun"
export PATH="$BUN_INSTALL/bin:$PATH"

#THIS MUST BE AT THE END OF THE FILE FOR SDKMAN TO WORK!!!
export SDKMAN_DIR="$HOME/.sdkman"
[[ -s "$HOME/.sdkman/bin/sdkman-init.sh" ]] && source "$HOME/.sdkman/bin/sdkman-init.sh"
