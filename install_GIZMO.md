## install required packages
mkdir -p $HOME/local
mkdir manual_install
cd manual_install/

### download openmpi, gsl, fftw, hdf5
wget https://download.open-mpi.org/release/open-mpi/v5.0/openmpi-5.0.10.tar.gz

wget https://mirrors.ibiblio.org/gnu/gsl/gsl-2.8.tar.gz

wget https://www.fftw.org/fftw-3.3.10.tar.gz

wget https://github.com/HDFGroup/hdf5/releases/download/2.1.0/hdf5-2.1.0.tar.gz

### install openmpi
tar -zxvf openmpi-5.0.10.tar.gz

cd openmpi-5.0.10/

./configure --prefix=$HOME/local

make -j8

make install

echo 'export PATH=$HOME/local/bin:$PATH' >> ~/.bashrc

echo 'export LD_LIBRARY_PATH=$HOME/local/lib:$LD_LIBRARY_PATH' >> ~/.bashrc

### install gsl
cd ..

tar -zxvf gsl-2.8.tar.gz

cd gsl-2.8/

./configure --prefix=$HOME/local

make -j8

make install

### install fftw with double and single precision
cd ..
tar -zxvf fftw-3.3.10.tar.gz

cd fftw-3.3.10/

./configure --prefix=$HOME/local --enable-mpi --enable-threads --enable-openmp

make -j8

make install

make clean

./configure --prefix=$HOME/local --enable-mpi --enable-threads --enable-openmp --enable-single

make -j8

make install

### install hdf5
cd ..

tar -zxvf hdf5-1.12.0.tar.gz

cd hdf5-1.12.0/

./configure --prefix=$HOME/local --enable-parallel --enable-shared

make -j8

make install

## download and install gizmo
cd

git clone https://github.com/pfhopkins/gizmo-public.git

cd gizmo-public/

### select Operating System (OS) or add one. You can check your OS using 'uname -a' command in terminal

vi Makefile.systype

### make a copy of Config.sh file and edit according to your need
cp Template-Config.sh Config.sh

### edit makefile (mainly add the paths to INCL and LIBS of the just installed packages)
vi Makefile

### then make to install
make clean

make
