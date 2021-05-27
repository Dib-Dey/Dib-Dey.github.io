===========================================
Dey's Coding Documentation 
===========================================

Hi! This is Dibyendu Dey's github space where he has documented all solved problems, useful tips and best-known-methods. Sphinx documentation was created to track all solved problems and its potential use for future references. 

===========================================
Linux Helps
===========================================
.. toctree::
   :maxdepth: 2

   linux.rst

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

   software.rst

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
	* go indisde following directory ``c:<Repo_dir>``
	* ``>git pull``
	* ``>cd doc``
	* ``sphinx-build -b html . ..`` 
	* After making new build, Please git add all files: ``git add *``
	* ``git commit -m "put your comments"``
	* ``git push``
	* if have issue with pushing , get out of ``Intel work vnc connection and try``
	* once update is completed check `www.dib-dey.github.io <https://dib-dey.github.io/>`_   

