# Udacity Project: Linux Server Configuration

This repository serve information about the linux server configuration for my Catalog-App.  
The server run on Amazon EC2 Instance with image of "Ubuntu, 18.04 LTS"

### Instance Information

|||
|-|-|
|URL|http://ec2-3-95-161-81.compute-1.amazonaws.com|
|IP address|3.95.161.81|
|SSH Port|2200|

## Ubuntu packages installed

* Apache HTTP Server
* mod_wsgi
* PostgreSQL
* python-pip
* libpq-dev

## Configurations

* SSH
  * Set Port to 2200
  * Disable root login
  * Disable password authentication
* Firewall
  * Deny all incoming
  * Allow all outgoing
  * Allow:
    * SSH custom port 2200
    * HTTP 80 (WWW)
    * NTP 123

## More steps done to get the server running

* Update all system packages
* Add new user “grader”
  * Give sudo access
  * Generate RSA key for authentication
* Create new database “catalog”
* Install Python packages:
  * httplib2
  * requests, flask
  * flask_login
  * oauth2client
  * sqlalchemy
  * passlib
  * psycopg2
* Cloning my Catalog App repository
* Create WSGI file and use it in apache configuration file

## Authors

* **Kfir Klichevski** - *Initial work* - [kklichevski](https://github.com/kklichevski/)
