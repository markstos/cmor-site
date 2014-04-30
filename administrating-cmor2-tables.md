---
layout: default
title: Administrating CMOR2 Tables
---

##  Administrating CMOR2 Tables

References to admin tables

In this page [repo] should be replaced with your tables repo name

### First time

Create a public key:
    
    ssh-keygen -t rsa

(take the defaults and follow what it says)  
  
Make a copy of the generated public key  
    
    cp ~/.ssh/id_rsa.pub ~/key_for_cmor_tables.pub

And email that key (as an attachment of course) to doutriaux1@llnl.gov

Once you have been granted write access to the repo
    
    git clone git@uv-cdat.llnl.gov:[repo].git

example:

    git clone git@uv-cdat.llnl.gov:cmip5-cmor-tables.git

The tables should be stored in "Tables" directory

Always make sure your repo is up to date:
    
    git pull

If you are adding a new Table

    git add Tables/[New_Table_Name]

example:

    git add Tables/CMIP5_Amon

Once you are done editind/adding tables:

Make sure you update the md5 files using python:

    python Lib/gen_table_md5s.py

Now commit and push your changes:

    git commit -am "Explain here what you just changed"
    git push

