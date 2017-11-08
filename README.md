 [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)


# SCExAO : Subaru Extreme Adaptive Optics - Real Time System Computer

## Overview

SCExAO instrument routines: image analysis, alignment loops etc...

Written in C, optimized for performance.


Executable launches a command line interface (CLI). Type "help" in the CLI to get started.

FALCON uses the [MILK package](https://github.com/milk-org/MILK)


## Downloading and installing 


The SCExAO package follows the standard git clone steps and GNU build process :

	git clone https://github.com/SCExAO-RTS-org/SCExAO
	git submodule init
	git submodule update
	autoreconf -i
	./configure
	make
	make install

Note: On OS X you need to use gcc-mp-5 for openMP:

	./configure "CC=/opt/local/bin/gcc-mp-5" CPPFLAGS="-I/usr/include/malloc/ -I/opt/local/include/readline" LDFLAGS="-L/opt/local/lib/"
(Replace "/opt/local/" is the location of your installed libraries. )



## Reporting bugs, issues

Report bugs and issues on [this page]( https://github.com/SCExAO-RTS-org/SCExAO/issues )


## Contributing to project


See [coding standards]( http://SCExAO-RTS-org.github.io/SCExAO/html/page_coding_standards.html ) 





## Documentation

[Online documentation]( http://SCExAO-RTS-org.github.io/SCExAO/ ) 


## Libraries

The following libraries are used:

- libtool
- automake
- readline, for reading the command line input
- ncurses-dev
- flex, for parsing the command line input
- bison, to interpret the command line input
- fftw, for performing Fourier Transforms
- gsl, for math functions and tools
- fitsio, for reading and writing FITS image files
- CUDA, CuBLAS, MAGMA for GPU acceleration (optional)

If you use NVIDIA GPUs, install cuda and magma libraries, and add "--enable-cuda and --enable-magma" options to the configure command.



## Getting Started

All functions are accessible from the command line interface (CLI). Enter the CLI and type "help" for instructions.

		./bin/SCExAO


## LICENCE


[GNU General Public License v3.0]( https://github.com/SCExAO-RTS-org/SCExAO/blob/master/LICENCE.txt )

