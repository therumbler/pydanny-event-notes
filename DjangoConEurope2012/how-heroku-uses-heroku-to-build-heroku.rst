==========================================
How Heroku Uses Heroku To Build Heroku
==========================================

by Craig Kerstiens

* Works at Heroku
* http://twitter.com/craigkerstiens

What is Heroku?
=================

* Platform as a Service (PaaS)
* focuses on developer productivity
* 4000 heroku apps
* 500+ releases a day
* 200+ deploys a day
* 105 public github repos
* 85 people across 21 teams
* a cloud unix

Philosophies
===============

* Do 1 thing and do it well
* Run and forget
* Defined Contract/API
* Developer Environments
* Environment Parity

Do 1 thing and do it well
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Small functional apps
* KISSMetrics Data Loader

    * Open DB connection
    * Run query
    * Post data

* Others

    * OAuth
    * Vault
    * API
    * Core
    
Run and forget
~~~~~~~~~~~~~~~~

* Start an app
* Let them run
* Forget about them
* Alert me when things break

Sample standing up an app
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

    git clone git://github.com/opencomparison/opencomparison.git
    heroku create -s cedar
    git push heroku master