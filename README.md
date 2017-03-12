# Missiley
Udacity Fullstack Web Developer Project 8: A Country-Missile Catalog on the cloud

This project is built with Python backend with:
- Flask as the web framework to expose APIs
- Spectre.css as the CSS framework for the look and feel
- OAuth implementation using GPlus and Facebook
- CRUD operations into an SQLLite Database
- SQL Alchemy as an ORM

##Public URL


##IP Address:
52.87.241.178

##SSH Port:
2222

##SSH Key location:


##Configuration:
- Base OS: Ubuntu with 512MB RAM, 1 vCPU, 20GB SSD


##Third party resources:




##How to Use?
1. Unpack the zip into a folder or clone the repo.
2. Using the VagrantFile attached, start a VM.
```
vagrant up
```
SSH into the machine as `vagrant` user
```
vagrant ssh
```
3. Place the rest of the contents (other than the VagrantFile) in the /vagrant folder and move to that folder.
```
cd /vagrant/catalog
```
4. Setup the Database by running:
```
python databsae_setup.py
```
5. To initialiaze the databse with some values:
```
python lots_of_missiles.py
```
4. At the root level, run
```
python app.py
```

##Author
Akshay Menon

##License
MIT

##Copyright
Copyright &copy; 2016 Akshay Menon


##Rubrics:
User Management

CRITERIA
MEETS SPECIFICATIONS
Can you log into the server as the user grader using the submitted key?

The SSH key submitted with the project can be used to log in as grader on the server.

Is remote login of the root user disabled?

You cannot log in as root remotely.

Is the grader user given sudo access?

The grader user can run commands using sudo to inspect files that are readable only by root.

Security

CRITERIA
MEETS SPECIFICATIONS
Is the firewall configured to only allow for SSH, HTTP, and NTP?

Only allow connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).

Are users required to authenticate using RSA keys?

Key-based SSH authentication is enforced.

Are the applications up-to-date?

All system packages have been updated to most recent versions.

Is SSH hosted on non-default port?

SSH is hosted on non-default port.

Application Functionality

CRITERIA
MEETS SPECIFICATIONS
Is there a web server running on port 80?

The web server responds on port 80.

Has the database server been configured to properly serve data?

Database server has been configured to serve data (PostgreSQL is recommended).

Has the web server been configured to serve the Item Catalog application?

Web server has been configured to serve the Item Catalog application as a WSGI app.

Documentation

CRITERIA
MEETS SPECIFICATIONS
Is a README file included in the GitHub repo containing all specified information?

A README file is included in the GitHub repo containing the following information: IP address, URL, summary of software installed, summary of configurations made, and a list of third-party resources used to completed this project.

