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
	
	>>> ps aux (to list all running process)
	>>> ps aux | grep ddey | tr -s " " | cut -d " " -f 2| xargs kill

How to check usage summary?

	>>> stodstatus storage-users --fields User,NumFiles,Usage,Age30,Age90,Age180,Age360 --fie " User, GB ( usage )" --sort -Age360,-Age180,-Age90,-Usage --number 100 "path=='/path_to_drive'"
	>>> stodstatus storage-directories --fie "path,subdirectory::80,user,group,numfiles,GB(usage)" --sort-by usage "path=='/path_to_drive'" 

Install pycharm in linux:
	
	>>> download with FIreFox, unpacked with "tar -xvzf pycharm-community-2020.3.3.tar.gz"
	>>> run "pycharm-community-2020.3.3/bin/pycharm.sh" (from the bin subdirectory)

Install Sublime:
	
download: https://download.sublimetext.com/sublime_text_3_build_3126_x64.tar.bz2

	>>> bunzip2 sublime_text_3_build_3126_x64.tar.bz2
	>>> tar -xvf sublime_text_3_build_3126_x64.tar
	>>> cd sublime_text_3
	>>> ./sublime_text

Install BeyondCompare:

Download the BeyondCompare 3 Linux Release (in my experience BC4 does not work), as a TAR file:

http://www.scootersoftware.com/bcompare-3.3.13.18981.tar.gz

Extract the file, installing it into a directory of your choice.

This example shows installation into the directory where the installer was downloaded and saved.

	>>> tar -xvzf bcompare-3.3.13.18981.tar.gz
	>>> mkdir bcomp_install
	>>> cd bcompare-3.3.13.18981
	>>> ./install.sh --prefix=`readlink -f ../bcomp_install/`
	>>> cd ..
	>>> ./bcomp_install/bin/bcompare

Install SystemVerilog syntax highlighting

Download --> SystemVerilog.sublime-syntax.txt. Then copy it to this location (~ is your home directory)

	>>> ~/.config/sublime-text-3/Packages/User

It will then be available in the syntax menu at the very bottom right of the Sublime window, either on its own



