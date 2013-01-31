manifest
========

On Windows
----------
    you can try these steps in cygwin (with ssh and git-core installed), but I had no luck... TRY NOT ENABLING COLORS when "repo init" asks you about them.
    
On Mac
    get a real OS, KTHXBAI
    (this may work on OS X with macports and/or the right deps)

On Linux
-------------
    sudo apt-get install git-core ssh

Common instructions
-------------------
    mkdir -p ~/bin
    wget  --no-check-certificate https://dl-ssl.google.com/dl/googlesource/git-repo/repo -O ~/bin/repo
    chmod a+x ~/bin/repo
    export PATH=$PATH:~/bin
    cd <WHERE YOU WANT YOUR CODE TO LIVE>
    repo init -u http://github.com/CompuderGrafix/manifest -b master

To sync all repositories, you need to...

    repo sync -j32
    
To start a development branch (development branches are automatically rebased on the remote revision tracked by the repo manifest... so if the manifest is set to track "master", then everytime master changes, your development branch's commits will automatically be changed to start at where origin/master is, rather than where it was)

    repo start <branch name> <project name>


Repo how-to (everything that mentions gerrit isn't applicable, because gerrit is a code review system that sits in between uploads and github)
http://source.android.com/source/version-control.html
