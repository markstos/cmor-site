---
layout: default
title: Obtaining Tables, using the Tools
---

##  Obtaining Tables, using the Tools

Explains how to obtain and use the CMOR tables

First time around, see your project specific page to figure out the name of your repo and how to clone it

Thereafter
    
    git pull

Python-based Tools

The Lib directory contains a file named tables_manip_tools.py

make sure this file is either in your current directory or is accessible in
your python path

    import sys
    sys.path.insert(0,"/path/to/directory/containing/tables_manip_tools.py")
    import tables_manip_tools
    repo="cmip5-cmor-tables" # replace with your project name
    prefix="CMIP5" # Replace with your prefix
    url="uv-cdat.llnl.gov"
    Tables=tables_manip_tools.CMORTables(repo,prefix,url)

Fetching a table:

    table=Tables.fetchTable("Oclim")

Fetching a table at a specific (official, i.e in table) date:

    table=Tables.fetchTable("Oclim","12 May 2010")

Fetching a table if know the git commit tag:

    table =Tables.fetchATable("Oclim",gitcommit)

Checking a table date is valid:

    Tables.checkTable("Oclim","11 April 2011")

Checking a table id is valid (as stored in CMOR files):

    checkTable("Table Oclim (11 April 2011) 02c858e13f41cc2d92dde421ff54f504")
    checkTable("Table Oclim (11 April 2011)") # w/o md5

Checking a Table date and md5 is valid:

    Tables.checkTable("Oclim","11 April 2011","02c858e13f41cc2d92dde421ff54f504")
