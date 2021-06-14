===========================================
Linux useful commands
===========================================

Find and grep:
	
	>>> find . -type f -name "*.sv" -o -name "*.svh" | xargs grep highz --color -n -s

List the files which have been found in find and grep:

	>>> find . -type f -name "*.sv" -o -name "*.svh" | xargs grep highz --color -n -s -l

Use max depth in finding:
	
	>>> find . -iname "*.json" -maxdepth 5 | xargs grep -l elab_opts | xargs ~/sublime

Get context during find:

	>>> git status | xargs grep softev -C 2 -s -n --color=always

Grep multiple files:

	>>> find . -type d \( -path ./target -o -path ./src \) -prune -type f -name "*.sv" -o -name "*.svh"

How to use find command?

	>>> find -type f -iname "IP743LPDDRGEN6DFISSEW*" -name "*.sv"

How to use grep efficiently? 

	search only in current directory:
	
	>>> grep -i "name"
	
	search in specific folder 
	
	>>> grep -R "name" folder/*
	
	find all the .json file and search the word json in each of the files 
	
	>>> find . Ps aux -name "*.json" | xargs grep --color=always "register"


How find the top 20 folders/files including the sub-directories, using largest disk space:
	
	>>> du -Sh * | sort -rh | head -20

How to kill specific process?

	>>> ps aux | grep ddey | tr -s " " | cut -d " " -f 2| xargs kill

How to check usage summary?

	>>> stodstatus storage-users --fields User,NumFiles,Usage,Age30,Age90,Age180,Age360 --fie " User, GB ( usage )" --sort -Age360,-Age180,-Age90,-Usage --number 100 "path=='/path_to_drive'"
	>>> stodstatus storage-directories --fie "path,subdirectory::80,user,group,numfiles,GB(usage)" --sort-by usage "path=='/path_to_drive'" 

Install pycharm in linux:
	
	>>> download with FIreFox, unpacked with "tar -xvzf pycharm-community-2020.3.3.tar.gz"
	>>> run "pycharm-community-2020.3.3/bin/pycharm.sh"

Install Sublime:
	
	>>> download: 