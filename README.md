cmor-site
=========

cmor site: is built using jekyll

###Ubuntu

    sudo apt-get install ruby gem2deb rubygems-integration
    sudo gem install jekyll
    
###MAC
macs come with ruby and should work out of the box

    sudo gem install jekyll
    
if you run in to problems try homebrews ruby

    ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
    brew install ruby 
    gem install jekyll
    
###CMOR
If you don't have write access to the repo, please fork the repo and then submit a pull request

     git clone git@gitihub.com:aims-group/cmor-site.git
     cd cmor-site
     vim a-page.md
     jekyll build
     
this will build the site in the _site directory please review your changes

    git commit -am "MBH: updating a-page with content x"
    git push
    
the site htt://kitt.llnl.gov/cmor has a cron job and updates every hour, if you need a quicker responce please email one of us.
