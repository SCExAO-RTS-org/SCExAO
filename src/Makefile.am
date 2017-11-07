SUBDIRS = src
ACLOCAL_AMFLAGS = -I m4


#SUFFIXES = .c .h .y .l

bin_PROGRAMS = SCExAO
SCExAO_SOURCES = CLImain.c CommandLineInterface/CLIcore.c CommandLineInterface/CLIcore.h CommandLineInterface/calc_bison.y CommandLineInterface/calc_flex.l CommandLineInterface/calc.h
SCExAO_CPPFLAGS = -I@abs_top_srcdir@/src -DCONFIGDIR=\"@abs_top_srcdir@/config\" -DSOURCEDIR=\"@abs_top_srcdir@/src\" -DABSSRCTOPDIR=\"@abs_top_srcdir@\" -fopenmp -ldl

ACLOCAL_AMFLAGS = -I m4

## For Bison and FLEX
AM_YFLAGS = -d
AM_LFLAGS = -i 

## The contents of this variable are passed to every compilation that invokes the C preprocessor IF target_CPPFLAGS does not exit; it is a list of arguments to the preprocessor. For instance, -I and -D options should be listed here.
## AM_CPPFLAGS = -DCONFIGDIR=\"@abs_top_srcdir@/config\"

noinst_HEADERS = CommandLineInterface/calc.h

BUILT_SOURCES = CommandLineInterface/calc_bison.h


SUBDIRS = 
SCExAO_LDADD = 


## Modules are built as libraries of convenience
## Linking order matters

## 
## SCExAO modules 
##

SUBDIRS += SCExAO_DM
SCExAO_LDADD += SCExAO_DM/libascexaodm.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/SCExAO_DM

SUBDIRS += SCExAO_control
SCExAO_LDADD += SCExAO_control/libscexaocontrol.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/SCExAO_control


## Core modules last, higher level modules at the top

SUBDIRS += cudacomp
SCExAO_LDADD += cudacomp/libcudacomp.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/cudacomp

SUBDIRS += psf
SCExAO_LDADD += psf/libpsf.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/psf

SUBDIRS += img_reduce
SCExAO_LDADD += img_reduce/libimgreduce.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/img_reduce

SUBDIRS += image_format
SCExAO_LDADD += image_format/libimageformat.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/image_format

SUBDIRS += ZernikePolyn
SCExAO_LDADD += ZernikePolyn/libzernikepolyn.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/ZernikePolyn

SUBDIRS += image_basic
SCExAO_LDADD += image_basic/libimagebasic.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/image_basic

SUBDIRS += image_filter
SCExAO_LDADD += image_filter/libimagefilter.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/image_filter

SUBDIRS += image_gen
SCExAO_LDADD += image_gen/libimagegen.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/image_gen

SUBDIRS += linopt_imtools
SCExAO_LDADD += linopt_imtools/liblinoptimtools.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/linopt_imtools

SUBDIRS += statistic
SCExAO_LDADD += statistic/libstatistic.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/statistic

SUBDIRS += info
SCExAO_LDADD += info/libinfo.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/info

SUBDIRS += fft
SCExAO_LDADD += fft/libfft.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/fft


## 
## CORE modules, should always be included
##

SUBDIRS += COREMOD_arith
SCExAO_LDADD += COREMOD_arith/libcoremodarith.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_arith

SUBDIRS += COREMOD_memory
SCExAO_LDADD += COREMOD_memory/libcoremodmemory.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_memory

SUBDIRS += COREMOD_iofits
SCExAO_LDADD += COREMOD_iofits/libcoremodiofits.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_iofits

SUBDIRS += COREMOD_tools
SCExAO_LDADD += COREMOD_tools/libcoremodtools.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_tools

SUBDIRS += 00CORE
SCExAO_LDADD += 00CORE/lib00core.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/00CORE

SUBDIRS += ImageStreamIO
SCExAO_LDADD += ImageStreamIO/libimagestreamio.la
SCExAO_CPPFLAGS += -I@abs_top_srcdir@/src/ImageStreamIO
