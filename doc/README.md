# spninx_doc
Personal webpage in GitHub using Sphinx Documentation

Clone the following repo:

	>git clone https://github.com/Dib-Dey/spninx_doc.git

Get to following directory and run the command as shown below:	

	>cd c:\<dir>\spninx_doc
	**usage: sphinx-build [OPTIONS] SOURCEDIR OUTPUTDIR [FILENAMES...]**
	>sphinx-build -b html . .\build 

Need to change the html theme: `weblink <http://www.sphinx-doc.org/en/stable/theming.html>`_

	>>> go to conf.py
	>>> change the theme variable html_theme = 'classic'

Any good example of docstring manipulation:

	>https://pythonhosted.org/an_example_pypi_project/sphinx.html


add the module for docu in code.rst file. 

	>>> automodule:: Python_problems.minion_game

If you want to show docstring of individual function 

	>>> need to add :members: as shown in code.rst 
