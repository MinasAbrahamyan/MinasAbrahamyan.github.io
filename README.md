# mnba.github.io
My github site (on github.io)



Jekyll site handling & blog-post writing instructions:
======================================================

	----
	Update the ruby to version >2.0, required by jekyll (updated to v2.3.1)
	https://www.brightbox.com/docs/ruby/ubuntu/
	==Adding the repository
	If you’re using Ubuntu 14.04 (Trusty) or newer then you can add the package repository like this:

	$ sudo apt-get install software-properties-common
	$ sudo apt-add-repository ppa:brightbox/ruby-ng
	$ sudo apt-get update
	----
	# $ sudo apt-get install ruby1.8 ruby1.9.3 ruby2.2
	$ sudo apt-get install ruby2.2

	sudo gem install minima

	Create in WebBrowser new repository with the name %username%.github.io

	git clone https://github.com/mnba/mnba.github.io.git

	~/my_prjs $ cd mnba.github.io/

	#--- Now on pages
	git checkout -b pages
	jekyll new .

	pluma  _config.yml 
	~/my_prjs/mnba.github.io $
	$ subl  _config.yml 

	$manually$ remove a line _site from file .gitignore 

	jekyll build

	git add .
	git commit  -am "Initial commit of jekyll build"

	git push

	##git checkout master  ##Didn't work yet
	#git checkout pages  # return back

	#--- now on master:

	$ git checkout -b master
	   Switched to a new branch 'master'
	   Your branch is based on 'origin/master', but the upstream is gone.
		  (use "git branch --unset-upstream" to fixup)
	$ git branch --unset-upstream

	git status   # ensure we are on right branch 

	git read-tree -m -u pages:_site

	# on master branch 
	git add .
	git commit -am "initial into the master"

	git push -u origin master

	# === Let's see if this works === 
	https://minasabrahamyan.github.io/

	Site is UP

	=== #Development Flow ===\/\/\/\/\/\/\/Cycle starts from here!==\/\/\/\/\/\/\/\/\/\/\/\/====

	# Checkout to pages:
	git checkout pages

	Go directory: _posts
	# Manually: Write a new file there, in _posts
	 /* Tutorials: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
		http://commonmark.org/help/ http://www.markdowntutorial.com/  */

	$ Then do:
	jekyll build

	# commit it on pages branch 
	git add . #do this?

	git commit -m "..."

	git push

	# ---- Now in master:
	git checkout master 

	# Do this first! 
	git read-tree -m -u pages:_site

	git add . #do this!

	git commit -m "..."

	git push
	# Now news are online!
	# === C'est tout! ==== /\/\/\/\ Cycle here /\/\/\/\/\/\===============



	-----
	git checkout pages
	-----

	jekyll build
	git add .
	git commit -m "-"
	git push

	git checkout master
	git read-tree -m -u pages:_site
	git add .
	git commit -m "-"
	git push

	git checkout pages
	------
