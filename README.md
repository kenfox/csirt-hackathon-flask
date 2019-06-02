# csirt-hackathon-flask-app

A minimal web app developed with [Flask](http://flask.pocoo.org/) framework. This app is developed by [XD-DENG](https://github.com/XD-DENG).

This web app contains the following essential elements of a web application:

- URL Building

- Authentication with Sessions

- Template & Template Inheritance

- Error Handling

- Integrating with *Bootstrap*

- Interaction with Database (SQLite)

- Invoking static resources

For more basic knowledge of Flask, you can refer to [a tutorial on Tutorialspoint](https://www.tutorialspoint.com/flask/).

## Getting Started
**Note**: This documentation is based on tests carried out on a clean Ubuntu 18.04 LTS version.

Before running the app, make sure you have the right environment for it and essential dependencies installed.

As this app is written in Python3, we need **python3**. To install the required dependencies, **pip3** is recommended and as a best practice, we want to isolate the environment for this app from the global environment so to do that we need **virtualenv**. We use **git** to pull this project to local working directory.

Once you have python3 and pip3 installed, lastly install virtualenv by typing the following in the `Terminal`:

`sudo pip3 install virtualenv`


## How to Run
**Step 1:** `cd` over to the directory that will be the parent dir for this project. Copy all the lines below into a new file and save it as **setup.sh**

```
#!/bin/bash

virtualenv -p python3 csirt-hackathon-venv
cd ./csirt-hackathon-venv
git clone https://csirt-gitlab.cisco.com/siddhrao/csirt-hackathon-flask-app.git
. ./bin/activate
pip3 install -r ./csirt-hackathon-flask-app/requirements.txt
./bin/python3 ./csirt-hackathon-flask-app/app.py
```

**Step 2:** Make it executable by typing `chmod +x setup.sh` in the terminal and run the executable by typing `. ./setup.sh`. You might be asked to enter your gitlab credentials to clone the repo. Wait while the script sets up the environment and installs dependencies for you.
# **Step 3:** Finally, run the app by typing `./bin/python3 ./csirt-hackathon-flask-app/app.py`


## Details about This Toy App

There are three tabs in this toy app

- **Public**: this is a page which can be accessed by anyone, no matter if the user has logged in or not.

- **Private**: Only logged-in user can access this page. Otherwise the user will get a 401 error page.

- **Admin Page**: This part is only open to the user who logged in as "Admin". In this tab, the administrator can manage accounts (list, delete, or add).


A few accounts were set for testing, like ***admin*** (password: admin), ***test*** (password: 123456), etc. You can also delete or add accounts after you log in as ***admin***.


## References

- http://flask.pocoo.org/

- https://www.tutorialspoint.com/flask/


## Credict
Image private.jpg: https://commons.wikimedia.org/wiki/File:(315-365)_Locked_(6149414678).jpg
Image public.jpg: https://commons.wikimedia.org/wiki/File:Drown%3F!_(131380682).jpg

