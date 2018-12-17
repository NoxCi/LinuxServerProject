# LinuxServerProject
Udacity Proyect 3

- IP address : 35.231.113.137 

- SSH port : 2200

- URL of web application : http://dev.project.com.35.231.113.137.xip.io/

- The sowftware installed was : python-pip, apache2, postgresql, libapache2-mod-wsgi, google-cloud-sdk. 

- The third-party resource i use was the Google Cloud Compute Engine to make VM intances intead of the recomended Amazon Lightsail, 'couse a i was unable to create a fully validate acount in AWS. Also xip.io was used to enable a DNS domain and been able to access the app in the cloud.

## Configuration
The port setup was done as follows:

```$ sudo ufw allow 2200/tcp```

```$ sudo ufw allow www```

```$ sudo ufw allow ntp```

```$ sudo ufw enable```

The app was cloned in ```/var/www/ItemCatalog``` from github.

The configuration file for apache is /etc/apache2/sites-available/dev.project.conf.

The line```10.142.0.2 dev.project.com``` was added to the file /etc/hosts in order to use xip.io.

The file ```/etc/ssh/sshd_config``` was modify and change from ```port 22``` to ```port 2200``` to use ssh in port 2200. 

With pip the next libraries were installed: flask, packaging, oauth2client, redis, passlib, flask-httpauth, sqlalchemy, flask-sqlalchemy, psycopg2-binary, bleach, requests.
