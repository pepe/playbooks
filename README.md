# Ansible playbooks used at LS

All [Ansible](http://www.ansibleworks.com) playbooks for company servers.

## Static server

This playbook installs and configure web server with git, ruby, nginx. It also
clones repos for all virtual hosts, create nginx vhosts and build
[Middleman](http://www.middlemanapp.com) apps.

Play this playbook with:

    ansible-playbook -i hosts static.yml
