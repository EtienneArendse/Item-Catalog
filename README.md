# README for Linux Server Config project - (there is also a seperate README file on how to run the Item Catalog within Linux server.)

## IP address == 35.176.180.146

## SSH port == 2200

## web application URL ==

## A summary of software I installed and configuration changes made ==

python pip
Apache
Git
Virtual Environment
flask
wsgi python
jinja2
oauth2
rsa
oauth2client
postgresql
sqlalchemy
psycopg2
Configured firewall to allow port 80, 2200 and 123
Configured apache to run project
Configured postgresql to run database for project
Configured the local timezone to UTC
Changed the SSH port to 2200
Updated all currently installed packages
Created new user Grader
Set SSH login keys
Configured virtual host to run project

## A list of third-party resources I made use of to complete this project ==

https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps

## contents of the SSH key for the grader user (paste in "Notes to Reviewer" field) ==

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCyFxnfSTfQyzoOo/sybDUK1fVc+xIzBSvvFw43J035fM+WZKXbsGUIuRtJfNy0rCBK0yR8Quk8Ivy3XDMriFbPZ2VG8oBBhlNmsgNm4QYMiQf2eXIX+a23kwdOIqR1UQAJEKM7zHaaaC8bfvpc6w41B7nVlxW+haX3sEmU+4lZRE5gv8qOGPOKhUj9TRY094CScxaHaxD9B8ZhmUUNaiyvtjLPGMnw7vY8wQJBm4XX7nUJg9qEbIbxo5Qvtup8T2MMbXlMpJtqPispjikAMl0nbU+lZ9YdsJ0fUZihD7M7jObUwPlZa+oAVx4T0KQxVAeC5OfyDUznrsnUflu3es3F grader@ip-172-26-13-105


# notes for running and setting up Item-Catalog project

## Run the virtual machine!

Using the terminal, change directory to catalog (**cd catalog**), then type **vagrant up** to launch your virtual machine.


## Running the Item Catalog App
Once it is up and running, type **vagrant ssh**. This will log your terminal into the virtual machine, and you'll get a Linux shell prompt. When you want to log out, type **exit** at the shell prompt.  To turn the virtual machine off (without deleting anything), type **vagrant halt**. If you do this, you'll need to run **vagrant up** again before you can log into it.


Now that you have Vagrant up and running type **vagrant ssh** to log into your VM.  change to the /vagrant directory by typing **cd /vagrant**. This will take you to the shared folder between your virtual machine and host machine.

Type **ls** to ensure that you are inside the directory that contains project.py, database_setup.py, and two directories named 'templates' and 'static'

Now type **python database_setup.py** to initialize the database.

Type **python lotsofmenus.py** to populate the database items. (Optional)

Type **python project.py** to run the Flask web server. In your browser visit **http://localhost:8000** to view the Item Catalog App.  You should be able to view, add, edit, and delete items.


