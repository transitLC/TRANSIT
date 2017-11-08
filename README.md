 [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)


# TRANSIT : Transit Light  Curve Analysis 

## Overview

Set of image processing tools and functions accessible through a command line interface (CLI). Holds images in RAM, with image stream support (shared memory with low-latency IPC support).

Written in C, optimized for performance.

Executable launches a command line interface (CLI). Type "help" in the CLI to get started.


## Downloading and installing 


The FALCON package follows the standard git clone steps and GNU build process :

	git clone https://github.com/transitLC/TRANSIT
	cd TRANSIT
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

Report bugs and issues on [this page]( https://github.com/transitLC/TRANSIT/issues )


## Contributing to project


See [coding standards]( http://FALCON-org.github.io/transitLC/html/page_coding_standards.html ) 





## Documentation

[Online documentation]( http://transitLC.github.io/TRANSIT/ ) 


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

		./bin/TRANSIT


## LICENCE


[GNU General Public License v3.0]( https://github.com/transitLC/TRANSIT/blob/master/LICENCE.txt )

