# SiteManager-Planning

The purpose for this repo is to collect all thoughts on the planning stages for the SiteManager web hosting control panel.  

## Repo layout

* `Proposed/` - All proposed features live in here until they are promoted to Approved status.

* `Approved/` - All approved features will be moved to this folder after they have been dicussed and documented, all approved features will live in their own sub-directories.  

## History behind the project

The idea came about for SiteManager as a result of years using products such as WHM/cPanel and even Dreamhosts control panel.

As we currently own our own server and host at the very least 10 websites we wanted to leverage some of what the Dreamhost control panel offers aswel as some of the rebust features of cPanel.

One thing we currently don't like about cPanel is the way the home directories are set up for each account.  We want to have our clients websites hosted in their own folders, cpanel currently requires them to live in `public_html/` which for each domain and subdomains becomes a bit of a cluster...

For instance the public website for renegadestudios.ca would live in `/home/someuser/renegadestudios.ca/http/public` on our implementation, this resembles the way dreamhost does things.  This would also promote support for various frameworks such as [Laravel](http://laravel.com) and [Ruby on Rails](http://rubyonrails.org).

This would also allow us to support site- and system-independent configurations and non-standard configurations.  Want a custom PHP or Ruby version for a specific site? easy, just complie and install into your sites director and edit your configuration files located in `somedomain.com/config`.
