manifest
========

On windows only
---------------
In windows, first you need msysgit (http://code.google.com/p/msysgit/), putty (http://the.earth.li/~sgtatham/putty/latest/x86/putty-0.62-installer.exe), and python2.6.
Add both of these to your PATH environment variable (right click computer > properties > environment variables)
1.  the directory in which your python is installed
2.  C:\Users\YOURUSERNAME\bin
Then, find "git bash" in your start menu, and open it.

continue as though you were on linux.

On linux only
-------------
    sudo apt-get install git-core ssh

Common instructions
-------------------
    mkdir -p ~/bin
    curl https://dl-ssl.google.com/dl/googlesource/git-repo/repo > ~/bin/repo
    chmod a+x ~/bin/repo
    repo init -u http://github.com/CLASSORGANIZATIONNAME/manifest -b master

To sync all repositories, you need to...
    repo sync -j32
    
To start a development branch (development branches are automatically rebased on the remote revision tracked by the repo manifest... so if the manifest is set to track "master", then everytime master changes, your development branch's commits will automatically be changed to start at where origin/master is, rather than where it was)
    repo start <branch name> <project name>
