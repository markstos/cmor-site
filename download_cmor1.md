---
layout: default
title: CMOR Download
---

##  CMOR Download

The current version of CMOR is 1.3.

Download the CMOR Software:

* [cmor.tar.gz](media/tar/cmor.tar.gz) (ver 1.3) 

Download the CMOR input files for your project:

* [CFMIP\_cmor\_tables.tar.gz](media/tar/CFMIP_cmor_tables.tar.gz)
* [IAEMIP\_cmor\_tables.tar.gz](media/tar/IAEMIP_cmor_tables.tar.gz)
* [IPCC\_cmor\_tables.tar.gz](media/tar/IPCC_cmor_tables.tar.gz)

After gunzipping and extracting the files from the tars, you should read the
file named "INSTALL" (in the CMOR directory). This tells you how to create the
library. As explained in the INSTALL file, you can compile the test codes
called ipcc\_test\_code.f90 and test\_region.f90, which are in the Test
subdirectory. Then run the executables (ipcc\_test\_code and test\_region). If
you need to alter the makefile (or the compile file), other than changing
paths, please send us a copy of what you had to do, so others can avoid
repeating your work. If you are able to compile successfully, but CMOR returns
an error message on execution, you should contact Karl Taylor
(taylor13@llnl.gov). We have run ipcc\_test\_code and many other test codes on 5
different platforms: SGI, linux (PGI compiler), HP-UX, IBM (AIX-xlf), and SUN
(OS-5.8)..

Documentation of CMOR itself (cmor\_users\_guide.pdf) is found in the Doc
subdirectory included in the tar file. There is a sample code (very similar to
ipcc\_test\_code.f90) listed as an appendix in the documentation. This should
help you to write a code for converting your data to CF-compliant data, as
required for IPCC and other MIP submissions.

Please let me know if you uncover any suspected bugs, or if you have
suggestions or need further clarification.

Karl E. Taylor taylor13@llnl.gov
