# Ansible playbooks used at LS

All [Ansible](http://www.ansibleworks.com) playbooks for company servers.

## Static server

This playbook installs and configure web server with git, ruby, nginx. It also
clones repos for all virtual hosts, create nginx vhosts and build
[Middleman](htttp://www.middlemanapp.com) apps.

Virtual hosts are listed in
[Middleman configuration](roles/middleman/vars/main.yml)

Play this playbook with:

    ansible-playbook -i hosts static.yml
