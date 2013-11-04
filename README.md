setup-heroku-django
===================

A script that creates a django project for heroku. It installs and sets up everything.


Requirements
------------

This script only works in a CentOS environment. However, it should be easy to edit the script to use apt-get rather than yum, and then it should work fine on Ubuntu. 


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

* It installs all the relevant software you need to build and deploy a site with django.
* It sets up an empty django project and configures it for heroku.
* Finally, it actually deploys your empty project to heroku. 

When all is finished, you should be able to visit the URL heroku spits out at the end of the script, and you should see the default "It's working" message that all empty django projects start with.

From there, you can build away.
