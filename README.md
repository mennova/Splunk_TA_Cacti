# Splunk\_TA\_Cacti version 1.0.0

## Setup and Install

### Search Head
Install and Deploy the app to the search head.

On the search head, the add-on will provide:
 * search time extractions, lookups, macros and event types

To complete the install, you will need to update the follow:
 * macros.conf
   * *cacti_index*: replace index=\* with the appropriate index

### Cacti Server / Universal Forwarder
To complete the ingestion of data, deploy the Splunk\_TA\_Cacti to the forwarder installed on the same host as your Cacti implementation.  If you have multiple installs, you can deploy it across multiple Cacti servers.

For this add-on to work, you will need to have installed the Cacti Mirage plugin to the Cacti servers.  In addition, you will need the following information:
 * Path to Cacti install (i.e. /var/www/html/cacti or /usr/share/lib/cacti)
 * Path to mirage\_poller\_output.log (i.e /var/www/html/cacti/log/mirage\_poller\_output.log)
 * Index to send data to (either default or index=cacti, etc)

For deploying the add-on, copy the following files from the *default* directory to the *local* directory.
 * inputs.conf

Edit the *local/inputs.conf* file and make the following changes:
 * enable all inputs 
    disabled = false

Copyright 2016 Matthew Modestino, Philippe Tang, Menno Vanderlist

For documentation, see README.txt
