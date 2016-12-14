# Starter-Kit

This is a concise skeleton for building single-page web apps with [PostgreSQL] (https://www.postgresql.org/), 
Python ([Flask] (http://flask.pocoo.org/)), [Angular 2] (https://angular.io/), and [Heroku] (https://www.heroku.com/).

<p align="center">
  <a href="" target="_blank">
    <img alt="PPFA stack" src="frontend/www/assets/img/PPFA.png"></img>
  </a>
</p>

## Table of Contents
* [Getting Started] (#getting-started)
* [File Structure] (#file-structure)
* [Frequently Asked Questions] (#frequently-asked-questions)

## Getting Started

#### 1. Download and install the following software:

+ [OpenSSH] (https://sourceforge.net/projects/sshwindows/?source=typ_redirect) (required - for Windows users only)
+ [git] (https://git-scm.com/downloads) (required)
+ [VirtualBox] (https://www.virtualbox.org/wiki/Downloads) (required)
+ [Vagrant] (https://www.vagrantup.com/downloads.html) (required)

#### 2. Open the command line (terminal) and type the following command:
>
```bash
git clone https://github.com/maangulo12/starter-kit.git
```

![Alt text] (frontend/www/assets/img/step2.png "Step 2")

#### 3. Change directory into the downloaded project:
>
```bash
cd starter-kit
```

![Alt text] (frontend/www/assets/img/step3.png "Step 3")

#### 4. Run vagrant to setup the development environment:
>
```bash
vagrant up
```

![Alt text] (frontend/www/assets/img/step4.png "Step 4")

*This step may take some time.*

#### 5. SSH into the virtual machine:
>
```bash
vagrant ssh
```

![Alt text] (frontend/www/assets/img/step5.png "Step 5")

*It may ask you to enter a passphrase and a password.* 

```
Passphrase for key: (just press Enter)
Password: vagrant
```

#### 6. Change directory into the vagrant folder:
>
```bash
cd /vagrant/
```

![Alt text] (frontend/www/assets/img/step6.png "Step 6")

#### 7. Run the task runner to run the application:
>
```bash
gulp
```

![Alt text] (frontend/www/assets/img/step7.png "Step 7")

#### 8. Open [http://localhost:3000](http://localhost:3000):

![Alt text] (frontend/www/assets/img/step8.png "Step 8")

### File Structure

```
starter-kit/
 ├──backend/                   * our backend (server-side) code folder
 |   ├──__init__.py            * our main module for this app
 |   ├──config.py              * our app config module
 |   ├──models.py              * our database models
 │   ├──view.py                * our app views
 │   │
 │   └──api/                   * our api folder
 │       └──v1/                * our api v1 folder
 |           ├──__init__.py    * our api v1 package module
 │           └──api.py         * implements the first api endpoints 
 │                               (this module can be broken into multiple modules or packages)
 |
 ├──frontend/                  * our frontend (client-side) code folder
 |   ├──this needs work!
 │
 ├──local/                     * our local config folder
 │   ├──pg_hba.conf            * config file used by vagrant for authentication to the local database 
 │   └──pg_ident.conf          * config file used by vagrant for authentication to the local database
 |
 ├──.gitignore                 * specifies files that git should ignore
 ├──app.json                   * specifies information required to run this app on Heroku
 ├──gulpfile.js                * our build system config file for automating tasks
 ├──manage.py                  * our python script for performing commands
 ├──package.json               * specifies our node dependencies
 ├──Procfile                   * what Heroku uses to deploy the app
 ├──README.md                  * this README file 
 ├──requirements.txt           * specifies our python dependencies
 ├──runtime.txt                * specifies our python runtime version
 ├──server.py                  * our python server script 
 ├──tsconfig.json              * specifies options for the typescript compiler  
 ├──typings.json               * specifies packages needed by the typescript compiler
 └──Vagrantfile                * what vagrant uses to configure the virtual machine
```

## Database on the Virtual Machine

#### PostgreSQL Database
    Host: localhost
    Port: 5432
    Database: app_db
    Username: postgres
    Password: password

#### pgAdmin

pgAdmin is a free to use, open-source management and administration tool for PostgreSQL.
To download the application, go to [pgAdmin] (https://www.pgadmin.org/). 

#### Connecting to PostgreSQL Database using pgAdmin



## Frequently Asked Questions

#### 1. How do I run the application again after turning off my computer?
Follow steps 3 through 8 from above.

#### 2. I have made changes to a page, but browser is not displaying the changes.

Close the browser. Restart the application. Cancel the gulp command 
(press CTRL-C) and run the gulp command once again. Open the browser again 
and go to [http://localhost:3000](http://localhost:3000).

#### 3. Firefox is not displaying my changes

## Resources for Learning

[Angular 2 in 60 Minutes] (https://www.youtube.com/watch?v=-zW1zHqsdyc)