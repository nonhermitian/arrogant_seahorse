# Quantum Information Software Kit (QISKit) [0.5.0]

[![Build Status](https://travis-ci.org/nonhermitian/arrogant_seahorse.svg?branch=master)](https://travis-ci.org/nonhermitian/arrogant_seahorse)

## Installation

It is recommended that you have [Anaconda for Python 3.6+](https://www.anaconda.com/download/) installed.

### Linux
You need `gcc-5` or higher installed.

### Mac OS
You should have the Xcode command line tools installed (`xcode-select --install`).  Optionally, you can install the `llvm` from Homebrew for OpenMP support: `brew install llvm`.  If doing so, the relvant directories must be added to your `.bash_profile`.  For example:

```
# for homebrew llvm
export PATH="/usr/local/opt/llvm/bin:$PATH"
export LDFLAGS="$LDFLAGS -L/usr/local/Cellar/llvm/6.0.0/lib"
export CPPFLAGS="$CXXFLAGS -I/usr/local/Celler/llvm/6.0.0/include"
```
In this case, the build instructions below are slightly modified:

```
CC=clang CXX=clang python setup.py build_ext -inplace
```

### Windows
You must have Visual Studio 2015 (not 2017) installed with the optional C++ and Python packages installed.  The [Community Edition](https://go.microsoft.com/fwlink/?LinkId=532606&clcid=0x409) is free.

### Universal
To build the `c++` modules, go to the installation directory and run:

```
python setup.py build_ext -inplace
```
To run the tests (online tests require that you have your `Qconfig.py` file in the same directory as `setup.py`:

```
python setup.py test
```

If everything passes (it should), installation is:

```
python setup.py install
```
