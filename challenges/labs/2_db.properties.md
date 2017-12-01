
primer linea del log
[root@veroj1 cloudera-scm-server]# head -1 cloudera-scm-server.log 
2017-12-01 16:34:12,914 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfile.encoding=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.schema.dir=/usr/share/cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewGC, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Version: 5.12.1 (#6 built by jenkins on 20170818-0807 git: 9bdee611802535491d400e03c98ef694a2c77d0a)
[root@veroj1 cloudera-scm-server]# 


[root@veroj1 cloudera-scm-server]# grep "Started Jetty server" cloudera-scm-server.log 
2017-12-01 16:54:35,677 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.



vi /etc/cloudera-scm-server/db.properties
# Copyright (c) 2012 Cloudera, Inc. All rights reserved.
#
# This file describes the database connection.
#

# The database type
# Currently 'mysql', 'postgresql' and 'oracle' are valid databases.
com.cloudera.cmf.db.type=mysql

# The database host
# If a non standard port is needed, use 'hostname:port'
com.cloudera.cmf.db.host=10.0.2.4

# The database name
com.cloudera.cmf.db.name=cmf

# The database user
com.cloudera.cmf.db.user=cmf

# The database user's password
com.cloudera.cmf.db.password=cmf_password

# The db setup type
# By default, it is set to INIT
# If scm-server uses Embedded DB then it is set to EMBEDDED
# If scm-server uses External DB then it is set to EXTERNAL
com.cloudera.cmf.db.setupType=EXTERNAL
