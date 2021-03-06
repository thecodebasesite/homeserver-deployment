## Ansible Roles for deploying my web apps.


### Community roles used:

* https://github.com/UnderGreen/ansible-role-mongodb
* https://github.com/geerlingguy/ansible-role-mysql
* https://github.com/geerlingguy/ansible-role-nginx
* https://github.com/geerlingguy/ansible-role-nodejs
* https://github.com/geerlingguy/ansible-role-pip
* https://github.com/ANXS/postgresql

### Homemade roles used:

* https://github.com/elmeriniemela/ansible-django
* https://github.com/elmeriniemela/ansible-mern
* https://github.com/elmeriniemela/ansible-flask
* https://github.com/elmeriniemela/ansible-acme
* https://github.com/elmeriniemela/ansible-nextcloud


### Usage

* Deploy Django applications `ansible-playbook ansible-django.yml -K`. For updates use `--tags=secrets,django`
* Deploy MERN stack application `ansible-playbook ansible-mern.yml -K`. For updates use `--tags=secrets,mern`
* Deploy flask based website thecodebase. `ansible-playbook ansible-flask.yml -K`
* Order wildcard certificate from LetsEncrypt with CloudFlare `ansible-playbook ansible-acme.yml -K`
* Deploy personal NextCloud server `ansible-playbook ansible-nextcloud.yml -K`

credentials.yml must contain the following secrets:
* website_db_password
* mysql_root_password
* website_secret_key
* mongodb_user_admin_password
* mongodb_root_admin_password
* mongodb_root_backup_password
* cloudflare_dns_api_key
* thecodebase_admin_password
* nextcloud_admin_password
* nextcloud_user_mysql_password