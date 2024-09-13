## install required packages
brew install cmake

brew install gsl

brew install cgal

brew install cfitsio

brew install sdl2_image

sudo port install mathgl

(install xcode from app store befor qt installation)

brew install qt

sudo port install qt4-mac

## verify required packages
brew info cmake

brew info gsl

brew info cgal

brew info cfitsio

brew info sdl2_image

port contents mathgl

brew info qt

port contents qt4-mac

## make DisPerSE
unzip DisPerSE-master.zip

cd DisPerSE-master

mkdir build

cd build

cmake ../

make install -j 4
