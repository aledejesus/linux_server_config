
# Full Stack Web Developer Nanodegree
## Project 3: Linux Server Configuration
### Description
In this project I set up a Ubuntu 16.04 server on AWS Lightsail, modified the firewall and SSH configuration to make it more secure, installed Apache2 and deployed the [Item Catalog](https://github.com/aledejesus/item_catalog) project.

### SSH details
* IP address: 18.206.204.20
* Port: 2200

### URL
* http://18.206.204.20.xip.io

### Installed Software
The following linux packages had to be installed to correctly configure the server:
* Apache2: to serve web applications
* libapache2-mod-wsgi-py3: to serve the Item Catalog project
* PostgreSQL: database Item Catalog uses
* python3-pip: to install python 3 packages
* pyvenv: to create python 3.5 virtual environments
* finger: to get user info easier.

Additionally, all python packages in Item Catalog's requirements.txt file were installed.

### Configurations Modified
To secure and comply with project requirements, the following configuration changes were made:
* UFW
  * Restricted incoming connections to port 80 (HTTP), 123 (NTP) and 2200 (SSH)
  * Allowed outgoing traffic on any port
* SSH
  * Changed listening port to 2200 instead of port 22
  * Prohibited remote root login
  * Prohibited password-based login
* Apache2
  * Disabled default site
  * Enabled item catalog site (after creating its configuration file)

### Thrid-party resources

To be able to complete this project I had to read through one or more articles in the following websites:
* https://stackoverflow.com
* https://modwsgi.readthedocs.io
* https://httpd.apache.org
* https://ubuntuforums.org/
* https://classroom.udacity.com
