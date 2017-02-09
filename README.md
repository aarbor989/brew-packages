# brew-packages
## Brew and Brew Cask packages backed up every login
```
brew list | awk '{s="brew install "; for(i=1;i<=NF;i++){ print s $i}}' > ~/git/brew-packages/brew_install.sh
brew cask list | awk '{s="brew cask install "; for(i=1;i<=NF;i++){ print s $i}}' >> ~/git/brew-packages/brew_install.sh
git add ~/git/brew-packages/brew_install.sh 
git commit -m "updating brew install list" 
git push origin master
```