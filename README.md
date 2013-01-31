manifest
========

On windows only
---------------
In windows, I'd recommend using cygwin and letting repo do the legwork... otherwise, you'll need msysgit (http://code.google.com/p/msysgit/), and putty (http://the.earth.li/~sgtatham/putty/latest/x86/putty-0.62-installer.exe), and you'll have to manually keep all of the repos in sync with origin
If you're on windows, and not using cygwin, stop reading here. you're on your own
In cygwin setup, make sure you have git-core, ssh, and python installed.

On linux only
-------------
    sudo apt-get install git-core ssh

Common instructions
-------------------
    mkdir -p ~/bin
    wget  --no-check-certificate https://dl-ssl.google.com/dl/googlesource/git-repo/repo -O ~/bin/repo
    chmod a+x ~/bin/repo
    repo init -u http://github.com/CompuderGrafix/manifest -b master

To sync all repositories, you need to...

    repo sync -j32
    
To start a development branch (development branches are automatically rebased on the remote revision tracked by the repo manifest... so if the manifest is set to track "master", then everytime master changes, your development branch's commits will automatically be changed to start at where origin/master is, rather than where it was)

    repo start <branch name> <project name>


Repo how-to (everything that mentions gerrit isn't applicable, because gerrit is a code review system that sits in between uploads and github)
http://source.android.com/source/version-control.html
