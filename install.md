---
layout: default
title: Install
---

## INSTALL
###CMOR2 installation instructions

    INSTALLATION INSTRUCTIONS  
    ------------------------- 
    Climate Model Output Rewriter (CMOR) version 2.0 installation instructions.

 
    DOWNLOAD 
    --------
    You can get the latest version of the software from the CMOR homepage
    http://www2-pcmdi.llnl.gov/cmor/


    INSTALLATION
    ------------ 
    CMOR 2 requires external packages that need to be installed first. Be sure to 
    build NetCDF4 with the --enable-netcdf-4 option! Also make sure to install 
    UDUNITS version 2 and not version 1 !


    FIRST:
     Install external dependencies: 
     - zlib (usually already present on most system), http://zlib.net
     - HDF5: available at: http://hdf.ncsa.uiuc.edu/HDF5
     - NetCDF4: available at: http://www.unidata.ucar.edu/software/netcdf/
                DOT NOT FORGET to build with --enable-netcdf-4 option
     - udunits2: (not 1) http://www.unidata.ucar.edu/software/udunits/udunits-2/udunits2.html

     NOTES: it strongly recommend to use the --disable-shared argument to the 
        ./configure when building udunits2, hdf5 and netcdf4. Otherwise make 
        sure the path to hdf5 and netcdf4 lib directory is in your search path 
        or in your LD_LIBRARY_PATH environment variable.
        Also with building NetCDF4, it is very important (although extremeley 
        counter-intuitive) to add the --enable-netcdf-4 argument, otherwise 
        support for netcdf4 will not be enabled...

    You only need to install the C libraries for these.

    SECOND: Install CMOR (version 2) library
        run the configuration script, build and install

        ./configure --prefix=/path/to/where/you/want/cmor --with-netcdf=/path/to/NetCDF4 --with-hdf5=/path/to/HDF5 --with-udunits2=/path/to/udunits2
        make
        make install

       NOTE: at the configure stage there are some influential variables:
        CC       : C comipler to use
        CPPFLAGS : C preprocessing macros
        CFLAGS   : C compilation flags
        FC       : Fortran compiler to use
        FFLAGS   : Fortan Compilation flags
        LDFLAGS  : Linking time compilation flags
        
        CMOR will "Best-guess" your system and set these, but if you need 
        specific values for your system make sure to set these environment 
        variables first
        
    *) installing the python version
        /path/to/your/python/bin/python setup.py install
        or simply
        make python 
        the later picks up whatever python is in your path

    CLEANING:
      make clean
      or to completely clean (i.e. remove the built lib):
      make distclean    
    
    UNINSTALLING
      make uninstall
        Note: the keyword, "uninstall", removes the library and include
              files from the location specified by "PREFIX" at configure time.

    TESTING:
      multiple tests are available
        make test
        make test_python

    LINKING ---------------------------------------------

        You will need to link against libcmor.a and the netcdf4 hdf5

    Example of linking with a fortran comipler:

    /opt/ibmcmp/xlf/8.1/bin/xlf90 -qsuffix=f=f90   
    $(DEBUG)  Test/test_fortran_example_00.f90 -L/lgm/cmor2/lib -L. -lcmor  -I/lgm/NetCDF4/include  -L/lgm/NetCDF4/lib -lnetcdf  -lhdf5_hl -lhdf5 -lm -lz  -ludunits2  -o test_fortran_example_00

    You can  look in the Makefile under the testipcc section for an example compilation on your system.

    MINI F.A.Q. is compilation

    If you get an error similar to this one:
    Error: Generic function 'cmor_write' at (1) is not an intrinsic function
    It probably means that the argument type you passed to the fortran are wrong 
    and that the compiler canot find a matching function in the cmor_write interface 
