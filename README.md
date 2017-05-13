# Missiley
Udacity Fullstack Web Developer Project 8: A Country-Missile Catalog on the cloud

This project is built with Python backend with:
- Flask as the web framework to expose APIs
- Spectre.css as the CSS framework for the look and feel
- OAuth implementation using GPlus and Facebook
- CRUD operations into an Postgres Database
- SQL Alchemy as an ORM

## Public URL
[http://52.87.241.178/](http://52.87.241.178/)

## IP Address:
52.87.241.178

## SSH Port:
2200

## SSH Key location:
`/home/grader/.ssh/authorized_keys`


## Configuration:
- Base OS: Ubuntu with 512MB RAM, 1 vCPU, 20GB SSD
- Updated all package `sudo apt-get update` `sudo apt-get upgrade`
- Installed git `sudo apt-get install git-all`
- Installed Apache `sudo apt-get install apache2`
- Installed mod_wsgi `sudo apt-get install python-setuptools libapache2-mod-wsgi`
- Installed PostgreSQL `sudo apt-get install postgresql`
- Navigated to `/var/www/html`
- Cloned code repo from git hub `git clone https://github.com/akshaym91/p9-missiley.git`
- Created a new user grader `sudo adduser grader`
- Added `grader` to sudoers
- `touch /etc/sudoers.d/grader`
- `vim /etc/sudoers.d/grader` and append:
```
grader ALL=(ALL:ALL) ALL
```
- Generated keys on local machine using`ssh-keygen`
- Copied public key to the dev environment under `.ssh/authorized_keys`
- Changed permissions for .ssh
- Reloaded service `sudo service ssh restart`
- Tested logging in as `grader` by `ssh -i [privateKeyFilePath] grader@52.87.241.178`
- Change default ssh port at `/etc/ssh/sshd_config`
- Changed firewall settings on both Lightsail account and UFW
```
sudo ufw allow 2200/tcp
sudo ufw allow 80/tcp
sudo ufw allow 123/udp
sudo ufw enable 
```
- Login as `postgres` by `sudo su - postgres` and got into `psql` shell
- Set up database
```
CREATE DATABASE missiley;
CREATE USER missiley;
ALTER ROLE missiley WITH PASSWORD '<password>';
GRANT ALL PRIVILEGES ON DATABASE missiley TO missiley;
\q
exit
```
- In the code base made appropriate changes to use Postgres instead of Sqlite
- `engine = create_engine('postgresql://missiley:password@localhost/missiley')`
- Set up the webserver to serve the files from the app by using resources found [here](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/)
- Added the domain to the developer console in both google oauth and facebook oauth.
- Restarted webserver

## Third party resources:

1. [Flask+SQLAlchemy](http://stackoverflow.com/questions/37950713/deploying-app-using-flask-with-apache-and-sqlalchemy)
2. [IO Error](http://stackoverflow.com/questions/12201928/python-open-method-ioerror-errno-2-no-such-file-or-directory)
3. [Running wsgi application on Apache](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/)
4. [Difference between SQLLite and Postgres](https://www.digitalocean.com/community/tutorials/sqlite-vs-mysql-vs-postgresql-a-comparison-of-relational-database-management-systems)
5. [Flask application on ubuntu](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)

## Author
Akshay Menon

## License
MIT

## Copyright
Copyright &copy; 2016 Akshay Menon

