# Zsh

We'll install `zsh` for all the features offered by `oh-my-zsh`. The installation and usage is really intutive. The `env.sh` is a config file we maintain so as to not pollute the `~/.zshrc` too much. `env.sh` holds aliases, exports, path changes etc.

### Zsh

Install zsh and zsh completions using homebrew

```
    brew install zsh zsh-completions
```

Now you can customize your shell using two frameworks Prezto or Oh My Zsh. So follow one of the two sections below.

#### Oh My Zsh

Install oh-my-zsh on top of zsh to get additional functionality

```
    curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh
```

if you're still in the default shell, change default shell to zsh manually

```
chsh -s /usr/local/bin/zsh
```

edit the `.zshrc` by opening the file in a text editor

```
    ZSH_THEME=pygmalion

    plugins=(git colored-man colorize github jira vagrant virtualenv pip python brew osx zsh-syntax-highlighting)

    # Add env.sh
    source ~/Projects/config/env.sh
```

### env.sh

```
#!/bin/zsh

DEFAULT_USER="josephphillips"

#PATH
export PATH="/usr/local/share/python:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin"
export EDITOR='subl -w'
# export PYTHONPATH=$PYTHONPATH
# export MANPATH="/usr/local/man:$MANPATH"
export PKG_CONFIG_PATH=/usr/local/lib/pkgconfig/

#RBENV
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init -)"

#Aliases
alias zshconfig='nano ~/.zshrc'
alias envconfig='nano ~/Sites/config/env.sh'
alias showFiles='defaults write com.apple.finder AppleShowAllFiles YES; killall Finder /System/Library/CoreServices/Finder.app'
alias hideFiles='defaults write com.apple.finder AppleShowAllFiles NO; killall Finder /System/Library/CoreServices/Finder.app'

# Use Atom for editing config files
alias zshconfig="code ~/.zshrc"
alias envconfig="code ~/Projects/config/env.sh"
```



