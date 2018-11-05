# ANSIBLE SCRIPTS

## Configure inventory
 `$ ansible-playbook playbooks/setup_host.yml`

#### Notes:
 - it replaces the existing inventory
 - can only configure 1 host

## Install python for ansible scripts to execute
 `$ ansible all -m raw -a "test -e /usr/bin/python || (apt -y update && apt install -y python-minimal)"`

## PLAYBOOK 1: Setup Basic Wordpress Website with Nginx, MySQL, and PHP 
 `$ ansible-playbook playbooks/setup_wordpress.yml`

#### Notes:
 - default mysql username: **root**
 - default mysql password: He\*\*\*\*\*\*\*
 - location **/var/www/html/index.php**


## PLAYBOOK 2: Setup FTP User
 `$ ansible-playbook playbooks/ftp_user.yml`

#### Notes:
 - ftp user's files directory -- /home/**user**/ftp/files/

## PLAYBOOK 3: Migrate site
 `$ ansible-playbook playbooks/migrate.yml`

#### Notes:
 - Entered path must be on this format (/var/www/...)
    - e.g. migrate html folder to remote server
    - /var/www/html (no slash at the end)
 - The path entered will be the path used by the remote destination server
