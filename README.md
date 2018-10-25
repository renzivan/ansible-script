# ANSIBLE SCRIPTS

## Install python for ansible to run
 `$ ansible all -m raw -a "test -e /usr/bin/python || (apt -y update && apt install -y python-minimal)"`

## Configure inventory
 `$ ansible-playbook playbooks/setup_host.yml`
#### Notes:
 - it replaces the existing inventory
 - can only configure 1 host

## Setup Basic Wordpress Website with Nginx, MySQL, and PHP 
 `$ ansible-playbook playbooks/setup_wordpress.yml`
#### Notes:
 - default mysql username: **root**
 - default mysql password: He\*\*\*\*\*\*\*
 - location **/var/www/html/index.php**


## Setup FTP User
 `$ ansible-playbook playbooks/ftp_user.yml`
#### Notes:
 - ftp user's files directory -- /home/**user**/ftp/files/

