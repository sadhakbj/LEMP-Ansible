# LEMP server automation using Ansible

Server automation for a php project with Nginx, MySQL.

This script automates the following tasks:

- Installation of the following services and extensions:
  - PHP with required extensions (e.g. MySQL, Xml etc) and composer
  - Nginx
  - MySQL Serrver and Client
- Removes the default nginx vhost file
- Updates a vhost file
- Creates new non root low privileged user

## Installation and running

- Clone the repository: `git clone git@github.com:sadhakbj/LEMP-Ansible.git`
- Update the host file to include the server ip address
- Update environment variables as per the need inside `roles/web/vars/main.yml` or `roles/db/vars/main.yml`
- Update nginx vhost file as per your need inside: `roles/web/templates/vhost.j2`
- Make sure you have ssh access to the provided host / server
- Run the following command to automate the server setup: `ansible-playbook -i hosts site.yml`
