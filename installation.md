---
layout: default
title: CMOR Installation
---

##  CMOR Installation

Download the required libraries    
The CMOR2 requires external libraries: the zlib, netCDF-4.0 , HDF5 and
UDUNITS-2 packages to be installed.

* [zlilb ](http://zlib.net/)   
* [HDF5 library  ](http://www.hdfgroup.org/HDF5/)
* [netCDF4 library  ](http://www.unidata.ucar.edu/software/netcdf/)
* [Unidata units library - version 2](http://www.unidata.ucar.edu/software/udunits/udunits-2/udunits2.html)
* [uuid library](http://www.ossp.org/pkg/lib/uuid)

Configuring the libraries  
Be sure to build NetCDF4 with the `--enable-netcdf-4` option! Also make sure to install UDUNITS version 2 and not version 1 ! 

We suggest you use the following parameters when installing the external
components:  

* HDF5 library:   

        ./configure --prefix=<installdir> --disable-shared

* netCDF4 library:   

        ./configure --prefix=<installdir> --with-hdf5=<installdir> --enable-netcdf-4&#160; --disable-shared

  * Be sure to build NetCDF4 with the --enable-netcdf-4 option! 

* UDUNITS  version 2  library: 
  * NOTE that udunuits can now be built at the same time as netcdf by adding --with-udunits to the netcdf configure command   
  * Be sure to build UDUNITS version 2 and not version 1 ! 

        ./configure --prefix=<installdir> --disable-shared

  * UUID library:   

        ./configure --prefix=<installdir> --disable-shared
        
        ./configure --prefix=<installdir_cmor> --with-netcdf=<installdir-NetCDF>  --with-udunits2=<installdir_udunits2> --with-uuid=<installdir_uuid>
        make 
        make install

* Installing python version

    add: --with-python=<intall_dir_python>
    to the configure line

### Detailed instructions can be found in the INSTALL file in the CMOR distribution   
* [INSTALL](install.html)

For questions concerning CMOR2 installation, contact Charles Doutriaux( [doutriaux1@llnl.gov ](doutriaux1@llnl.gov) ).
