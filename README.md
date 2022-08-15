# nagios-helpers
Command-line helper scripts for Nagios

Two quick commandline scripts to put Nagios hosts and services into maintenance mode and send an email to either a person or group with the details.  Make sure to modify the four variables at the top of these scripts.

#### How it works
These scripts will look for matching `service_desc` entries in the Nagios config files and identify the services attached. These are added to an array which is echoed out, showing which alerts will be suppressed, or enabled.  You _may_ need to change the `HOSTLIST` and `commandfile` variables if you have Nagios installed in a non-standard location. 

You'll need to either run these as root or the Nagios user.

Should be self-explanatory, but:
- <ins>USER</ins> is the email address notifications will be sent FROM.
- <ins>RECEIVER</ins> is the email address that notifications are sent TO.
- <ins>NURL</ins> is the Nagios base URL, used to construct links in the notifications.  
- <ins>CONAME</ins> is the Company name, which is added to the footer in notifications.

Disclaimer: These were thrown together quickly, and I haven't had a chance to clean up the code.  It's not hacky, it's just not beautiful, but it's on the to-do list.
