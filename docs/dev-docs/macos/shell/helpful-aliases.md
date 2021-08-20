alias d="date -u '+%Y/%m/%d/%H%M' | pbcopy"
alias uuid='uuidgen | tr "[:upper:]" "[:lower:]" | tr -d " \t\n\r" | pbcopy'

#Ruby convert yaml to json
#alias y2j="ruby -rjson -ryaml -e \"puts YAML.load_file($1).to_json\""

#alias startmouseapp="sh PycharmProjects/StartMouseApp/StartMouseApp.sh"

alias pg_start="launchctl load ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist"
alias pg_stop="launchctl unload ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist"
# Git aliases
alias gac="git add . && git commit -am $1"
alias gph="git push origin HEAD"
alias gpm="git push origin master"
alias gcb="git checkout -b $1"
alias ghkm="git push heroku $1:master"
# end git aliases

# Flutter
alias fltwc="flutter run --track-widget-creation"
alias flr="flutter run"

# Maven aliases
alias mvnshade="mvn clean install -Djava.awt.headless=true -DskipTests=true -Pshade"

alias love='/Applications/love.app/Contents/MacOS/love'

# functions
function termrel() { echo Reloading terminal; . ~/.zshrc; };

> automatic when installing rvm and nvm
## Add RVM to PATH for scripting. Make sure this is the last PATH variable change.
export PATH="$PATH:$HOME/.rvm/bin"

export NVM_DIR="/Users/jk023413/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
