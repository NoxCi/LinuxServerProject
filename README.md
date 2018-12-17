# LinuxServerProject
Udacity Proyect 3

- IP address : 35.231.113.137 

- SSH port : 2200

- URL of web application : http://dev.project.com.35.231.113.137.xip.io/

- The sowftware installed was : python-pip, apache2, postgresql, libapache2-mod-wsgi, google-cloud-sdk, git. 

- The third-party resource i use was the Google Cloud Compute Engine to make VM intances intead of the recomended Amazon Lightsail, 'couse a i was unable to create a fully validate acount in AWS. Also xip.io was used to enable a DNS domain and been able to access the app in the cloud.

## Configuration
- The port setup was done as follows:

```$ sudo ufw allow 2200/tcp```

```$ sudo ufw allow www```

```$ sudo ufw allow ntp```

```$ sudo ufw enable```

- To create de ```grader``` user just required the next comand

```$ sudo adduser grader```


to make it sudo user i used 

```usermod -aG sudo grader```

then on my own machine i generate the ssh keys with

```ssh-keygen -t rsa -f ~/.ssh/my-ssh-key -C grader```

the public key then was submited in the metadata of the instance in Google Cloud Compute Engine.

- The UTC timezone was configure with

```sudo timedatectl set-timezone UTC```

- Then the catalog database user was created as follows

```$ sudo adduser catalog```

```$ sudo su postgres -c 'creatuser -dRSP catalog```

- After that the app was cloned in ```/var/www/ItemCatalog``` from github.

- to configure apache the next configuration file was used ```/etc/apache2/sites-available/dev.project.conf``` and set with ```$ sudo a2ensite dev.project.conf```.

- The line```10.142.0.2 dev.project.com``` was added to the file /etc/hosts in order to use xip.io.

- The file ```/etc/ssh/sshd_config``` was modify and change from ```port 22``` to ```port 2200``` to use ssh in port 2200.

- With pip the next libraries were installed: flask, packaging, oauth2client, redis, passlib, flask-httpauth, sqlalchemy, flask-sqlalchemy, psycopg2-binary, bleach, requests.
