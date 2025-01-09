# What is Logs?
#### Linux and application that run on it generates messages which is stored in different forms is called logs. Linux uses a set of configuration files, directories, programs, commands and daemons to create, store and recycle these log messages. 

# To see logs in ubuntu machine
````
ls /var/log

````
![image](https://github.com/user-attachments/assets/4601e36d-31ae-419d-83fb-cd8e92d051fa)

# Important logs files for troubleshooting 
*  syslog: System realted infomartion, contains infomartion like processes, daemons.
*  dmesg: Useful for hardware or driver realted information.
*  auth.log: Used to check user authentication, ssh logins and sudo attempts.

# How to check logs as per system, server, application, database.
* System logs:
  1. /var/log/syslog
  2. /var/log/auth.log
  3. /var/log/dmesg
  4. /var/log/boot.log
* Nginx logs:
  1. /var/log/nginx/access.log
  2. /var/log/nginx/error.log
  3. /var/log/nginx
* Httpd logs
  1. /var/log/httpd
  2. /var/log/access_log
  3. /var/log/error_log
* MySQL logs
  1. /var/log/mysql/error.log
*Tomcat logs
 1. /opt/tomcat/log
 2. /opt/tomcat/catlina.out

