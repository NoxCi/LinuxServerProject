# LinuxServerProject
Udacity Proyect 3

- IP address : 35.231.113.137 
- SSH port : 2200
- URL of web application : http://dev.project.com.35.231.113.137.xip.io/
- The sowftware install was : python-pip, apache2, postgresql, libapache2-mod-wsgi. Then the file /etc/apache2/sites-available/dev.project.conf was created to confure the apache server, the line```10.142.0.2 dev.project.com``` was added to the file /etc/hosts, /etc/ssh/sshd_config was modify from ```port 22``` to ```port 2200``` to use ssh in port 2200. With pip the next libraries was installed flask, packaging, oauth2client, redis, passlib, flask-httpauth, sqlalchemy, flask-sqlalchemy, psycopg2-binary, bleach, requests.
- The third-party resource i use was the Google Cloud Compute Engine to make VM intances intead of the recomended Amazon Lightsail, 'couse a i was unable to create fully validate acount in AWS.
