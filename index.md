---
layout: default
title:
---

##  Climate Model Output Rewriter (CMOR)

The "Climate Model Output Rewriter" (CMOR, pronounced "Seymour") comprises a
set of C-based functions, with bindings to both Python and FORTRAN 90, that
can be used to produce CF-compliant netCDF files that fulfill the requirements
of many of the climate community's standard model experiments. These
experiments are collectively referred to as MIP's and include, for example,
AMIP, CMIP, CFMIP, PMIP, APE, and IPCC scenario runs. The output resulting
from CMOR is "self-describing" and facilitates analysis of results across
models.

Much of the metadata written to the output files is defined in MIP-specific
tables, typically made available from each MIP's web site. CMOR relies on
these tables to provide much of the metadata that is needed in the MIP
context, thereby reducing the programming effort required of the individual
MIP contributors.

CMOR2

* [Download](download.html)
* [Documentation](documentation.html)
* [Tables](tables.html)
* [Mailing list](mailing-list.html)
* [RELEASE NOTES ]()

For questions concerning CMOR2, contact the cmor [list](mailing-list.html) ( [cmor@lists.llnl.gov](cmor@lists.llnl.gov) ).

Old CMOR (CMOR1)

* [Download](download_cmor1.html)
* [Documentation](documentation_cmor1.html)

For questions concerning CMOR, contact Karl Taylor ( [taylor13@llnl.gov](taylor13@llnl.gov) ).
