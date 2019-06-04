# csirt-hackathon-flask

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

Clone the Ansible repo to bootstrap the instance

```bash
git clone REPO_URL
cd csirt-hackathon-ansible
ansible-playbook -i inventory playbook.yml
```

Install pip dependencies and run the application using honcho.
Honcho will read the Procfile to run the webapp via gunicorn.

```bash
cd /opt/csirt
pipfile install
pipfile run honcho start
```

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

