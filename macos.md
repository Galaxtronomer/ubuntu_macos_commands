# useful terminal commands for macos
#### (I created this file to save the list of commands I use/used on my macos. I will be regularly updating this file.)

## Reboot system
sudo reboot

## Install Homebrew package manager
xcode-select --install

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

(echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> /Users/ankit/.zprofile

eval "$(/opt/homebrew/bin/brew shellenv)"

brew help

## Install packages using brew
brew update

brew upgrade

brew install gcc

brew install openssh

brew install wget

## Remove temporary or unused files
brew autoremove

## Install Anaconda python
shasum -a 256 Anaconda3-2024.02-1-MacOSX-arm64.sh

bash Anaconda3-2024.02-1-MacOSX-arm64.sh

## Change laptop host name
sudo scutil --set HostName Galaxy

## Install python packages
pip install gala

pip install pynbody

## Add new executable apps to app list [solve 'app is damaged or can’t be opened' problem]
xattr -c /Applications/SAOImageDS9.app

xattr -c /Applications/FV.app
