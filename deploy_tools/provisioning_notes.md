Provisioning a new site
=======================

## Required packages:

* nginx
* Python 3.8
* virtualenv + pip
* Git

eg, on Ubuntu:

sudo apt-get install python3.8 nginx git python3.8-venv
python3.8 -m venv ../virtualenv

## Nginx Virtual Host config

* see nginx.template.conf
* replace SITENAME with, e.g., staging.my-domain.com

## Systemd service

* see gunicorn-systemd.conf
* replace sitename with, e.g., staging.my-domain.com

## Folder structure:
Assume we have a user account at /home/username

/home/username
    └── sites
        └── SITENAME
             ├── database
             ├── source
             ├── static
             └── virtualenv
