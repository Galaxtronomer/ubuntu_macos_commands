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

## Install and uninstall packages using brew
brew update

brew upgrade

brew install gcc

brew install openssh

brew install wget

brew install ghostscript

brew install ffmpeg

brew install --cask gimp

brew install gh

brew install --cask gedit

brew uninstall gedit

## Remove temporary or unused files
brew autoremove

brew cleanup

## Install mac port package manager
(first download and install macport installer and then)

sudo port selfupdate

sudo port upgrade outdated

## Install and uninstall package using mac port
sudo port install gedit

sudo port uninstall gedit

## Know the containing directory of a package
brew --prefix cmake

port contents gedit

## Install Anaconda python
shasum -a 256 Anaconda3-2024.02-1-MacOSX-arm64.sh

bash Anaconda3-2024.02-1-MacOSX-arm64.sh

## Activate or deactivate conda
conda activate

conda deactivate

## Install python packages
pip install gala

pip install pynbody

pip install kivy

pip install buildozer

## Add new executable apps to app list 
#### (solve 'app is damaged or can’t be opened' problem)
xattr -c /Applications/SAOImageDS9.app

xattr -c /Applications/FV.app

## Enable or diable ssh login
sudo systemsetup -getremotelogin

(To enable)

sudo systemsetup -setremotelogin on

(To disable)

sudo systemsetup -setremotelogin off

## Connecting to ssh or sftp
ssh -X user_name@host_address

sftp user_name@host_address

## Generate ssh key
ssh-keygen -R host_address

## Disable icon preview in finder
defaults write com.apple.finder ShowIconPreview -bool false

killall Finder

## Get your ip address at specific network
ipconfig getifaddr en0

## Get your public ip address
curl ifconfig.me

## Count files in working folder
ls -1 | wc -l

## Check any issue with brew
brew doctor

## Link the unlinked kegs
brew link glib

brew link qt

(or)

brew link --force glib
brew link --force qt

## Finding files containing specific word in files with specific extension
grep -rnw handles *.py

## Directories size ignoring permission denied messages
sudo du -h -d 1 / 2>/dev/null

## See first few lines of a file (default 10 lines) without opening
head file_name

head -n 20 file_name

## Change png to pdf
sips -s format pdf preprogram.png --out preprogram.pdf

## Join multiple PDFs
pdfunite infile1.pdf infile2.pdf infile3.pdf outfile.pdf

pdfunite infile*.pdf outfile.pdf

## decript an encripted PDF file
(install qpdf, if not already)

brew install qpdf

qpdf --decrypt encripted.pdf decripted.pdf

## Zip directory
zip -r dir_name.zip dir_name

## Unzip a file
unzip filename.zip

## zip a tar directory
tar -czvf dir_rname.tar.gz dir_name/

## Unzip a tar file
tar -xzvf filename.tar.gz

## find a keyword in specific files (say in file with .txt extension)
grep -rnw keyword *.txt
