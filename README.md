Trellis Stackdriver Logging
=========

Automates setting up Stackdriver Logging for all important service 
and sites configured with Trellis on Google Compute Engine or Amazon EC2 
instances. Currently Stackdriver Logging only officially supports Google 
Cloud or AWS.

If you are using GCE you should be good to go as the instances are already 
authorized to use the logging agent.

**If you are using AWS EC2 you will need to complete the authorization steps 
in the link below first before running this role.**

##### https://cloud.google.com/logging/docs/agent/authorization

Also it goes without saying you need to sign up for the Google Cloud Platform, 
they have a great **$300 / 60 day new customer promo where you can try out all 
their services, get free technical support from Google, also they guarantee 
they won't ding you with any overcharges when your trial is up if you don't 
stay.** You probably will though, I'm hooked and won't ever use another provider.

##### https://cloud.google.com/free-trial/

After the role has completed you can view your logs at the URL below

https://console.cloud.google.com/projectselector/logs

APIv2 is just being released so down the road I will set up importing logs 
from other environments. Pull requests always welcome if anyone feels like 
figuring it out before I do.

##### Service & Website Logs Monitored By Default
Also I listed their configured tags, you can use the tags to filter and search 
for specific services or events in the log viewer.

* fail2ban (fail2ban)
* memcache (memcache)
* mysql (mysql)
* mysql-slow (mysql-slow)
* nginx access (nginx-access)
* nginx error (nginx-error)
* php7.0-fpm (php7.0-fpm)
* php7.1-fpm (php7.1-fpm)
* syslog (syslog)
* every configured site's access log (nginx-access-example_com)
* every configured site's error log (nginx-error-example_com)

Requirements
------------

- Trellis - https://github.com/roots/trellis/
- Stackdriver Logging - https://cloud.google.com/logging/
- Google Compute Engine or AWS EC2 instance

Role Variables
--------------



Dependencies
------------



Example Playbook
----------------

Add this at the end of the Trellis server.yml file:

      roles:
         - { role: stackdriver-logging, tags: [stackdriver-logging] }

License
-------

MIT

Author Information
------------------

https://github.com/RiFi2k/
