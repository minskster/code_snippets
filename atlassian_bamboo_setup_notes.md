# How to resolve some issues that appear in time of setup Atlassian Bamboo

## [If you don't know the bamboo admin password use recovery mode](https://confluence.atlassian.com/bamboo/lockout-recovery-process-952624910.html)
1. "-Datlassian.recovery.password=temporarypassword" to the JVM_SUPPORT_RECOMMENDED_ARGS in \bin\setenv.sh
2. Login with the user name: recovery_admin 

## [Prepare MySQL DB for Bamboo ](https://confluence.atlassian.com/bamboo/mysql-289276817.html)
```
mysql> CREATE DATABASE bamboo CHARACTER SET utf8 COLLATE utf8_bin;
mysql> GRANT ALL PRIVILEGES ON bamboo.* TO 'bamboouser'@'localhost' IDENTIFIED BY 'password';
mysql> FLUSH PRIVILEGES;
mysql> QUIT
```

# [Log mail sending](https://confluence.atlassian.com/bamkb/troubleshooting-notifications-email-im-216957451.html)
1. Open <bamboo-install>/bin/setenv.sh and set JVM_SUPPORT_RECOMMENDED_ARGS=-Dmail.debug=true
2. Add via GUI or <bamboo-install>/atlassian-bamboo/WEB-INF/classes/log4j.properties
log4j.logger.com.sun.mail=DEBUG
log4j.logger.com.atlassian.bamboo.mail=DEBUG
