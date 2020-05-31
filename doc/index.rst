===========================================
Dey's Coding Documentation 
===========================================

Hi! This is Dibyendu Dey's github space where he has documented all solved problems, useful tips and best-known-methods. Sphinx documentation was created to track all solved problems and its potential use for future references. 

===========================================
Python Helps
===========================================
.. toctree::
   :maxdepth: 2

   tips.rst

===========================================
Software helps	  
===========================================
.. toctree::
   :maxdepth: 2

   git.rst

===========================================
Software Projects	  
===========================================
.. toctree::
   :maxdepth: 2

   project.rst

===========================================
Release Methods   
===========================================
Below are steps to push the Sphinx documentations:	
	* Both Doc and Build in same repo 
		``cd <repo_dir>``
		``>git pull``
		``sphinx-build -b html . ..``
	* After making new build, Please git add all files: ``git add *``
		``git commit -m "put your comments"``
		``git push``
	* once update is completed check `www.dib-dey.github.io <https://dib-dey.github.io/>`_   
