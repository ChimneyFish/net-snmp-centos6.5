# net-snmp-centos6.5

This part is to help users with Centos outdated releases add repositories that work.


Add archives replaceing the x in /6.x/ to whatever version you are running.

Please note, that if you want to upgrade packages, you will have to add the update path per version.

    http://archive.kernel.org/centos-vault/6.5/updates/x86_64/$basearch/ 
    http://archive.kernel.org/centos-vault/6.6/updates/x86_64/$basearch/ 
    http://archive.kernel.org/centos-vault/6.7/updates/x86_64/$basearch/ 
so on and so forth.

Here is a list of tested repos that will return packages

    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/os/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/contrib/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/centosplus/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/fasttrack/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/updates/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/cr/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/extras/x86_64/$basearch/ 
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.x/virt/x86_64/$basearch/


 Upgrade Path that will work for the build net-snmp build.
 Scrip needs to run as root user or a user with sudo priv.
 This will take a long time so once you hit enter on the command at the bottom,walkaway and get some rest.

    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.6/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.7/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.8/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/6.9/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.0.1406/updates/x86_64/$basearch/
    yum-config-manager --add-repo=http://linuxsoft.cern.ch/centos-vault/7.1.1501/updates/x86_64/$basearch/
    yum update -y && yum upgrade --skip-broken -y

#  Build instuctions (incomplete as of now)

   Change Directory to the to the Directory of git clone location or where you extractedthe zip file
   
    
