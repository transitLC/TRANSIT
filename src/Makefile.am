SUBDIRS = src
ACLOCAL_AMFLAGS = -I m4


#SUFFIXES = .c .h .y .l

bin_PROGRAMS = TRANSIT
TRANSIT_SOURCES = CLImain.c CommandLineInterface/CLIcore.c CommandLineInterface/CLIcore.h CommandLineInterface/calc_bison.y CommandLineInterface/calc_flex.l CommandLineInterface/calc.h
TRANSIT_CPPFLAGS = -I@abs_top_srcdir@/src -DCONFIGDIR=\"@abs_top_srcdir@/config\" -DSOURCEDIR=\"@abs_top_srcdir@/src\" -DABSSRCTOPDIR=\"@abs_top_srcdir@\" -fopenmp -ldl

ACLOCAL_AMFLAGS = -I m4

## For Bison and FLEX
AM_YFLAGS = -d
AM_LFLAGS = -i 

## The contents of this variable are passed to every compilation that invokes the C preprocessor IF target_CPPFLAGS does not exit; it is a list of arguments to the preprocessor. For instance, -I and -D options should be listed here.
## AM_CPPFLAGS = -DCONFIGDIR=\"@abs_top_srcdir@/config\"

noinst_HEADERS = CommandLineInterface/calc.h

BUILT_SOURCES = CommandLineInterface/calc_bison.h


SUBDIRS = 
TRANSIT_LDADD = 


## Modules are built as libraries of convenience
## Linking order matters

## 
## Transit LC module 
##

SUBDIRS += transitLC
TRANSIT_LDADD += transitLC/libtransitlc.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/transitLC



## Core modules last, higher level modules at the top


SUBDIRS += cudacomp
TRANSIT_LDADD += cudacomp/libcudacomp.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/cudacomp

SUBDIRS += psf
TRANSIT_LDADD += psf/libpsf.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/psf

SUBDIRS += img_reduce
TRANSIT_LDADD += img_reduce/libimgreduce.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/img_reduce

SUBDIRS += image_format
TRANSIT_LDADD += image_format/libimageformat.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/image_format

SUBDIRS += ZernikePolyn
TRANSIT_LDADD += ZernikePolyn/libzernikepolyn.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/ZernikePolyn

SUBDIRS += image_basic
TRANSIT_LDADD += image_basic/libimagebasic.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/image_basic

SUBDIRS += image_filter
TRANSIT_LDADD += image_filter/libimagefilter.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/image_filter

SUBDIRS += image_gen
TRANSIT_LDADD += image_gen/libimagegen.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/image_gen

SUBDIRS += linopt_imtools
TRANSIT_LDADD += linopt_imtools/liblinoptimtools.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/linopt_imtools

SUBDIRS += statistic
TRANSIT_LDADD += statistic/libstatistic.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/statistic

SUBDIRS += info
TRANSIT_LDADD += info/libinfo.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/info

SUBDIRS += fft
TRANSIT_LDADD += fft/libfft.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/fft


## 
## CORE modules, should always be included
##



SUBDIRS += COREMOD_arith
TRANSIT_LDADD += COREMOD_arith/libcoremodarith.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_arith

SUBDIRS += COREMOD_memory
TRANSIT_LDADD += COREMOD_memory/libcoremodmemory.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_memory

SUBDIRS += COREMOD_iofits
TRANSIT_LDADD += COREMOD_iofits/libcoremodiofits.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_iofits

SUBDIRS += COREMOD_tools
TRANSIT_LDADD += COREMOD_tools/libcoremodtools.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_tools

SUBDIRS += 00CORE
TRANSIT_LDADD += 00CORE/lib00core.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/00CORE

SUBDIRS += ImageStreamIO
TRANSIT_LDADD += ImageStreamIO/libimagestreamio.la
TRANSIT_CPPFLAGS += -I@abs_top_srcdir@/src/ImageStreamIO
