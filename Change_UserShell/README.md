Proactive EA to read the desired user accounts UserShell and change to /usr/bin/false to prevent login.

By default, user accounts have a UserShell of /bin/bash, but if you wish to use these accounts while preventing them from being able to login, this EA will change the UserShell to /usr/bin/false.

Rather than setting up as a proactive EA, you could just make this a script run via policy.  The script has to be run as root in order to change the UserShell.

Requirements for use:
* Enter local user accounts to have the script check in the USER array
* Enter the local admin account you do NOT wish to change the UserShell for in line 15 (if [ "${USER[$i]}" != "ladmin" ]; then)

To test the script works as expected WITHOUT changing the UserShell, comment out line 22.
