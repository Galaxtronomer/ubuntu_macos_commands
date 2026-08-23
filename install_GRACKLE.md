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

