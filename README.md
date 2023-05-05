# net-snmp-centos6.5

This is to help users with Centos outdated releases add repositories that work.
I designed this Wiki to install a single package from a repositoy hence the name

Add archives replaceing the x in /6.x/ to whatever version you are running.

Please note, that if you want to upgrade packages correctly you will need to add all the versions of the repos up to the version that you want to reach, otherwise you will end up with missing dependancies.  Example:

    http://archive.kernel.org/centos-vault/6.5/updates/x86_64/$basearch/ 
    http://archive.kernel.org/centos-vault/6.6/updates/x86_64/$basearch/ 
    http://archive.kernel.org/centos-vault/6.7/updates/x86_64/$basearch/ 
so on and so forth.

Here is a list of tested repos that will return packages.  You can look at the site http://linuxsoft.cern.ch/centos-vault to view a list of versions.

    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/os/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/contrib/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/centosplus/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/fasttrack/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/updates/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/cr/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/extras/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/virt/x86_64/$basearch/


 Here is the list of repos that I used to install net-snmp and net-snmp-utils
 This will take a long time so once you hit enter on the command at the bottom,walkaway and get some rest.
 !!!!Very Important.... Make sure you update a version at a time and delete the completed repos once completed, otherwise you will break your system.

    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.6/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.7/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.8/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.9/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.0.1406/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.1.1501/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.6/os/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.7/os/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.8/os/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.9/os/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.0.1406/os/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.1.1501/os/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.6/centosplus/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.7/centosplus/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.8/centosplus/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.9/centosplus/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.0.1406/centosplus/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.1.1501/centosplus/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.6/contrib/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.7/contrib/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.8/contrib/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.9/contrib/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.0.1406/contrib/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.1.1501/contrib/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.6/fasttrack/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.7/fasttrack/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.8/fasttrack/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.9/fasttrack/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.0.1406/fasttrack/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.1.1501/fasttrack/x86_64/$basearch/
    
    yum update -y && yum upgrade --skip-broken -y && yum distribution-syncronization

 # (Broken)
Download original Tar archive  You need to modify file extentions and edit the Makefile, Makefile.rules, and the ./configure script to get it to halfway build correctly.

    wget -A --https-only https://sourceforge.net/projects/net-snmp/files/net-snmp/5.4.4/net-snmp-5.4.4.tar.gz

This will download as a .tmp, just rename it and remove the .tmp extention, so that it is left as a .tar.tg archive.
To build this you will need to run the folloing commands while terminaled into the net-snmp-5.4.4 folder. 
    ./configure
    make
    make install
Note that if you want to specify option you can always view the output of ./configure --help.  otherwise you will configure with default options.



   
    
