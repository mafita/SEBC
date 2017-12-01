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

