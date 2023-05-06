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


# Installing net-snmp and net-snmp-utils on cent os 6.5 (working)

Install 6.5 Repo

    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.5/os/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.5/fasttrack/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.5/centosplus/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.5/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.5/contrib/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.5/extras/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.5/xen4/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.5/cr/x86_64/$basearch/
   
Run the update and the upgrade 

   yum update --skip-broken && yum upgrade --skip-broken
   
Install packages

   yum install net-snmp-utils.x86_64 net-snmp.x86_64 --nogpgcheck --skip-broken
   
If successfull, you should return an output somthing like this.

   ================================================================================
 Package
    Arch   Version          Repository                                     Size
================================================================================
Updating:
 net-snmp
    x86_64 1:5.5-50.el6_6.1 linuxsoft.cern.ch_centos-vault_6.5_cr_x86_64_ 306 k
 net-snmp-utils
    x86_64 1:5.5-50.el6_6.1 linuxsoft.cern.ch_centos-vault_6.5_cr_x86_64_ 174 k
Updating for dependencies:
 net-snmp-libs
    x86_64 1:5.5-50.el6_6.1 linuxsoft.cern.ch_centos-vault_6.5_cr_x86_64_ 1.5 M

Transaction Summary
================================================================================
Upgrade       3 Package(s)

Total size: 2.0 M
Is this ok [y/N]: y
Downloading Packages:
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Updating   : 1:net-snmp-libs-5.5-50.el6_6.1.x86_64                        1/6 
  Updating   : 1:net-snmp-utils-5.5-50.el6_6.1.x86_64                       2/6 
  Updating   : 1:net-snmp-5.5-50.el6_6.1.x86_64                             3/6 
  Cleanup    : 1:net-snmp-5.5-49.el6.x86_64                                 4/6 
  Cleanup    : 1:net-snmp-utils-5.5-49.el6.x86_64                           5/6 
  Cleanup    : 1:net-snmp-libs-5.5-49.el6.x86_64                            6/6 
  Verifying  : 1:net-snmp-utils-5.5-50.el6_6.1.x86_64                       1/6 
  Verifying  : 1:net-snmp-5.5-50.el6_6.1.x86_64                             2/6 
  Verifying  : 1:net-snmp-libs-5.5-50.el6_6.1.x86_64                        3/6 
  Verifying  : 1:net-snmp-libs-5.5-49.el6.x86_64                            4/6 
  Verifying  : 1:net-snmp-5.5-49.el6.x86_64                                 5/6 
  Verifying  : 1:net-snmp-utils-5.5-49.el6.x86_64                           6/6 

Updated:
  net-snmp.x86_64 1:5.5-50.el6_6.1    net-snmp-utils.x86_64 1:5.5-50.el6_6.1   

Dependency Updated:
  net-snmp-libs.x86_64 1:5.5-50.el6_6.1                                         

Complete!

# Hope this Helps!!!!
