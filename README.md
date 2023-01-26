tautology.io
============

This is the codebase that runs [Tautology's portfolio site](http://tautology.io/). It is developed using [nanoc](http://nanoc.stoneship.org/) and rsynced in static form to the server. It is based largely on the source code for [Danne's portfolio](http://danne.stayskal.com). [Contact her](mailto:danne@stayskal.com) with any questions.

Installation
------------

Zeroth, install prerequisites:

* [OpenSSH](http://www.openssh.com/)
* [Rsync](http://rsync.samba.org/)
* [Ruby](http://www.ruby-lang.org/)
* [RubyGems](http://rubygems.org/pages/download)
* [Ruby Version Manager](https://rvm.beginrescueend.com/)
* [Bundler](http://gembundler.com/)

First, clone this codebase

	$ git clone git@github.com:tautology-art/tautology.io

Second, accept the RVM version and gemset, building Ruby 2.2.2 if you need

	$ rvm install ruby-2.2.2

Finally, install Bundler and the rest of the gemset

	$ gem install bundler
	$ bundle install

At this point, you're ready to make changes.

Maintenance
-----------

This codebase uses nanoc to build a tree of static HTML, CSS, and JavaScript resources to be uploaded to the server.  Assets (such as images and recordings) are included in this final build.  Once Bundler has nanoc and friends installed, running a maintenance server is straightforward:

	$ nanoc autocompile

This will automatically compile any changes made to the build and make them available through a lightweight webserver running at http://localhost:3000/.

Deployment
----------

To deploy, make sure you've got your deploy keys in place, then run:

	$ ./push

Easy as pie.

Credits
-------

Unless otherwise noted, all content on this site is © 2023 Tautology Arts Collective and available to you under the [Creative Commons BY-NC-SA 3.0](http://creativecommons.org/licenses/by-nc-sa/3.0/us/) license. All exceptions to this license are noted in [the colophon for this site](https://github.com/linenoise/portfolio/blob/master/content/colophon.html)
