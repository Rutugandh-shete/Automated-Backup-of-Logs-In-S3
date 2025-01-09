
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
     
* Tomcat logs
 1. /opt/tomcat/log
 2. /opt/tomcat/catlina.out

# How to take automated logs backup to s3 bucket 
**1. Launch one instance.**
![image](https://github.com/user-attachments/assets/f4a3ec59-23e2-4ede-b15a-95dad545a3da)
**2. Create s3 bucket.**
![image](https://github.com/user-attachments/assets/f300078c-4d66-4db8-98b8-e88fe1e9b09b)
**3. Create one role and give s3 full permmision**
![image](https://github.com/user-attachments/assets/c6fb388c-17fb-4d46-9234-cd262041d271)
**4. Attach role to instance**
![image](https://github.com/user-attachments/assets/59e08675-f991-407c-9b62-4341784c7cd9)
**5. Configure AWS**
![image](https://github.com/user-attachments/assets/aec81b56-a7e2-4aa8-8fe6-11c36e8f29b0)
**6. Install crond on your machine**
![image](https://github.com/user-attachments/assets/73f232b5-c68a-4b75-9372-2345749d59e8)
**7. Create one cron job to store your logs to s3 bucket**
````
sudo crontab -e

````

````

* * * * * aws s3 sync /var/log/ s3://<bucket-name>/log_file_name --exclude "*" --include "*.log"

````
![image](https://github.com/user-attachments/assets/ad07dee4-0d92-43f5-bb9b-7e29770b7cb8)

# Logs are stored on s3 bucket for every minute 
![image](https://github.com/user-attachments/assets/37886f83-9ebd-4d7c-bc96-fb698dd4e5bf)


