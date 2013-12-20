==========================================
Django Trigger Happy : Readability Service
==========================================

This project is a readability module for Django Trigger Happy 
that will handle the data from/to your readability account


Requirements :
==============
* django_th: 0.8.1
* readability-api: 0.2.2


Installation:
=============
to get the project, from your virtualenv, do :

.. code:: python

    pip install django-th-readability
    
then

.. code:: python

    python manage.py syncdb

to startup the database

Parameters :
============
As usual you will setup the database parameters.

Important parts are the settings of the available services :

Settings.py 
-----------

INSTALLED_APPS
~~~~~~~~~~~~~~

add the module th_rss to INSTALLED_APPS

.. code:: python

    INSTALLED_APPS = (
        'th_readability',
    )    

TH_SERVICES 
~~~~~~~~~~~

TH_SERVICES is a list of the services use by Trigger Happy

.. code:: python

    TH_SERVICES = (
        'th_readability.my_readability.Servicereadability',
    )

TH_READABILITY
~~~~~~~~~~~~~~
TH_READABILITY is the settings you will need to be able to add/read data in/from readability Service.

.. code:: python

    TH_READABILITY = {
        'consumer_key': 'abcdefghijklmnopqrstuvwxyz',
    }

Setting up : Administration
===========================

once the module is installed, go to the admin panel and activate the service readability. 

All you can decide here is to tell if the service requires an external authentication or not.

Once they are activated. User can use them.