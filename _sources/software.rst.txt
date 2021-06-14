===========================================
Git Documentation 
===========================================
Check whether a **directory is linked** with git or not 

	>>> git remote show origin 
	>>> git remote -v
	>>> #result
	>>> origin  https://github.com/Dib-Dey/Dib-Dey.github.io.git (fetch)
	>>> origin  https://github.com/Dib-Dey/Dib-Dey.github.io.git (push) 

If you get error with origin address, remove and add origin again(**first time cloning only**).

	>>> git remote rm origin
	>>> git remote add origin https://github.com/Dib-Dey/Dib-Dey.github.io.git 

check if a directory is **git controlled**:

	>>> git rev-parse --is-inside-work-tree

remove a file from tracking not local untracked file (**not** delete completely)

	>>> git rm --cached calculator_gui/gui.pyc

===========================================
Github setup
===========================================
set up github repo for first time

You can follow steps in following web:

	>>> https://pages.github.com/

It will generate git repo. The address:*https://github.com/Dib-Dey/Dib-Dey.github.io.git*.  where sphinx **build** added.

	>>> #go inside the folder c:\deydocuments\coding\build
	>>> git remote add origin https://github.com/Dib-Dey/Dib-Dey.github.io.git

Sphinx help for GitHub can be found in `Sphinx help <https://daler.github.io/sphinxdoc-test/includeme.html>`_
If you getting a 404 error, try the following:
	
	>>> cd <location of build> #example - C:\deydocuments\coding\build
	>>> touch .noj\ekyll
	>>> git add .nojekyll
	>>> git commit -m "added .nojekyll"

===========================================
Convert SVN repo to Git
===========================================

Below steps need to be followed if one wants to convert their SVN repo to Git.

step:1 (System)

	>>> Recommended OS: Unix

Step:2 (System requirement) 

	>>> Setup ~/.itools – add these tool versions (tested working January 2019)
	>>> P:subversion 1.7.2
	>>> P:git 1.8.2
	>>> Note: if .itools file doesn’t exist then make one writing these two lines

Step:3 (command) 

Get SVN committers from repo, convert to username/email for proper git commit information. Execute these commands (may take a while)

	>>> svn log {your SVN repo URL} -q > svn-log.txt
	>>> Example:  svn log https://example-svn-repo-url -q > svn-log.txt

	>>> cat svn-log.txt | awk -F"|" '/^r/ {gsub (/ /, "", $2 ); print$2" = <"$2">"}' | sort -u > authors-transform.txt

Step:4 
Below is the final conversion command:

	>>> git svn clone {your SVN repo url} -T trunk -b branches -t tags -A authors-transform.txt
	>>> Example xommand : git svn clone https://example-svn-repo-url -T trunk -b branches/number_1 -b branches -b branches/dev -t tags -A authors-transform.txt
	>>> Please refer to following link: https://stackoverflow.com/questions/54224050/svn-to-git-conversion-branch-formation

===========================================
Python to exe
===========================================
Below are steps:

	* ``pip install Pyinstaller`` 
	* Get inside the package folder 
	* Form a onefile entry to the package. e.g. ``Wx_CalC.py``
	* Package your entire application into a single executable file ``--onefile``
	* ``pyinstaller Wx_CalC.py --onefile``
	* Generate two folders: ``Build and Dist``
	* Inside Dist/ onefile exe can be found 

===========================================
Python Package
===========================================
steps followed:

	* Generate Entry file to your package cli.py
	* Test it and put it inside setup.py 
	* ``python setup.py sdist bdist_wheel``
	* It will generate ``dist`` which has ``.tar`` file for distribution 

===========================================
Publishing sphinx-generated docs on github
===========================================

Key is to add ``.nojekyll`` to the build folder. When GitHub sees a ``.nojekyll file``, it serves the root index.html file. 

More Info:

	>>> https://daler.github.io/sphinxdoc-test/includeme.html