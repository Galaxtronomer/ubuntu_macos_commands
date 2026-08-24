### download Grackle
git clone --recursive https://github.com/grackle-project/grackle

### install Grackle (configure Grackle as a shared library)
cd grackle

cmake -DCMAKE_INSTALL_PREFIX=$HOME/local -DBUILD_SHARED_LIBS=ON -B build

cmake --build build

cmake --install build

### testing installation
cd build/examples

./cxx_example

### -----------------------
### Older version installation
### -----------------------

### remove previous Grackle installation
rm -f ~/local/include/grackle*

rm -f ~/local/lib/libgrackle*

rm -f ~/local/lib/pkgconfig/grackle*

rm -f ~/local/lib64/libgrackle*

rm -f ~/local/lib64/pkgconfig/grackle*

### verify removal
find ~/local -name "*grackle*" -type f 2>/dev/null

### download Grackle 2.2
git clone --recursive --branch grackle-2.2 https://github.com/grackle-project/grackle.git

### enter the build directory
cd grackle/src/clib

### create machine configuration file
cp Make.mach.linux-gnu Make.mach.my-system

### Edit machine file - set paths for your system
### Change: LOCAL_HDF5_INSTALL = $(HOME)/local
### Change: MACH_INSTALL_PREFIX = $(HOME)/local
vi Make.mach.my-system

### clean any previous build files
make clean

### setup machine configuration
make machine-my-system

### set optimization level to high
make opt-high

### build the library
make

### verify the library was created
ls -la libgrackle.la

### install the library and headers to ~/local
make install

### verify headers were installed
ls -la ~/local/include/grackle*

### verify library was installed
ls -la ~/local/lib/libgrackle*

# Restore PATH if you changed it
# export PATH=$OLDPATH
