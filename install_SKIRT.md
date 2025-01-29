---
# - **Installing SKIRT**
---
## Install required packages
(install CMake)

(download '.dmg' file from https://cmake.org/download/, and install by opening it and dragging "CMake.app" to the Application folder)

(add cmake path to .zshrc file)

export PATH="/Applications/CMake.app/Contents/bin:${PATH}"

## Get the SKIRT code
cd

mkdir SKIRT

cd SKIRT

mkdir release run git

git clone https://github.com/SKIRT/SKIRT9.git git

## Configure and build the code
cd git

chmod +rx configSKIRT.sh

chmod +rx makeSKIRT.sh

./makeSKIRT.sh

## Download the SKIRT resource files
./downloadResources.sh

## Finalize the installation
export PATH="${HOME}/SKIRT/release/SKIRT/main:${PATH}"

---
# - **Installing PTS**
---
## Get the PTS code
cd

mkdir PTS

cd PTS

mkdir run pts

## Configuring PTS paths and aliases
export PYTHONPATH=~/PTS

alias pts="python -m pts.do"

## Testing the PTS installation
pts try me

## Listing Python package dependencies
pts list_dependencies
