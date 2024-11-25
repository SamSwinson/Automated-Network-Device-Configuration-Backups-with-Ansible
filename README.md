# Automated Network Device Configuration Backups with Ansible

This is a simple and easy way to implement automatic network device configuration backups.

I have the Ansible playbook set up to pull the device configurations and then push them to a Gitlab/Github. In my setup a make a new directory for each date to save the configurations in, but, if you want to easily track changes between backups then have them all in a single directory and use either Gitlab/Github to compare the changes.

There are 2 ways to implement this. The first is using a local account on each device in which case you both the hosts local account file for the ansible hosts file and then vault local account for your vault. This will allow you to cycle through all the hosts with different user names and passwords. If you are using a single account utilising AAA then use the single account hosts and vault files, these are a bit simpler because it is just 2 variables we can pass into the playbook.
