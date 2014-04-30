---
layout: default
title: CMOR Download
---

##  CMOR Download

 The current version of CMOR is 2.9.1 

CMOR2 supports NetCDF4 compression and irregular grids.

Since May 14th, 2010 the CMOR repo has been moved to "git" instead of
subversion. You can obtain git at: [http://git-scm.com/](http://git-scm.com/)

The First thing you will need to do is to "clone" the cmor repository. This
will take you automatically to the latest stable version

Download the  CMOR v2.9.1  Software:

RELEASE NOTES can be found [here](https://raw.github.com/PCMDI/cmor/master/RELEASE-NOTES)

In order to be notified when new releases are made, or for general questions
about CMOR, please subscribe to the cmor list 
(See [here](mailing-list.html) for more info on this).

As mentioned above the current version (2.9.1) can be obtained by cloning the
repo:

    git clone git://github.com/PCMDI/cmor.git

 This protocol is using on special port that is sometimes blocked by some organization, if this doesn't work, please use the VERY SLOW http protocol bellow 
    
    git clone http://github.com/PCMDI/cmor.git

This will take you to the latest stable version, if subsequent versions are
released you can obtain them automatically by using the following command:

    git pull

Unstable (experimental/bleeding-edge) version can be found under the "devel"
branch.

This branch, can be obtained by issuing:

    git clone git://github.com/PCMDI/cmor.git
    cd cmor
    git checkout -b devel origin/devel

thereafter you can get the latest changes via:

    git pull

It is always possible to jump back to the current "stable" release by issuing:

    git checkout master

You can also download  CMOR v1.3  , which is build on NetCDF 3.6 library
and writes data in netcdf 3.x format

    svn export http://www-pcmdi.llnl.gov/svn/repository/cmor/branches/cmor-1.x

Download the CMOR input files for your project:

CMOR2 Tables for AR5 are distributed as part of a separate repository, you can
access in the Tables subdirectory via:

    git clone git://github.com/PCMDI/cmip5-cmor-tables.git

 This protocol is using on special port that is sometimes blocked by some organization, if this doesn't work, please use the VERY SLOW http protocol bellow: 
    
    git clone http://github.com/PCMDI/cmip5-cmor-tables.git

or on the web by clicking [here](https://github.com/PCMDI/cmip5-cmor-tables) and the md5s for
each version are available [here](https://raw.github.com/PCMDI/cmip5-cmor-tables/master/Tables/md5s)
Note that tables written for CMOR1 will work with
CMOR2 but will produce  LOTS  of warning.

Read the file named "  INSTALL  " (in the CMOR directory) for the most
recent installation instructions or go to  
[Installation](installation.html). This tells you how to create the library. As
explained in the INSTALL file, you should also compile the  test codes  ,
which are  in the Test subdirectory. If you need to alter the makefile
(or the compile file), other than changing paths, please send us a copy of
what you had to do, so others can avoid repeating your work. If you are able
to compile successfully, but CMOR returns an error message on execution, you
should contact Karl Taylor (taylor13@llnl.gov).

[Documentation](https://github.com/PCMDI/cmor/raw/master/Doc/cmor_users_guide.pdf)  
of CMOR itself (  cmor_users_guide.pdf  ) is  in the   Doc subdirectory  included in the distribution. 
There is a sample code listed as an appendix in the documentation. 
This should help you to write a code for converting your data to  
[ CF-compliant ](http://cf-convention.github.io)  data, as required for IPCC and other MIP submissions. 

Please let us know if you uncover any suspected bugs, or if you have
suggestions or need further clarification.

Karl E. Taylor ( [taylor13@llnl.gov ](taylor13@llnl.gov)) (version 1.x and general questions about cmor)  
Charles Doutriaux ( [doutriaux1@llnl.gov](doutriaux1@llnl.gov) ) (version 2.0 and later)  
