Provisioning a new site
=======================

## Requires packages:

* nginx
* Python 3
* Git
* pip
* virtualenv

eg, on Ubuntu:

	sudo apt-get install nginx git python3 python3-pip
	sudo pip3 install virtualenv

## Nginx Virtual Host config

* see nginx.sites-available.template.lists.scientistlearnscode.co.uk
* replace "list.scientistlearnscode.co.uk" with relevant sitename

## Systemd setup for gunicorn

* create a gunicorn.service file in /etc/systemd/system/
* see systemd.template.gunicorn.service
* replace "list.scientistlearnscode.co.uk" with relevant sitename

## Folder structure:
Assume we have a user account at /home/username

/home/username
-sites
	-SITENAME
		- database
		- source
		- static
		- virtualenv