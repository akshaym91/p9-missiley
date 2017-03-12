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
2200

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

