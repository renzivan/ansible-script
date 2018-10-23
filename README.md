# ANSIBLE SCRIPTS
## SetUp Basic Wordpress Website with Nginx, MySQL, and PHP

### Install python remotely
 `$ ansible all -m raw -a "test -e /usr/bin/python || (apt -y update && apt install -y python-minimal)"`
### Run playbook
 `$ ansible-playbook playbooks/basic.yml -e "wp_db_name=<database_name>"`
#### Notes:
 - mysql username: root
 - mysql password: He\*\*\*\*\*\*\*
 - configure host credentials in **dev.ini**
 - location **/var/www/html/index.php**
