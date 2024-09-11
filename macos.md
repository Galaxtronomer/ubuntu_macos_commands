# useful terminal commands for macos
#### (I created this file to save the list of commands I use/used on my macos. I will be regularly updating this file.)

<h2 style="color:red;">reboot system</h2>
sudo reboot

## Install Homebrew package manager
xcode-select --install

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

(echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> /Users/ankit/.zprofile

eval "$(/opt/homebrew/bin/brew shellenv)"

brew help

brew update

## Install Anaconda python
shasum -a 256 Anaconda3-2024.02-1-MacOSX-arm64.sh
bash Anaconda3-2024.02-1-MacOSX-arm64.sh

## Change laptop host name
sudo scutil --set HostName Galaxy

## 
