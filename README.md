# ANSIBLE SCRIPTS
## Setup Basic Wordpress Website with Nginx, MySQL, and PHP

### Install python remotely
 `$ ansible all -m raw -a "test -e /usr/bin/python || (apt -y update && apt install -y python-minimal)"`
### Run playbook with 1 parameter -- database name
 `$ ansible-playbook playbooks/basic.yml -e "wp_db_name=<database_name>"`
#### Notes:
 - default mysql username: **root**
 - default mysql password: He\*\*\*\*\*\*\*
 - configure host credentials in **dev.ini**
 - location **/var/www/html/index.php**


## Setup FTP User

### Run playbook with 3 parameters -- user, password, and directory access
 `$ ansible-playbook playbooks/ftp_user.yml -e "ftp_user=<user> ftp_pass=<passwd> bind_to=<directory>"`
#### Notes:
 - ftp user's files directory -- /home/**user**/ftp/files/

#### Update 10.24.18
##### Dynamic host and ssh login
 `$ ansible-playbook playbooks/ftp_user.yml -e "ftp_user=<user> ftp_pass=<passwd> bind_to=<directory> inv_host=<host_ip> inv_user=<ssh user> inv_pass=<ssh pass>"`


