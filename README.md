setup-heroku-django
===================

This is a bash script that creates a django project for heroku. Since setting everything up correctly for heroku is somewhat complicated, this script automates the task. It installs and sets up everything. Basically, if you want to create a django project and deploy it to heroku, you create a folder to house it, copy the `setup` script into that folder, then run the `setup` script. After that, you should have a live (empty) django site on heroku that you can work on.


Requirements
------------

* CentOS: This script only works in a CentOS environment. However, it should be easy to edit the script to use apt-get rather than yum, and then it should work fine on Ubuntu.
* Git: This script assumes you have git installed on your system.
* A heroku account: This script will ask for your heroku credentials at some point.


Usage
-----

On a CentOS machine, cd into a folder where you want your new django project to live, and copy the `setup` script there.

Then run the `setup` script. You need to specify a project name as the first argument:

    $ ./setup myproject

This will create an empty django project that is all ready to go. To deploy to heroku, you simply need to run this command:

    $ git push heroku master
    
What it does
------------

The `setup` script is a bash script that does the following:

* It installs all the relevant software you need to build and deploy a django site with heroku.
* It sets up an empty django project and configures it for heroku.
* Finally, it actually deploys your empty project to heroku. 

When all is finished, you should be able to visit the URL heroku spits out at the end of the script, and you should see the default "It's working" message that all empty django projects start with.

From there, you can build away.
