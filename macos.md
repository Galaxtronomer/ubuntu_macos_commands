# useful terminal commands for macos
#### (I created this file to save the list of commands I use/used on my macos. I will be regularly updating this file.)

## Reboot system
sudo reboot

## Change laptop password
passwd

security set-keychain-password

## Change laptop host name
sudo scutil --set HostName Galaxy

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

brew cleanup

## Install Anaconda python
shasum -a 256 Anaconda3-2024.02-1-MacOSX-arm64.sh

bash Anaconda3-2024.02-1-MacOSX-arm64.sh

## Activate or deactivate conda
conda activate

conda deactivate

## Install python packages
pip install gala

pip install pynbody

## Add new executable apps to app list 
#### (solve 'app is damaged or can’t be opened' problem)
xattr -c /Applications/SAOImageDS9.app

xattr -c /Applications/FV.app

## Enable ssh login
sudo systemsetup -getremotelogin

sudo systemsetup -setremotelogin on

_To disable_

sudo systemsetup -setremotelogin off

## Connecting to ssh or sftp
ssh -X user_name@host_address

sftp user_name@host_address

## Disable icon preview in finder
defaults write com.apple.finder ShowIconPreview -bool false

killall Finder

## Get your ip address at specific network
ipconfig getifaddr en0

## Get your public ip address
curl ifconfig.me
