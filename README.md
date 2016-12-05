Stackdriver Logging
=========

Automates setting up Stackdriver Logging for Trellis on Google Compute Engine or Amazon EC2

Requirements
------------

- Trellis - https://github.com/roots/trellis/
- Stackdriver Logging - https://cloud.google.com/logging/
- Google Compute Engine or Amazon EC2 VM instance

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
