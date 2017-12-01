    List the cloud provider you are using (AWS, GCE, Azure, CloudCat, other)
		Azure
    List your instances by IP address and DNS name (don't use /etc/hosts for this)
		10.0.2.4 veroj1.southcentralus.cloudapp.azure.com
		10.0.2.5 veroj2.southcentralus.cloudapp.azure.com
		10.0.2.6 veroj3.southcentralus.cloudapp.azure.com
		10.0.2.7 veroj4.southcentralus.cloudapp.azure.com
    List the Linux release you are using
		Red Hat Enterprise Linux Server release 7.4 (Maipo)
    List the file system capacity for the first node
		[root@vjaramillo1 opt]# df -h
		Filesystem      Size  Used Avail Use% Mounted on
		/dev/sda2        32G  2.4G   30G   8% /
		devtmpfs         14G     0   14G   0% /dev
		tmpfs            14G     0   14G   0% /dev/shm
		tmpfs            14G   33M   14G   1% /run
		tmpfs            14G     0   14G   0% /sys/fs/cgroup
		/dev/sdd         79G   58M   75G   1% /disk2
		/dev/sdc         79G   57M   75G   1% /disk1
		/dev/sda1       497M  142M  356M  29% /boot
		/dev/sdb1        55G  2.1G   51G   4% /mnt/resource
		tmpfs           2.8G     0  2.8G   0% /run/user/1000
		
    List the command and output for yum repolist enabled
		[root@vjaramillo1 opt]# yum repolist enabled
		Loaded plugins: langpacks, product-id, search-disabled-repos
		repo id                                                           repo name                                                                     status
		!rhui-microsoft-azure-rhel7                                       Microsoft Azure RPMs for Red Hat Enterprise Linux 7                                2
		!rhui-rhel-7-server-dotnet-rhui-debug-rpms/7Server/x86_64         dotNET on RHEL Debug RPMs for Red Hat Enterprise Linux 7 Server from RHUI         27
		!rhui-rhel-7-server-dotnet-rhui-rpms/7Server/x86_64               dotNET on RHEL RPMs for Red Hat Enterprise Linux 7 Server from RHUI               63
		!rhui-rhel-7-server-dotnet-rhui-source-rpms/7Server/x86_64        dotNET on RHEL Source RPMs for Red Hat Enterprise Linux 7 Server from RHUI        32
		!rhui-rhel-7-server-rhui-debug-rpms/7Server/x86_64                Red Hat Enterprise Linux 7 Server from RHUI (Debug RPMs)                       6,382
		!rhui-rhel-7-server-rhui-extras-debug-rpms/x86_64                 Red Hat Enterprise Linux 7 Server - Extras from RHUI (Debug RPMs)                126
		!rhui-rhel-7-server-rhui-extras-rpms/x86_64                       Red Hat Enterprise Linux 7 Server - Extras from RHUI (RPMs)                      709
		!rhui-rhel-7-server-rhui-extras-source-rpms/x86_64                Red Hat Enterprise Linux 7 Server - Extras from RHUI (Source RPMs)               276
		!rhui-rhel-7-server-rhui-optional-debug-rpms/7Server/x86_64       Red Hat Enterprise Linux 7 Server - Optional from RHUI (Debug RPMs)            4,263
		!rhui-rhel-7-server-rhui-optional-rpms/7Server/x86_64             Red Hat Enterprise Linux 7 Server - Optional from RHUI (RPMs)                 13,030
		!rhui-rhel-7-server-rhui-optional-source-rpms/7Server/x86_64      Red Hat Enterprise Linux 7 Server - Optional from RHUI (Source RPMs)           3,038
		!rhui-rhel-7-server-rhui-rh-common-debug-rpms/7Server/x86_64      Red Hat Enterprise Linux 7 Server - RH Common from RHUI (Debug RPMs)              31
		!rhui-rhel-7-server-rhui-rh-common-rpms/7Server/x86_64            Red Hat Enterprise Linux 7 Server - RH Common from RHUI (RPMs)                   228
		!rhui-rhel-7-server-rhui-rh-common-source-rpms/7Server/x86_64     Red Hat Enterprise Linux 7 Server - RH Common from RHUI (Source RPMs)             89
		!rhui-rhel-7-server-rhui-rpms/7Server/x86_64                      Red Hat Enterprise Linux 7 Server from RHUI (RPMs)                            17,720
		!rhui-rhel-7-server-rhui-source-rpms/7Server/x86_64               Red Hat Enterprise Linux 7 Server from RHUI (Source RPMs)                      5,185
		!rhui-rhel-7-server-rhui-supplementary-debug-rpms/7Server/x86_64  Red Hat Enterprise Linux 7 Server - Supplementary from RHUI (Debug RPMs)           0
		!rhui-rhel-7-server-rhui-supplementary-rpms/7Server/x86_64        Red Hat Enterprise Linux 7 Server - Supplementary from RHUI (RPMs)               238
		!rhui-rhel-7-server-rhui-supplementary-source-rpms/7Server/x86_64 Red Hat Enterprise Linux 7 Server - Supplementary from RHUI (Source RPMs)          8
		!rhui-rhel-server-rhui-rhscl-7-debug-rpms/7Server/x86_64          Red Hat Software Collections Debug RPMs for Red Hat Enterprise Linux 7 Server    570
		!rhui-rhel-server-rhui-rhscl-7-rpms/7Server/x86_64                Red Hat Software Collections RPMs for Red Hat Enterprise Linux 7 Server from   9,198
		!rhui-rhel-server-rhui-rhscl-7-source-rpms/7Server/x86_64         Red Hat Software Collections Source RPMs for Red Hat Enterprise Linux 7 Serve  3,841
		repolist: 65,056

-------------------------------MYSQL
[root@veroj1 opt]# wget http://repo.mysql.com/mysql-community-release-el7-5.noarch.rpm
--2017-12-01 15:53:17--  http://repo.mysql.com/mysql-community-release-el7-5.noarch.rpm
Resolving repo.mysql.com (repo.mysql.com)... 23.32.73.150
Connecting to repo.mysql.com (repo.mysql.com)|23.32.73.150|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 6140 (6.0K) [application/x-redhat-package-manager]
Saving to: ‘mysql-community-release-el7-5.noarch.rpm’

100%[============================================================================================================>] 6,140       --.-K/s   in 0s      

2017-12-01 15:53:18 (294 MB/s) - ‘mysql-community-release-el7-5.noarch.rpm’ saved [6140/6140]

[root@veroj1 opt]# wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.44.tar.gz
--2017-12-01 15:53:24--  https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.44.tar.gz
Resolving dev.mysql.com (dev.mysql.com)... 137.254.60.11
Connecting to dev.mysql.com (dev.mysql.com)|137.254.60.11|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://cdn.mysql.com//Downloads/Connector-J/mysql-connector-java-5.1.44.tar.gz [following]
--2017-12-01 15:53:24--  https://cdn.mysql.com//Downloads/Connector-J/mysql-connector-java-5.1.44.tar.gz
Resolving cdn.mysql.com (cdn.mysql.com)... 23.32.73.150
Connecting to cdn.mysql.com (cdn.mysql.com)|23.32.73.150|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3465760 (3.3M) [application/x-tar-gz]
Saving to: ‘mysql-connector-java-5.1.44.tar.gz’

100%[============================================================================================================>] 3,465,760   11.3MB/s   in 0.3s   

2017-12-01 15:53:25 (11.3 MB/s) - ‘mysql-connector-java-5.1.44.tar.gz’ saved [3465760/3465760]

[root@veroj1 opt]# sudo rpm -ivh mysql-community-release-el6-5.noarch.rpm
error: open of mysql-community-release-el6-5.noarch.rpm failed: No such file or directory
[root@veroj1 opt]# sudo rpm -ivh mysql-community-release-el7-5.noarch.rpm
Preparing...                          ################################# [100%]
Updating / installing...
   1:mysql-community-release-el7-5    ################################# [100%]
[root@veroj1 opt]# sudo yum update
Loaded plugins: langpacks, product-id, search-disabled-repos
mysql-connectors-community                                                                                                     | 2.5 kB  00:00:00     
mysql-tools-community                                                                                                          | 2.5 kB  00:00:00     
mysql56-community                                                                                                              | 2.5 kB  00:00:00     
(1/3): mysql-connectors-community/x86_64/primary_db                                                                            |  16 kB  00:00:00     
(2/3): mysql-tools-community/x86_64/primary_db                                                                                 |  37 kB  00:00:00     
(3/3): mysql56-community/x86_64/primary_db                                                                                     | 179 kB  00:00:00     
No packages marked for update
[root@veroj1 opt]# sudo yum install mysql-server
Loaded plugins: langpacks, product-id, search-disabled-repos
Resolving Dependencies
--> Running transaction check
---> Package mysql-community-server.x86_64 0:5.6.38-2.el7 will be installed
--> Processing Dependency: mysql-community-common(x86-64) = 5.6.38-2.el7 for package: mysql-community-server-5.6.38-2.el7.x86_64
--> Processing Dependency: mysql-community-client(x86-64) >= 5.6.10 for package: mysql-community-server-5.6.38-2.el7.x86_64
--> Processing Dependency: perl(Data::Dumper) for package: mysql-community-server-5.6.38-2.el7.x86_64
--> Processing Dependency: perl(DBI) for package: mysql-community-server-5.6.38-2.el7.x86_64
--> Running transaction check
---> Package mysql-community-client.x86_64 0:5.6.38-2.el7 will be installed
--> Processing Dependency: mysql-community-libs(x86-64) >= 5.6.10 for package: mysql-community-client-5.6.38-2.el7.x86_64
---> Package mysql-community-common.x86_64 0:5.6.38-2.el7 will be installed
---> Package perl-DBI.x86_64 0:1.627-4.el7 will be installed
--> Processing Dependency: perl(RPC::PlClient) >= 0.2000 for package: perl-DBI-1.627-4.el7.x86_64
--> Processing Dependency: perl(RPC::PlServer) >= 0.2001 for package: perl-DBI-1.627-4.el7.x86_64
---> Package perl-Data-Dumper.x86_64 0:2.145-3.el7 will be installed
--> Running transaction check
---> Package mysql-community-libs.x86_64 0:5.6.38-2.el7 will be installed
---> Package perl-PlRPC.noarch 0:0.2020-14.el7 will be installed
--> Processing Dependency: perl(Net::Daemon) >= 0.13 for package: perl-PlRPC-0.2020-14.el7.noarch
--> Processing Dependency: perl(Compress::Zlib) for package: perl-PlRPC-0.2020-14.el7.noarch
--> Processing Dependency: perl(Net::Daemon::Log) for package: perl-PlRPC-0.2020-14.el7.noarch
--> Processing Dependency: perl(Net::Daemon::Test) for package: perl-PlRPC-0.2020-14.el7.noarch
--> Running transaction check
---> Package perl-IO-Compress.noarch 0:2.061-2.el7 will be installed
--> Processing Dependency: perl(Compress::Raw::Bzip2) >= 2.061 for package: perl-IO-Compress-2.061-2.el7.noarch
--> Processing Dependency: perl(Compress::Raw::Zlib) >= 2.061 for package: perl-IO-Compress-2.061-2.el7.noarch
---> Package perl-Net-Daemon.noarch 0:0.48-5.el7 will be installed
--> Running transaction check
---> Package perl-Compress-Raw-Bzip2.x86_64 0:2.061-3.el7 will be installed
---> Package perl-Compress-Raw-Zlib.x86_64 1:2.061-4.el7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

======================================================================================================================================================
 Package                                  Arch                    Version                         Repository                                     Size
======================================================================================================================================================
Installing:
 mysql-community-server                   x86_64                  5.6.38-2.el7                    mysql56-community                              59 M
Installing for dependencies:
 mysql-community-client                   x86_64                  5.6.38-2.el7                    mysql56-community                              19 M
 mysql-community-common                   x86_64                  5.6.38-2.el7                    mysql56-community                             257 k
 mysql-community-libs                     x86_64                  5.6.38-2.el7                    mysql56-community                             2.0 M
 perl-Compress-Raw-Bzip2                  x86_64                  2.061-3.el7                     rhui-rhel-7-server-rhui-rpms                   32 k
 perl-Compress-Raw-Zlib                   x86_64                  1:2.061-4.el7                   rhui-rhel-7-server-rhui-rpms                   57 k
 perl-DBI                                 x86_64                  1.627-4.el7                     rhui-rhel-7-server-rhui-rpms                  802 k
 perl-Data-Dumper                         x86_64                  2.145-3.el7                     rhui-rhel-7-server-rhui-rpms                   47 k
 perl-IO-Compress                         noarch                  2.061-2.el7                     rhui-rhel-7-server-rhui-rpms                  260 k
 perl-Net-Daemon                          noarch                  0.48-5.el7                      rhui-rhel-7-server-rhui-rpms                   51 k
 perl-PlRPC                               noarch                  0.2020-14.el7                   rhui-rhel-7-server-rhui-rpms                   36 k

Transaction Summary
======================================================================================================================================================
Install  1 Package (+10 Dependent packages)

Total download size: 82 M
Installed size: 354 M
Is this ok [y/d/N]: y
Downloading packages:
warning: /var/cache/yum/x86_64/7Server/mysql56-community/packages/mysql-community-common-5.6.38-2.el7.x86_64.rpm: Header V3 DSA/SHA1 Signature, key ID 5072e1f5: NOKEY
Public key for mysql-community-common-5.6.38-2.el7.x86_64.rpm is not installed
(1/11): mysql-community-common-5.6.38-2.el7.x86_64.rpm                                                                         | 257 kB  00:00:00     
(2/11): mysql-community-libs-5.6.38-2.el7.x86_64.rpm                                                                           | 2.0 MB  00:00:00     
(3/11): mysql-community-client-5.6.38-2.el7.x86_64.rpm                                                                         |  19 MB  00:00:00     
(4/11): perl-Compress-Raw-Zlib-2.061-4.el7.x86_64.rpm                                                                          |  57 kB  00:00:00     
(5/11): perl-Compress-Raw-Bzip2-2.061-3.el7.x86_64.rpm                                                                         |  32 kB  00:00:00     
(6/11): perl-DBI-1.627-4.el7.x86_64.rpm                                                                                        | 802 kB  00:00:00     
(7/11): perl-Data-Dumper-2.145-3.el7.x86_64.rpm                                                                                |  47 kB  00:00:00     
(8/11): perl-Net-Daemon-0.48-5.el7.noarch.rpm                                                                                  |  51 kB  00:00:00     
(9/11): perl-IO-Compress-2.061-2.el7.noarch.rpm                                                                                | 260 kB  00:00:00     
(10/11): perl-PlRPC-0.2020-14.el7.noarch.rpm                                                                                   |  36 kB  00:00:00     
(11/11): mysql-community-server-5.6.38-2.el7.x86_64.rpm                                                                        |  59 MB  00:00:02     
------------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                  33 MB/s |  82 MB  00:00:02     
Retrieving key from file:/etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
Importing GPG key 0x5072E1F5:
 Userid     : "MySQL Release Engineering <mysql-build@oss.oracle.com>"
 Fingerprint: a4a9 4068 76fc bd3c 4567 70c8 8c71 8d3b 5072 e1f5
 Package    : mysql-community-release-el7-5.noarch (installed)
 From       : file:/etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
Is this ok [y/N]: y
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
Warning: RPMDB altered outside of yum.
  Installing : mysql-community-common-5.6.38-2.el7.x86_64                                                                                        1/11 
  Installing : perl-Data-Dumper-2.145-3.el7.x86_64                                                                                               2/11 
  Installing : mysql-community-libs-5.6.38-2.el7.x86_64                                                                                          3/11 
  Installing : mysql-community-client-5.6.38-2.el7.x86_64                                                                                        4/11 
  Installing : 1:perl-Compress-Raw-Zlib-2.061-4.el7.x86_64                                                                                       5/11 
  Installing : perl-Net-Daemon-0.48-5.el7.noarch                                                                                                 6/11 
  Installing : perl-Compress-Raw-Bzip2-2.061-3.el7.x86_64                                                                                        7/11 
  Installing : perl-IO-Compress-2.061-2.el7.noarch                                                                                               8/11 
  Installing : perl-PlRPC-0.2020-14.el7.noarch                                                                                                   9/11 
  Installing : perl-DBI-1.627-4.el7.x86_64                                                                                                      10/11 
  Installing : mysql-community-server-5.6.38-2.el7.x86_64                                                                                       11/11 
  Verifying  : perl-Compress-Raw-Bzip2-2.061-3.el7.x86_64                                                                                        1/11 
  Verifying  : perl-Net-Daemon-0.48-5.el7.noarch                                                                                                 2/11 
  Verifying  : perl-Data-Dumper-2.145-3.el7.x86_64                                                                                               3/11 
  Verifying  : perl-PlRPC-0.2020-14.el7.noarch                                                                                                   4/11 
  Verifying  : mysql-community-client-5.6.38-2.el7.x86_64                                                                                        5/11 
  Verifying  : mysql-community-server-5.6.38-2.el7.x86_64                                                                                        6/11 
  Verifying  : 1:perl-Compress-Raw-Zlib-2.061-4.el7.x86_64                                                                                       7/11 
  Verifying  : mysql-community-common-5.6.38-2.el7.x86_64                                                                                        8/11 
  Verifying  : mysql-community-libs-5.6.38-2.el7.x86_64                                                                                          9/11 
  Verifying  : perl-DBI-1.627-4.el7.x86_64                                                                                                      10/11 
  Verifying  : perl-IO-Compress-2.061-2.el7.noarch                                                                                              11/11 

Installed:
  mysql-community-server.x86_64 0:5.6.38-2.el7                                                                                                        

Dependency Installed:
  mysql-community-client.x86_64 0:5.6.38-2.el7      mysql-community-common.x86_64 0:5.6.38-2.el7      mysql-community-libs.x86_64 0:5.6.38-2.el7     
  perl-Compress-Raw-Bzip2.x86_64 0:2.061-3.el7      perl-Compress-Raw-Zlib.x86_64 1:2.061-4.el7       perl-DBI.x86_64 0:1.627-4.el7                  
  perl-Data-Dumper.x86_64 0:2.145-3.el7             perl-IO-Compress.noarch 0:2.061-2.el7             perl-Net-Daemon.noarch 0:0.48-5.el7            
  perl-PlRPC.noarch 0:0.2020-14.el7                

Complete!
[root@veroj1 opt]# vi /etc/my.cnf
[root@veroj1 opt]# sudo systemctl start mysqld
[root@veroj1 opt]# sudo mysql_secure_installation  



NOTE: RUNNING ALL PARTS OF THIS SCRIPT IS RECOMMENDED FOR ALL MySQL
      SERVERS IN PRODUCTION USE!  PLEASE READ EACH STEP CAREFULLY!

In order to log into MySQL to secure it, we'll need the current
password for the root user.  If you've just installed MySQL, and
you haven't set the root password yet, the password will be blank,
so you should just press enter here.

Enter current password for root (enter for none): 
OK, successfully used password, moving on...

Setting the root password ensures that nobody can log into the MySQL
root user without the proper authorisation.

Set root password? [Y/n] y
New password: 
Re-enter new password: 
Password updated successfully!
Reloading privilege tables..
 ... Success!


By default, a MySQL installation has an anonymous user, allowing anyone
to log into MySQL without having to have a user account created for
them.  This is intended only for testing, and to make the installation
go a bit smoother.  You should remove them before moving into a
production environment.

Remove anonymous users? [Y/n] y
 ... Success!

Normally, root should only be allowed to connect from 'localhost'.  This
ensures that someone cannot guess at the root password from the network.

Disallow root login remotely? [Y/n] n
 ... skipping.

By default, MySQL comes with a database named 'test' that anyone can
access.  This is also intended only for testing, and should be removed
before moving into a production environment.

Remove test database and access to it? [Y/n] y
 - Dropping test database...
ERROR 1008 (HY000) at line 1: Can't drop database 'test'; database doesn't exist
 ... Failed!  Not critical, keep moving...
 - Removing privileges on test database...
 ... Success!

Reloading the privilege tables will ensure that all changes made so far
will take effect immediately.

Reload privilege tables now? [Y/n] y
 ... Success!




All done!  If you've completed all of the above steps, your MySQL
installation should now be secure.

Thanks for using MySQL!


Cleaning up...
