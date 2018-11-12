# INSTALL ANSIBLE
 `$ apt-get update`
 `$ apt-get install software-properties-common`
 `$ apt-add-repository --yes --update ppa:ansible/ansible`
 `$ apt-get install ansible`

####Note:
 On older Ubuntu distributions, "software-properties-common" is called "python-software-properties".


# ANSIBLE SCRIPTS

## PLAYBOOK 1: Setup Basic Wordpress Website with Nginx, MySQL, and PHP
 - Configure target host
 `$ ansible-playbook playbooks/wordpress/setup_host.yml`
 - Setup Wordpress site
 `$ ansible-playbook playbooks/wordpress/setup_wordpress.yml`

#### Notes:
 - default mysql username: **root**
 - default mysql password: He\*\*\*\*\*\*\*
 - location **/var/www/html/index.php**


## PLAYBOOK 2: Setup FTP User
 - Configure target host
 `$ ansible-playbook playbooks/ftp_user/setup_host.yml`
 - Setup FTP User
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
